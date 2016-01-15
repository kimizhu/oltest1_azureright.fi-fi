---
description: na
keywords: na
title: Configuring Applications for Azure Rights Management
search: na
ms.date: na
ms.service: rights-management
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea09cbc5-b98b-444e-8b60-5bc3cb199c36
---
# Oikeuksien hallinnan Office-integrointi
Luotaessa tai käytettäessä sisältöä, joka on suojattu sisältöoikeuksien hallinnan (IRM) avulla, vain seuraavat Microsoft Office -versiot ovat tuettuja.

|Tähän Office-tuoteperheeseen…|…liittyvät nämä Rights Management -rajoitukset|
|---------------------------------|--------------------------------------------------|
|[!INCLUDE[MO_O15ProPlus_1](../Token/MO_O15ProPlus_1_md.md)]|Tuettu tässä versiossa.|
|Microsoft Office 2010|Tuettu tässä versiossa.<br /><br />Oikeuksien hallinnalla suojatun sisällön julkaisemiseen tarvitaan Office Professional Plus. Oikeuksien hallinnalla suojatun sisällön käyttämiseen tarvitaan Office Standard.|
|Microsoft Office 2007|Ei tuettu tässä versiossa.|

## Office 2013 -asiakaskokoonpano
Kun [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -ratkaisulla halutaan tukea [!INCLUDE[MO_O15ProPlus_2](../Token/MO_O15ProPlus_2_md.md)] -ohjelmiston IRM-ominaisuuksia, on tehtävä seuraavat toimet.

#### Office 2013:n asentaminen ja määrittäminen siten, että Rights Management -ratkaisua käytetään yhdessä Office IRM -ominaisuuksien kanssa.

1.  Asenna [!INCLUDE[MO_O15ProPlus_2](../Token/MO_O15ProPlus_2_md.md)] lataussivustosta.

2.  Suorita seuraava rekisterin päivityskomento järjestelmänvalvojan oikeuksin suoritettavasta komentokehotteesta:

    ```
    reg add "HKEY_CURRENT_USER\SOFTWARE\Microsoft\Office\15.0\Common\DRM" /t REG_DWORD /v "UseRMSOnline" /d 1 /f
    ```

3.  Kirjaudu sisään Office-sovelluksiin [!INCLUDE[o365_1](../Token/o365_1_md.md)] -tunnistetiedoilla.

## Office 2010 -asiakaskokoonpano
Kun [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -ratkaisulla halutaan tukea Office 2010:n IRM-ominaisuuksia, on tehtävä seuraavat toimet.

> [!NOTE]
> Koska näitä toimia ei voi peruuttaa, niiden suoritukselle suositellaan testausympäristöä.

#### Office 2010:n asentaminen ja määrittäminen siten, että Rights Management -ratkaisua käytetään yhdessä Office IRM -ominaisuuksien kanssa.

1.  Rekisteröi Office 365 -vuokraajatili.

    Näin saat kelvollisen Office 365 -käyttäjätunnuksen ja sähköpostitilin (kuten user@mytestdomain.onmicrosoft.com), joita voit käyttää, kun kirjaudut Office 365 -portaalisivustoon, ja myöhemmin, kun käytät Exchange Onlinea isännöitynä sähköpostipalveluna.

    Lisätietoja: [Office 365:een kirjautuminen](http://onlinehelp.microsoft.com/fi-fi/office365-enterprises/ff637600.aspx).

2.  Asenna yhteensopiva Windows-käyttöjärjestelmän versio, johon sisältyy tarvittava RMS-asiakas.

    [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] edellyttää RMS-asiakasta, joka tulee seuraavien tuotteiden mukana: Windows Vista, Windows 7 SP1, Windows Server 2008 ja Windows Server 2008 R2 SP1 sekä Office 2010. Voi olla myös tarpeen asentaa seuraavat hotfix-korjaukset, jos AD RMS -klusteri on päivitetty käyttämään salaustilaa 2, joka käyttää avainpituudeltaan 2 048 -bittisiä RSA-avaimia. Jos kyseessä on Windows Vista- tai Windows Server 2008 -tietokone, asenna [artikkelissa 2627272](http://support.microsoft.com/kb/2627272) mainittu hotfix-korjaus. Jos kyseessä on Windows 7- tai Windows Server 2008 R2 -tietokone, asenna [artikkelissa 2627273](http://support.microsoft.com/kb/2627273) mainittu hotfix-korjaus. Jos myös Office 2010 -sovelluksissa ilmenee virheitä, tarkista, että olet asentanut [Office 2010 -hotfix-korjauksen, johon viitataan artikkelissa 2596501](http://support.microsoft.com/kb/2596501) ja joka auttaa korjaamaan kyseiset virheet. Lisätietoja salaustila 2:sta: [AD RMS Cryptographic Modes (AD RMS:n salaustilat)](http://technet.microsoft.com/library/hh867439)

    [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] tukee sekä 32-bittisiä (x86) että 64-bittisiä (x64) asennuksia.

3.  Asenna Office 2010 joko asennusvälineestä tai käyttämällä Office 2010:n 60 päivän kokeiluversiota, jonka voi ladata Microsoftin verkkosivustosta napsauttamalla [tätä](http://technet.microsoft.com/fi-fi/evalcenter/ee390818.aspx).

4.  Kirjaudu sisään Office 365 -portaalisivustoon ja määritä Office 2010 -työpöytäsi käyttämään Office 365 -ohjelmistoa.

    Kun kirjaudut sisään Office 365 -sivustoon, asenna Office 365 Sign-In Assistant seuraavalla tavalla:

    1.  Valitse sivun yläosasta **Aloitus**.

    2.  Valitse Aloitus-sivulta **Ohjelmisto**-ruutu ja valitse sitten **Aseta Office-työpöytäsovellukset toimimaan Office 365 Technical Preview'n kanssa**.

    3.  Kun Office 365:n ohjattu päivitys käynnistyy, seuraa näytössä näkyviä ohjeita ja asenna Microsoft Sign-In Assistant ja muut tarvittavat Office-päivitykset sekä käynnistä tietokone uudelleen.

5.  Lataa ja suorita Service Location Registry Script Generator -työkalu [lataussivustosta](http://go.microsoft.com/fwlink/p/?LinkId=242548).

    Kun työkalu on ladattu, pura se kansioon, tarkista, että kaikki Office-sovellukset on suljettu, ja suorita työkalu sitten ohjeiden mukaan Windows-komentosarjatiedoston luomiseksi. Suoritettavan tiedoston nimi on seuraava: Microsoft.AADRM.ServiceLocationRegScriptTool.exe.

    Lisätietoja tämän työkalun suorituksesta on seuraavassa osiossa.

6.  Suorita luotu Windows-komentosarjatiedosto, jotta asiakas tulee määritettyä käyttämään [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -ratkaisua.

    > [!NOTE]
    > Tämän komentosarjatyökalun käyttö ei edellytä järjestelmänvalvojan oikeuksia, mutta työkalua suorittavalla käyttäjällä täytyy olla kirjoitusoikeudet työkalun sisältävään kansioon.

7.  Avaa Outlook 2010 ja määritä Exchange Online -sähköpostiasetukset.

    Jos kyseessä on ensimmäinen kerta, kun avaat Outlookin tässä tietokoneessa, sinua pyydetään määrittämään sähköpostitili. Voit jatkaa prosessia, jonka kuluessa Exchange-sähköpostiasetuksissa otetaan käyttöön Exchange Online ja vuokraajatili.

    Lisätietoja: [Sähköpostitilin lisääminen tai poistaminen](http://office.microsoft.com/fi-fi/outlook-help/add-or-remove-an-email-account-HA010354414.aspx).

### Service Location Registry Script Generator -työkalu
Jotta tietokone voidaan määrittää käyttämään Office 2010:tä [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -ratkaisun kanssa, tarvitaan komentoriviapuohjelma, jonka nimi on Service Location Registry Script Generator. Tämän työkalun voi suorittaa kuka tahansa käyttäjä normaalilta komentoriviltä, mutta työkalu on suoritettava kansiossa, johon käyttäjällä on kirjoitusoikeudet, sillä se luo komentosarjatiedoston, jota käytetään määrittämään Office 2010 toimimaan Rights Management -ratkaisun kanssa. Kun työkalu suoritetaan, se pyytää käyttäjää antamaan Office 365 -tunnistetiedot erityisessä valintaikkunassa. Näiden tunnistetietojen avulla se luo komentosarjatiedoston, jolla käyttäjän tietokoneen asetukset määritetään.

Kun työkalu on suoritettu, järjestelmänvalvojan on suoritettava luotu komentosarjatiedosto järjestelmänvalvojan oikeuksin suoritettavasta komentokehotteesta, sillä se asettaa Windows-rekisteriavaimet, joita tarvitaan Office 2010:n määrittämiseksi toimimaan [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -ratkaisun kanssa.

Alla on tietoja ohjesyntaksista ja työkalun käyttöesimerkkejä.

```
C:\>Microsoft.AADRM.ServiceLocationRegScriptTool.exe /?
=
            Service Location Registry Script Generator
=
Microsoft.AADRM.ServiceLocationRegScriptTool.exe -r:<AADRM URL> -s:<STS Site ID> -u:<O365 Authentication System user name> -p:<User password>

   -r: The Uniform Resource Locator (URL) that is the base address for your Windows Azure Active Directory Rights Management (AADRM) server
   -s: The host name identifier for the Secure Token Service (STS) site
   -u: The O365 Authentication System user name, typically provided in e-mail format (for example, "user@contoso.com")
   -p: The password for the O365 Authentication System user.

---------
EXAMPLES
---------

-------------------------------EXAMPLE 1-------------------------------
C:\>Microsoft.AADRM.ServiceLocationRegScriptTool.exe

Description
-----------
Runs the Service Location Registry Script Generator tool using default settings and prompts you to enter credentials.

-------------------------------EXAMPLE 2-------------------------------
C:\>Microsoft.AADRM.ServiceLocationRegScriptTool.exe -r:https://AadrmUrl.com -s:StsName

Description
-----------
Runs the Service Location Registry Script Generator tool using non-default values and prompts you to enter credentials.

-------------------------------EXAMPLE 3-------------------------------
C:\>Microsoft.AADRM.ServiceLocationRegScriptTool.exe -r:https://AadrmUrl.com -s:StsName -u:user@contoso.com -p:password

Description
-----------
Runs the Service Location Registry Script Generator tool using non-default values.
```
> [!NOTE]
> Tätä työkalua suoritettaessa voi ilmetä virheitä, jos rekisteriavaimia ei löydy. Nämä virheet eivät vaikuta työkalun toimintaan, joten ne voi jättää huomiotta.

