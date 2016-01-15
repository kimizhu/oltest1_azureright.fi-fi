---
description: na
keywords: na
title: Administering Azure Rights Management by Using Windows PowerShell
search: na
ms.date: na
ms.service: rights-management
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a890e04a-4b70-41b5-8d5f-3c210a669faa
---
# Oikeuksien hallinta Windows PowerShellin avulla
[!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] voidaan asettaa palveltavan [!INCLUDE[o365_1](../Token/o365_1_md.md)] -tilisi käyttöön aktivoimalla oikeuksien hallinta [!INCLUDE[o365_2](../Token/o365_2_md.md)] -hallintakeskuksessa. Voit myös ladata Windows PowerShellin [!INCLUDE[aad_rightsmanagement_1](../Token/aad_rightsmanagement_1_md.md)] -moduulin, jolla voidaan valmistella [!INCLUDE[o365_2](../Token/o365_2_md.md)] -vuokraaja ja suorittaa muita [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -hallintatoimia.

Kun [Windows PowerShellin asentaminen oikeuksien hallintaa varten](../Topic/Installing_Windows_PowerShell_for_Azure_Rights_Management.md) on suoritettu ja [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] on otettu käyttöön (joko [!INCLUDE[o365_2](../Token/o365_2_md.md)] -portaalin toiminnolla tai PowerShell-hallintatoimella), muita hallintatoimia ei oletusarvoisesti ehkä enää tarvita. Joissakin vaativammissa käyttötilanteissa saatetaan kuitenkin tarvita ominaisuuksia, jotka saadaan käyttöön vain yhdessä [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelun ja Windows PowerShell -työkalujen kanssa. Seuraava taulukko auttaa selvittämään, soveltuuko jokin näistä tehtävätyypeistä omiin tarpeisiisi. Taulukossa on myös mainittu Windows PowerShellin cmdlet-komennot, joista on hyvä olla tietoinen, jos olet kiinnostunut kyseisistä [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -ominaisuuksista.

|Jos haluat tehdä tämän toiminnon…|…käytä seuraavia cmdlet-komentoja|
|-------------------------------------|-------------------------------------|
|Yhteyden muodostaminen [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palveluun tai yhteyden katkaiseminen.|**Connect-AadrmService**<br />**Disconnect-AadrmService**<br />Lisätietoja: [Connecting to the Azure Rights Management Service](http://msdn.microsoft.com/en-us/library/6966d848-9fa2-41fe-a1da-7e3ab935ce39) ja [Disconnecting from the Azure Rights Management Service](http://msdn.microsoft.com/en-us/library/6d78bdb9-068e-4136-ab34-9ddbf00c6c5f)|
|[!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -palvelun poistaminen käytöstä (tai palauttaminen käyttöön käytöstä poiston jälkeen).|**Enable-Aadrm**<br />**Disable-Aadrm**<br />Lisätietoja: [Enabling the Azure Rights Management Service](http://msdn.microsoft.com/en-us/library/4d4fa296-2fce-467c-8b83-89d243808741) ja [Disabling the Azure Rights Management Service](http://msdn.microsoft.com/en-us/library/2f95ba8a-9865-4698-90dd-bcd218d8a7e5)|
|Tehokäyttäjien hallinta [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -asennuksessa.|**Enable–AadrmSuperUserFeature**<br />**Add–AadrmSuperUser**<br />**Get–AadrmSuperUser**<br />**Remove–AadrmSuperUser**<br />Lisätietoja: [Managing Super Users for Azure Rights Managed Content](http://msdn.microsoft.com/en-us/library/42eeda9a-b38c-47eb-b4da-1128e7fcdb8e)|
|[!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -asennukseen valtuutettujen käyttäjien ja ryhmien hallinta.|**Add–AadrmRoleBasedAdministrator**<br />**Get–AadrmRoleBasedAdministrator**<br />**Remove–AadrmRoleBasedAdministrator** <br />Lisätietoja: [Adding, Listing, or Removing Role-based Administrators for Azure Rights Management](http://msdn.microsoft.com/en-us/library/ba956cb9-b7de-487f-b8d8-99143302ae6b)|
|[!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -asennukseen liittyvien hallintatehtävien lokin saaminen.|**Get-AadrmAdminLog**<br />Lisätietoja: [Downloading Audit Logs for Azure Rights Management](http://msdn.microsoft.com/en-us/library/236a5996-9ebd-4c6c-bae1-80b073f96a07)|
|Siirtyminen paikalliseen AD RMS -käyttöönottoon [!INCLUDE[aad_rightsmanagement_2](../Token/aad_rightsmanagement_2_md.md)] -asennuksesta.|**Set-AadrmMigrationUrl**<br />**Get–AadrmMigrationUrl**<br />Lisätietoja: [Listing or Setting the URL for Use in Migrating Azure Rights Managed Content to AD RMS](http://msdn.microsoft.com/en-us/library/20c0848a-872e-45f2-abed-69933345aab2)|
