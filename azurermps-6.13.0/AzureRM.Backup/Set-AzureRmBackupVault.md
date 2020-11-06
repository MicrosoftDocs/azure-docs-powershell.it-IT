---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511947"
---
# Set-AzureRmBackupVault

## Sinossi
Modifica il tipo di archiviazione di un caveau di backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmBackupVault** modifica il tipo di archiviazione di un Vault di backup di Azure.
Non è possibile modificare altre proprietà di un Vault.

## ESEMPI

### Esempio 1: cambiare lo spazio di archiviazione per un vault esistente
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

Questo comando ottiene il Vault di backup di Azure denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .
Il comando passa il Vault al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente modifica il tipo di archiviazione in LocallyRedundant.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Spazio di archiviazione
Specifica il tipo di archiviazione per i dati di backup.
I valori accettabili per questo parametro sono: LocallyRedundant e georidondanti.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Specifica un archivio di backup modificato da questo cmdlet.
Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Parameters: Vault (ByValue)

## OUTPUT

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault

## Note
* Quando si registra il primo server o una macchina virtuale per un Vault, il tipo di archiviazione è bloccato. In seguito, non è possibile modificare il tipo di archiviazione.

## COLLEGAMENTI CORRELATI

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)


