---
description: na
keywords: na
title: Comparing Azure Rights Management and AD RMS
search: na
ms.date: na
ms.service: rights-management
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8123bd62-1814-4d79-b306-e20c1a00e264
---
# Windows Azure AD Rights Management ja AD RMS
Arvioitaessa, onko [!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] oikea vaihtoehto, kun sisältö halutaan turvata omassa organisaatiossasi tai kun sisältöä jaetaan muissa organisaatioissa olevien luotettujen kumppanien kanssa, voi olla hyvä verrata [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelua Windows Server -ympäristössä toimineeseen edeltäjäänsä, joka oli Active Directory Rights Management Services (AD RMS). Seuraavassa taulukossa on verrattu rinnakkain [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelun ja AD RMS:n ominaisuuksia ja etuja.

|[!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)]|Active Directory Rights Management Services (AD RMS)|
|-----------------------------------------------------------------------------|--------------------------------------------------------|
|Tukee vain Microsoft Online Services -palveluja ja niihin liittyviä tuotteita, kuten Exchange Onlinea ja SharePoint Onlinea. Tällä hetkellä [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] ei tue perinteisiä paikallisia [!INCLUDE[Office](../Token/Office_md.md)]-palvelintuotteita, jollainen on esimerkiksi [!INCLUDE[ExchangeServer_1st](../Token/ExchangeServer_1st_md.md)].|Suunniteltu käytettäväksi lähinnä Microsoftin paikallisten palvelintuotteiden kanssa. Tällaisia tuotteita ovat Microsoft Office SharePoint Server ja [!INCLUDE[ExchangeServer](../Token/ExchangeServer_md.md)], SharePoint Online ja File Classification Infrastructure (FCI). AD RMS toimii kuitenkin Exchange Onlinen kanssa.|
|Ottaa käyttöön implisiittisen luottamuksen sellaisten organisaatioiden ja käyttäjien välillä, jotka ovat [!INCLUDE[o365_1](../Token/o365_1_md.md)] -asiakkaita. Sisältöä voi jakaa helposti ja turvallisesti käyttäjien välillä samassa organisaatiossa tai organisaatiorajojen yli, kun kyseessä on kelvollinen muun [!INCLUDE[o365_2](../Token/o365_2_md.md)] -vuokraajatilin käyttäjä.|Luottamus määritetään eksplisiittisesti kahden organisaation välisessä suorassa pisteestä pisteeseen -suhteessa käyttämällä joko luotettuja käyttäjätoimialueita tai Active Directory -liittoutumispalveluilla (AD FS) luotuja liittoutuneita luottamussuhteita.|
|Tarjoaa käyttöön ennalta määritettyjä oikeuskäytäntömalleja. Kyseessä on kaksi mallia, joista toinen tarjoaa vain luku -oikeuden suojattuun sisältöön ja toinen tarjoaa kirjoitus- tai muokkausoikeuden suojattuun sisältöön.|Tarjoaa mahdollisuuden luoda ja määrittää omia oikeuskäytäntömalleja. AD RMS -malleja voi määrittää yksityiskohtaisemmalla tasolla, kuten ohjeartikkelissa [AD RMS Policy Template Considerations (AD RMS -käytäntömalleihin liittyviä näkökohtia)](http://go.microsoft.com/fwlink/?LinkId=154765) on kuvattu.|
|Tukee Microsoft Office 2010- ja Microsoft Office 2013 -tuotteiden käyttäjiä.|Tukee Microsoft Office 2007:n sekä muiden Microsoft Office -tuotteiden, kuten Microsoft Office 2010:n ja Microsoft Office 2013:n, käyttäjiä.|
|Ei tue Windows XP -asiakkaita. Tukee asiakkaita, joiden käytössä on Windows Vista, Windows 7 tai Windows 8.|Tukee asiakkaita, joiden käytössä on Windows XP tai uudempi versio, kuten Windows Vista, Windows 7 tai Windows 8.|
|Tukee vain salaustilaa 2. Lisätietoja: [AD RMS Cryptographic Modes (AD RMS:n salaustilat)](http://go.microsoft.com/fwlink/?LinkId=266659)|Tukee salaustilaa 1 ja salaustilaa 2. Lisätietoja: [AD RMS Cryptographic Modes (AD RMS:n salaustilat)](http://go.microsoft.com/fwlink/?LinkId=266659).|
|Tukee siirtymistä vain [!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] -palvelusta Active Directory -oikeuksien hallintapalveluihin (AD RMS).|Tukee siirtymistä [!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] -palvelusta ja Active Directory -oikeuksien hallintapalveluista (AD RMS), jotka ovat käytössä Windows Server 2003 -ympäristössä.|
