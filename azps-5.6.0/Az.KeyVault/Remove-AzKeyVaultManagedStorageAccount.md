---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952510"
---
# Remove-AzKeyVaultManagedStorageAccount

## SYNOPSIS
Rimuove un account di archiviazione di Azure gestito da Vault della chiave e tutte le definizioni di firma di accesso condiviso associate.

## SINTASSI

### ByDefinitionName (Impostazione predefinita)
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
L'associazione di un account di archiviazione di Azure al Vault chiave viene disassociata. In questo modo non viene rimosso un account di archiviazione di Azure, ma le chiavi dell'account non vengono gestite dal Vault delle chiavi di Azure. Vengono rimosse anche tutte le definizioni della firma di accesso condiviso gestito da Vault delle chiavi.

## ESEMPI

### Esempio 1: Rimuovere un account di archiviazione di Azure gestito dal Vault della chiave e tutte le definizioni di firma di accesso condiviso associate.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

L'associazione dell'account di archiviazione di Azure 'mystorageaccount' al Vault delle chiavi 'myvault' interrompe la gestione delle chiavi da parte di Vault. L'account 'mystorageaccount' non verrà rimosso. Tutte le definizioni della firma di accesso condiviso gestite da Vault chiave associate all'account verranno rimosse.

### Esempio 2: rimuovere un account di archiviazione di Azure gestito dal Vault della chiave e tutte le definizioni di firma di accesso condiviso associate senza conferma dell'utente.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

L'associazione dell'account di archiviazione di Azure 'mystorageaccount' al Vault delle chiavi 'myvault' interrompe la gestione delle chiavi da parte di Vault. L'account 'mystorageaccount' non verrà rimosso. Tutte le definizioni della firma di accesso condiviso gestite da Vault chiave associate all'account verranno rimosse.

### Esempio 3: Eliminare definitivamente (ripulire) un account di archiviazione di Azure gestito da Vault della chiave e tutte le definizioni di firma di accesso condiviso associate da un vault abilitato per l'eliminazione reverscita.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

L'esempio presuppone che l'eliminazione rescisa sia abilitata per il vault. Verificare se è questo il caso esaminando le proprietà del vault o l'attributo RecoveryLevel di un'entità nel vault.
Il primo cmdlet disassocia l'account di archiviazione di Azure 'mystorageaccount' dal Vault delle chiavi 'myvault' e impedisce a Vault delle chiavi di gestire le relative chiavi. L'account 'mystorageaccount' non verrà rimosso. Tutte le definizioni della firma di accesso condiviso gestite da Vault chiave associate all'account verranno rimosse.
Il secondo cmdlet verifica che l'account di archiviazione sia in stato eliminato, ma ripristinabile. Per raggiungere questo stato può essere necessario del tempo, consenti circa 30s prima di tentare.
Il terzo cmdlet rimuove definitivamente l'account di archiviazione: il ripristino non sarà più possibile.

## PARAMETERS

### -AccountName
Nome dell'account di archiviazione gestito dal Vault chiave. Il cmdlet crea l'FQDN di un account di archiviazione gestito dal nome del vault, dall'ambiente attualmente selezionato e dal nome dell'account di archiviazione gestito.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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
Non chiedere conferma.

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
Oggetto ManagedStorageAccount.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Rimuovere definitivamente l'account di archiviazione gestito eliminato in precedenza.

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

### -PassThru
Il cmdlet non restituisce un oggetto per impostazione predefinita.
Se si specifica questa opzione, il cmdlet restituisce l'account di archiviazione gestito eliminato.

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

### -VaultName
Nome del Vault.
Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
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

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount

## NOTE

## COLLEGAMENTI CORRELATI

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

