---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863054"
---
# Add-AzKeyVaultManagedStorageAccount

## Sinossi
Aggiunge un account di archiviazione di Azure esistente al Vault Key specificato in modo che le chiavi vengano gestite dal servizio Key Vault.

## SINTASSI

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Configura un account di archiviazione di Azure esistente con Key Vault per i tasti dell'account di archiviazione da gestire tramite Key Vault. L'account di archiviazione deve già esistere. Le chiavi di archiviazione non vengono mai esposte al chiamante.
Key Vault auto rigenera e commuta la chiave attiva in base al periodo di rigenerazione.

## ESEMPI

### Esempio 1: impostare un account di archiviazione di Azure con il Vault chiave per gestire le chiavi
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

Imposta un account di archiviazione con Key Vault per consentire la gestione delle chiavi tramite Key Vault. Il set di tasti attivi è "Key1". Questa chiave verrà usata per generare i token SAS. Key Vault rigenererà la chiave "key2" dopo il periodo di rigenerazione dall'ora di questo comando e la imposterà come chiave attiva. Questo processo di rigenerazione automatica continuerà tra "Key1" e "key2" con una lacuna di 90 giorni.

### Esempio 2: impostare un account di archiviazione di Azure classico con il Vault chiave per gestire le chiavi
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

Imposta un account di archiviazione classico con Key Vault per consentire la gestione delle chiavi tramite Key Vault. Il set di tasti attivi è "Primary". Questa chiave verrà usata per generare i token SAS. Key Vault rigenererà il codice "secondario" dopo il periodo di rigenerazione dall'ora di questo comando e lo imposterà come chiave attiva. Questo processo di rigenerazione automatica continuerà tra "primario" e "secondario" con una lacuna di 90 giorni.

## PARAMETRI

### -AccountName
Nome dell'account di archiviazione gestito Key Vault. Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AccountResourceId
ID risorsa Azure dell'account di archiviazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveKeyName
Nome della chiave dell'account di archiviazione che deve essere usata per la generazione di token SAS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Disabilita l'uso della chiave dell'account di archiviazione gestita per la generazione di token SAS.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableAutoRegenerateKey
Chiave di rigenerazione automatica. Se true, la chiave inattiva dell'account di archiviazione gestita viene rigenerata automaticamente e diventa la nuova chiave attiva dopo il periodo di rigenerazione. Se false, le chiavi dell'account di archiviazione gestita non vengono rigenerate automaticamente.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegenerationPeriod
Periodo di rigenerazione. Se la chiave di rigenerazione automatica è abilitata, questo valore specifica l'intervallo di valori TimeSpan dopo il quale il tasto inattivo dell'account di archiviazione gestito viene rigenerato automaticamente e diventa la nuova chiave attiva.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Coppie chiave-valore in forma di tabella hash. Per esempio:

@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VAULTNAME
Nome del Vault.
Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount

## Note

## COLLEGAMENTI CORRELATI

[AZ. Vault](/powershell/module/Az.keyvault)
