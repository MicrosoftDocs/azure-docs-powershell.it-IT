---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 75f5e487c7cb1d434d12d6c02122991195c01066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991142"
---
# Backup-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Backup di un account di archiviazione gestito da KeyVault.

## SINTASSI

### ByStorageAccountName (impostazione predefinita)
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Backup-AzKeyVaultManagedStorageAccount** consente di eseguire il backup di un account di archiviazione gestito specificato in un vault delle chiavi scaricarlo e archiviarlo in un file.
Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno del Vault delle chiavi di Azure.
È possibile ripristinare un account di archiviazione di cui è stato eseguito il backup in qualsiasi vault chiave nell'abbonamento da cui è stato eseguito il backup, purché il vault si trova nella stessa area geografica di Azure.
I motivi tipici per usare questo cmdlet sono: 
- Si vuole conservare una copia offline dell'account di archiviazione nel caso in cui si elimini accidentalmente l'originale dal Vault.
 
- È stato creato un account di archiviazione gestito con il Vault delle chiavi e ora si vuole clonare l'oggetto in un'area di Azure diversa, in modo da poterlo usare da tutte le istanze dell'applicazione distribuita.
Usare il cmdlet **Backup-AzKeyVaultManagedStorageAccount** per recuperare l'account di archiviazione gestito in formato crittografato e quindi usare il cmdlet **Restore-AzKeyVaultManagedStorageAccount** e specificare un vault delle chiavi nella seconda area geografica.

## ESEMPI

### Esempio 1: Eseguire il backup di un account di archiviazione gestito con un nome file generato automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Questo comando recupera l'account di archiviazione gestito denominato MyMSAK dalla chiave vault denominata MyKeyVault e salva una copia di backup dell'account di archiviazione gestito in un file denominato automaticamente e visualizza il nome del file.

### Esempio 2: Eseguire il backup di un account di archiviazione gestito con un nome file specificato
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Questo comando recupera l'account di archiviazione gestito denominato MyMSAK dalla chiave vault denominata MyKeyVault e salva un backup dell'account di archiviazione gestito in un file denominato Backup.BLOB.

### Esempio 3: Eseguire il backup di un account di archiviazione gestito recuperato in precedenza con un nome file specificato, sovrascrivendo il file di destinazione senza chiedere conferma.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Questo comando crea un backup dell'account di archiviazione gestito denominato $msak. Nome nel vault denominato $msak. VaultName in un file denominato Backup.BLOB, sovrascrivendo automaticamente il file, se esiste già.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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
Sovrascrivere il file specificato, se esistente

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
Bundle di account di archiviazione di cui eseguire il backup, pipelined in seguito all'output di una chiamata di recupero.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome segreto.
Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato e il nome del segreto.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
File di output.
Il file di output per archiviare il backup dell'account di archiviazione.
Se non viene specificato, verrà generato un nome file predefinito.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Nome del Vault.
Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem

## OUTPUT

### System.String

## NOTE

## COLLEGAMENTI CORRELATI
