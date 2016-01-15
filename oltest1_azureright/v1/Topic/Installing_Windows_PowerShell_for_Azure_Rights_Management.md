---
description: na
keywords: na
title: Installing Windows PowerShell for Azure Rights Management
search: na
ms.date: na
ms.service: rights-management
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0d665ed6-b1de-4d63-854a-bc57c1c49844
---
# Windows PowerShellin asentaminen oikeuksien hallintaa varten
[!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] -palvelua voidaan hallita Windows PowerShellin avulla kaikissa seuraavat vaatimukset täyttävissä järjestelmissä:

-   Windows Vista, Windows 7, Windows Server 2008 R2

    > [!NOTE]
    > Mitä tulee Windows Server 2008 R2 -järjestelmään, vain x64-ympäristöä tuetaan alkuperäistilassa. WOW64, joka mahdollistaa 32-bittisen emuloinnin 64-bittisissä ympäristöissä, ei ole tuettu.

-   Windows PowerShell 2.0

-   Microsoft Online Services Sign-In Assistant 7.0

> [!NOTE]
> Microsoft Online Services Sign-In Assistant täytyy asentaa [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -todennusta varten. Lisätietoja: [Download Center: Microsoft Online Services -palveluiden kirjautumisavustaja IT-asiantuntijoille RTW](http://www.microsoft.com/download/en/details.aspx?displaylang=en&amp;id=28177).

## Rights Management -hallintamoduulin käytön aloittaminen
Jotta voit aloittaa [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -käyttöönoton vuokraajatilissäsi, tee ensin joitakin kokoonpanomuutoksia.

> [!NOTE]
> Seuraavat toimet edellyttävät, että ensin asennetaan Microsoft .NET Framework 4.0. Lisätietoja: [http://www.microsoft.com/net/](http://www.microsoft.com/net/).

#### Rights Management -hallintamoduulin asentaminen ja määrittäminen

1.  Lataa [!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] -palvelun Windows PowerShell -hallintamoduuli Download Centeristä.

    [Windows PowerShellin Rights Management -moduulin lataaminen](http://go.microsoft.com/fwlink/?LinkId=257721)

2.  Kaksoisnapsauta paikallisessa kansiossa, johon latasit ja tallensit [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -asennusohjelmatiedoston, WindowsAzureADRightsManagementAdministration.exe-tiedostoa. [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -hallintamoduulin asennus käynnistyy.

3.  Avaa %WINDIR%\System32\WindowsPowerShell\v1.0-kansio ja varmista, että Powershell.exe.config-tiedosto sisältää seuraavat XML-tiedot:

    ```
    <?xml version="1.0"?> 
    <configuration> 
        <startup useLegacyV2RuntimeActivationPolicy="true"> 
            <supportedRuntime version="v4.0.30319"/> 
            <supportedRuntime version="v2.0.50727"/> 
        </startup> 
    </configuration>
    ```

4.  Avaa järjestelmänvalvojan oikeuksin suoritettava Windows PowerShell -komentokehote ja kirjoita seuraavat komennot moduulin tuomiseksi ja yhdistämiseksi [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -asennukseen:

    ```
    Import-Module AADRM
    Connect-AadrmService -Verbose
    ```
    Sinulta pyydetään tunnistetietoja.

5.  Anna tunnistetiedot sellaiselta [!INCLUDE[o365_2](../Token/o365_2_md.md)] -käyttäjältä, jolla on organisaatiossa yleisen järjestelmänvalvojan oikeudet, ja odota todentamista.

    > [!NOTE]
    > Yleisillä järjestelmänvalvojilla on oletusarvoisesti [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -hallintaoikeudet.

    Kirjoita järjestelmänvalvojan oikeuksin suoritettavaan Windows PowerShell -kehoteikkunaan seuraava komento, joka ottaa [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelun käyttöön vuokraajatilissäsi.

    ```
    Enable-Aadrm
    Disconnect-AadrmService
    ```
    > [!IMPORTANT]
    > [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelu on oletusarvoisesti pois käytöstä, kun se on valmisteltu uuteen vuokraajatiliin. [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -ominaisuudet eivät ole vuokraajakäyttäjien käytettävissä, ennen kuin palvelu otetaan käyttöön tässä vaiheessa.

    Kun nämä toimet on tehty, vuokraajan pitäisi olla käytössä.

