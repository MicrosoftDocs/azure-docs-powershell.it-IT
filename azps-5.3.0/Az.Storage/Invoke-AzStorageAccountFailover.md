---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376221"
---
# Invoke-AzStorageAccountFailover

## Sinossi
Richiama il failover di un account di archiviazione.

## SINTASSI

### AccountName (impostazione predefinita)
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Richiama il failover di un account di archiviazione. La richiesta di failover può essere attivata per un account di archiviazione in caso di problemi di disponibilità. Il failover viene eseguito dal cluster primario dell'account di archiviazione al cluster secondario per gli account RA-GRS. Il cluster secondario diventerà primario dopo il failover.
Tenere presente l'impatto seguente sull'account di archiviazione prima di avviare il failover: 1,1. Verificare l'ultima volta che si usa la casella di controllo Ottieni statistiche servizio BLOB (Ottieni statistiche servizio https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) tabelle https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) e ottieni statistiche Servizio Code ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) per il tuo account. Questi sono i dati che potrebbero essere persi se si avvia il failover.
2. dopo il failover, il tipo di account di archiviazione verrà convertito in spazio di archiviazione ridondante locale (LRS). Puoi convertire l'account in uso di archiviazione Geo-ridondante (GRS).
3. dopo avere riabilitato GRS per l'account di archiviazione, Microsoft eseguirà la replica dei dati nella nuova area secondaria. Il tempo di replica dipende dalla quantità di dati da replicare. Tieni presente che ci sono costi di larghezza di banda per il bootstrap. https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## ESEMPI

### Esempio 1: richiamare il failover di un account di archiviazione
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

Questo comando controlla l'ultima ora di sincronizzazione di un account di archiviazione e ne richiama il failover, mentre il cluster secondario diventa primario dopo il failover. Poiché il failover richiede molto tempo, è consigliabile eseguirlo nel parametro backend with-AsJob e quindi attendere il completamento del processo.

## PARAMETRI

### -AsJob
Esegui cmdlet in background

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forzare il failover dell'account

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oggetto account di archiviazione

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome dell'account di archiviazione.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount

## Note

## COLLEGAMENTI CORRELATI
