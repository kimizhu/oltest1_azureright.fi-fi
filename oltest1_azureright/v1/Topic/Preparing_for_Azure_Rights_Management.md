---
description: na
keywords: na
title: Preparing for Azure Rights Management
search: na
ms.date: na
ms.service: rights-management
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: afbca2d6-32a7-4bda-8aaf-9f93f5da5abc
---
# Oikeuksien hallinnan valmisteleminen
Kun olet rekisteröitynyt ja määrittänyt organisaatiolle tilin [!INCLUDE[o365_1](../Token/o365_1_md.md)] -palvelussa, [!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] -käyttöönottoon tarvitaan vain muutama lisämääritys.

> [!TIP]
> Ennen kuin kokeilet [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelua, määritä käyttäjätilit joko Microsoft Online -hallintakonsolissa tai Exchange Online -ohjuspaneelissa. Kannattaa myös etukäteen luoda sähköpostioikeuksilla varustettuja käyttöoikeusryhmiä Exchange Onlinessa. Lisätietoja on Microsoftin tukisivuston ohjeartikkelissa [How to manage Active Directory security groups and to mail-enable group objects in an Office 365 environment (Active Directory -käyttöoikeusryhmien hallinta ja sähköpostioikeuksien myöntäminen ryhmäobjekteille Office 365 -ympäristössä)](http://support.microsoft.com/?kbid=2588125) (http://support.microsoft.com/?kbid=2588125).

## Oikeuksien hallinnan käyttöönotto
[!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] on oletusarvoisesti pois käytöstä, kun rekisteröidyt [!INCLUDE[o365_2](../Token/o365_2_md.md)] -tiliä varten [!INCLUDE[o365_w15_ent3_1](../Token/o365_w15_ent3_1_md.md)] -palvelussa. Jotta [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] voidaan ottaa käyttöön, [!INCLUDE[o365_2](../Token/o365_2_md.md)] -järjestelmänvalvojan täytyy ensin muodostaa yhteys [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palveluun ja ottaa se käyttöön Windows PowerShellin [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -hallintamoduulissa ja [!INCLUDE[o365_2](../Token/o365_2_md.md)] -hallintaportaalissa.

> [!IMPORTANT]
> Ennen kuin yrität siirtyä käyttämään [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelua tai suojaamaan ja käyttämään sisältöä tai määrittämään tukisovelluksia, kannattaa tarkistaa vielä kerran, että ohjeaiheessa [Windows PowerShellin asentaminen oikeuksien hallintaa varten](../Topic/Installing_Windows_PowerShell_for_Azure_Rights_Management.md) määritetyt asennus- ja määritystoimet on tehty.

