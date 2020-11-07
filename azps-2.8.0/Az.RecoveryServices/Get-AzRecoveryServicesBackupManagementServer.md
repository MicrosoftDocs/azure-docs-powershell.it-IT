---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 341b222c8b5e85a4b5f5221c34d6f45cd2993c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855726"
---
# Get-AzRecoveryServicesBackupManagementServer

## Sinossi
Ottiene i server di gestione di SCDPM e Azure Backup.

## SINTASSI

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzRecoveryServicesBackupManagementServer** ottiene un elenco dei server di gestione di backup registrati in un Vault.
Esistono due tipi di server di gestione del backup: System Center Data Protection Manager (SCDPM) e Azure Backup Management Servers.
I server di gestione backup vengono installati separatamente per gestire l'orchestrazione di backup.
Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.

## ESEMPI

### Esempio 1: ottenere tutti i server di gestione del backup
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

Questo comando consente di ottenere tutti i server di gestione del backup registrati con il Vault.

## PARAMETRI

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

### -Nome
Specifica il nome del server di gestione del backup da ottenere.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
ID ARM dell'archivio servizi di ripristino.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase

## Note

## COLLEGAMENTI CORRELATI

[Annullamento della registrazione-AzRecoveryServicesBackupManagementServer](./Unregister-AzRecoveryServicesBackupManagementServer.md)


