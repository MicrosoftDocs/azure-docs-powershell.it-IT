---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029814"
---
# Get-AzureEnvironment

## Sinossi
Ottiene gli ambienti Azure

## SINTASSI

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureEnvironment** ottiene gli ambienti Azure disponibili per Windows PowerShell.

Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.
Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.
Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

Il cmdlet **Get-AzureEnvironment** ottiene gli ambienti dal file di dati dell'abbonamento, non da Azure.
Se il file di dati dell'abbonamento non è aggiornato, eseguire il cmdlet **Add-AzureAccount** o **Import-PublishSettingsFile** per aggiornarlo.

Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

## ESEMPI

### Esempio 1: ottenere tutti gli ambienti
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

Questo comando consente di ottenere tutti gli ambienti disponibili per Windows PowerShell.

### Esempio 2: ottenere un ambiente per nome
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

Questo esempio restituisce l'ambiente AzureCloud.

### Esempio 3: ottenere tutte le proprietà di tutti gli ambienti
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

Questo comando consente di ottenere tutte le proprietà di tutti gli ambienti.

Il comando usa il cmdlet **Get-AzureEnvironment** per ottenere tutti gli ambienti Azure per l'account.
USA quindi il cmdlet **foreach-Object** per eseguire un comando **Get-AzureEnvironment** con il parametro **Name** in ogni ambiente.
Il valore del parametro **Name** è la proprietà **EnvironmentName** di ogni ambiente.

Senza parametri, **Get-AzureEnvironment** ottiene solo le proprietà selezionate di un ambiente.

## PARAMETRI

### -Nome
Ottiene solo l'ambiente specificato.
Digitare il nome dell'ambiente.
Il valore del parametro fa distinzione tra maiuscole e minuscole.
I caratteri jolly non sono consentiti.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.

## OUTPUT

### System. Management. Automation. PSCustomObject
Per impostazione predefinita, **Get-AzureEnvironment** restituisce un oggetto personalizzato.

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment
Quando si esegue **Get-AzureEnvironment** con il parametro **Name** , viene restituito un oggetto  **WindowsAzureEnvironment** .

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureAccount](./Add-AzureAccount.md)

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


