---
description: na
keywords: na
title: Azure Rights Management Deployment Roadmap
search: na
ms.date: na
ms.service: rights-management
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 086600c2-c5d8-47ec-a4c0-c782e1797486
---
# Oikeuksien hallinnan k&#228;ytt&#246;&#246;notto
Seuraavilla toimilla voit valmistella ja toteuttaa oikeuksien hallinnan sekä hallita sitä organisaatiossasi:

## Vaihe 1: Määritä Office 365 -tili
Jos olet jo saanut kutsun määrittää organisaatiollesi [!INCLUDE[o365_1](../Token/o365_1_md.md)] -tili ja olet jo suorittanut rekisteröinnin, olet melkein valmis aloittamaan. Jos kokeiltavat toiminnot eivät edellytä erikoisjärjestelyjä, tarvitaan vain muutama lisätoimi, jotta [!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] -palvelu voidaan määrittää ja ottaa käyttöön.

## Vaihe 2: Valmistele vuokraajatili Rights Management -käyttöä varten
Ennen kuin alat käyttää [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelua, Office 365 -tili on valmisteltava. Tähän liittyy tarvittavien ryhmien luominen [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelun hallintaa ja käyttöönottoa varten. Se tarkoittaa myös sitä, että [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelua varten on asennettava Windows PowerShell -moduuli, jotta [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelun yhdistämiseen ja käyttöönottoon voidaan tehdä muutoksia. Lisätietoja: [Windows PowerShellin asentaminen oikeuksien hallintaa varten](../Topic/Installing_Windows_PowerShell_for_Azure_Rights_Management.md) ja [Oikeuksien hallinnan valmisteleminen](../Topic/Preparing_for_Azure_Rights_Management.md).

## Vaihe 3: Määritä sovellukset
Sovellusten määrittämiseen voi liittyä Office-sovellusten määrittäminen asiakastietokoneisiin sekä sisältöoikeuksien hallinnan (IRM) ominaisuuksien määrittäminen ja käyttöönotto SharePoint Onlinessa tai Exchange Onlinessa.

Lisätietoja on seuraavissa ohjeaiheissa: [Oikeuksien hallinnan Office-integrointi](../Topic/Configuring_Applications_for_Azure_Rights_Management.md), [Enabling IRM Services in SharePoint Online](http://msdn.microsoft.com/en-us/library/45e4b980-9902-49f9-ac2a-5d3274a2725b) ja [Enabling IRM Services with Exchange Online](http://msdn.microsoft.com/en-us/library/14d9442e-cc3c-4ac5-b490-1acce154eb0f).

## Vaihe 4: Julkaise oikeuksilla suojattu sisältö ja käytä sitä
Kun [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] on otettu käyttöön asiakastietokoneissa ja Office 365 -sovelluksissa, voit aloittaa sen käytön suojatun sisällön julkaisemisessa ja käyttämisessä. Lisätietoja: [Oikeuksien hallinnan käyttäminen](../Topic/Using_Azure_Rights_Management.md).

## Vaihe 5: Hallinnoi oikeuksien hallintapalvelua vuokraajatililläsi tarpeen mukaan
Kun alat käyttää [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelua, haluat ehkä toisinaan tehdä hallintapalveluun lisämuutoksia Windows PowerShellin [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -moduulin avulla. Lisätietoja: [Oikeuksien hallinta Windows PowerShellin avulla](../Topic/Administering_Azure_Rights_Management_by_Using_Windows_PowerShell.md).

