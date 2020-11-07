---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687954"
---
# Get-AzureRmBackupVault

## Sinossi
Ottiene i Vault di backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmBackupVault** ottiene i Vault di backup di Azure.
Questo cmdlet restituisce gli oggetti **AzureRmBackupVault** da usare con altri cmdlet.

## ESEMPI

### Esempio 1: visualizzare tutti i Vault di backup
```
PS C:\>Get-AzureRmBackupVault
```

Questo comando consente di ottenere tutte le volte di backup di Azure.

### Esempio 2: visualizzare tutti i Vault creati in West US
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

Questo comando recupera tutti i caveau di backup.
Il comando li passa al cmdlet Where-Object usando l'operatore pipeline.
Questo cmdlet filtra i risultati in base alla proprietà **Region** .
Per altre informazioni, digitare `Get-Help Where-Object` .

### Esempio 3: ottenere un Vault specifico
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Questo comando ottiene il Vault denominato Vault03.

### Esempio 4: contare il numero di volte con spazio di archiviazione locale ridondante
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

Questo comando consente di ottenere tutte le volte di backup di Azure.
Il comando li passa a **Where-Object** , che filtra i risultati in base alla proprietà di **archiviazione** .
Il comando passa quelli che hanno un valore di LocallyRedundant al cmdlet Measure-Object, che conteggia i risultati.
Per altre informazioni, digitare `Get-Help Measure-Object` .

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'archivio di backup ottenuto da questo cmdlet.
Se più di un Vault di backup ha lo stesso nome, questo cmdlet li restituirà tutti.
Specifica il parametro *ResourceGroupName* per ottenere un Vault univoco.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse Azure in cui questo cmdlet ottiene un caveau di backup.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### AzureRmBackupVault

## Note
* Nessuno

## COLLEGAMENTI CORRELATI

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


