---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 8c90137e142086d7ea7c0bcc34321b3f38a12d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511939"
---
# Unregister-AzureRmBackupContainer

## Sinossi
Annulla la registrazione di un contenitore da un caveau di backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Unregister-AzureRmBackupContainer** Annulla la registrazione della macchina virtuale Windows Server o Azure da un Vault di backup di Azure.
Questo cmdlet consente di rimuovere i riferimenti a un contenitore dall'archivio di backup.
Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.

## ESEMPI

### Esempio 1: annullare la registrazione di un server Windows
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.
Il comando Archivia l'oggetto nella variabile $Vault.
Il secondo comando ottiene un contenitore con il nome specificato nel Vault in $Vault usando il cmdlet Get-AzureRmBackupContainer.
Il comando Archivia l'oggetto nella variabile $Container.
Il comando finale annulla la registrazione del server Windows specificato dall'archivio di backup di Azure.

### Esempio 2: annullare la registrazione di un server Windows senza conferma
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

Questo comando Annulla la registrazione del server Windows specificato dall'archivio di backup di Azure, così come nel primo esempio.
Questo comando specifica il parametro *Force* .
Di conseguenza, il comando non chiede conferma.

## PARAMETRI

### -Contenitore
Specifica la macchina virtuale Windows Server o Azure che il cmdlet Annulla la registrazione.
Per ottenere un **AzureRmBackupContainer** , usare il cmdlet Get-AzureRmBackupContainer.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.
Questo parametro è pertinente solo per gli oggetti **AzureBackupContainer** di tipo Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer
Parameters: container (ByValue)

## OUTPUT

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob

## Note
* Nessuno

## COLLEGAMENTI CORRELATI

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Registro-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


