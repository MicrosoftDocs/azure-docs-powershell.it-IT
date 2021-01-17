---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333007"
---
# Remove-AzKeyVaultManagedStorageAccount

## Sinossi
Consente di rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.

## SINTASSI

### ByDefinitionName (impostazione predefinita)
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

## Descrizione
Dissocia un account di archiviazione di Azure da Key Vault. In questo modo non viene rimosso un account di archiviazione di Azure, ma i tasti account vengono rimossi dall'archivio chiavi di Azure. Vengono rimosse anche tutte le definizioni di archiviazione gestite di Key Vault associate.

## ESEMPI

### Esempio 1: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate.
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

Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi. L'account "mystorageaccount" non verrà rimosso. Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.

### Esempio 2: rimuovere un account di archiviazione di Azure Key Vault gestito e tutte le definizioni SAS associate senza la conferma dell'utente.
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

Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault Key "Vault" e interrompe la gestione delle chiavi. L'account "mystorageaccount" non verrà rimosso. Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.

### Esempio 3: Elimina definitivamente (Purge) un account di archiviazione di Azure con chiave archiviata Key e tutte le definizioni SAS associate da un Vault abilitato per l'eliminazione soft.
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

L'esempio presuppone che l'eliminazione morbida sia abilitata per il Vault. Verificare se questo è il caso esaminando le proprietà del Vault o l'attributo RecoveryLevel di un'entità nel Vault.
Il primo cmdlet Annulla l'associazione dell'account di archiviazione di Azure "mystorageaccount" dal Vault chiave "Vault" e interrompe la gestione delle chiavi. L'account "mystorageaccount" non verrà rimosso. Verranno rimosse tutte le definizioni SAS di archiviazione gestite di Key Vault associate a questo account.
Il secondo cmdlet verifica che l'account di archiviazione si trovi in uno stato eliminato, ma ripristinabile. Il raggiungimento di questo stato può richiedere un po' di tempo, attendere 30 anni prima di tentare.
Il terzo cmdlet rimuove definitivamente l'account di archiviazione-il ripristino non sarà più possibile.

## PARAMETRI

### -AccountName
Nome dell'account di archiviazione gestito Key Vault. Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.

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
Rimuovere definitivamente l'account di archiviazione gestita precedentemente eliminata.

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
Cmdlet non restituisce un oggetto per impostazione predefinita.
Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.

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

### -VAULTNAME
Nome del Vault.
Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem

## OUTPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount

## Note

## COLLEGAMENTI CORRELATI

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

