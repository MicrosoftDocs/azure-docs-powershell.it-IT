---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865198"
---
# Backup-AzKeyVaultManagedStorageAccount

## Sinossi
Eseguire il backup di un account di archiviazione gestito con il Vault.

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

## Descrizione
Il cmdlet **backup-AzKeyVaultManagedStorageAccount** consente di eseguire il backup di un account di archiviazione gestita specificato in un Vault chiave, scaricarlo e archiviarlo in un file.
Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.
È possibile ripristinare un account di archiviazione di cui è stato eseguito il backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup, purché il Vault si trovi nella stessa geografia di Azure.
I motivi tipici per usare questo cmdlet sono i seguenti: 
- Si vuole mantenere una copia offline dell'account di archiviazione se si elimina accidentalmente l'originale dall'archivio.
 
- È stato creato un account di archiviazione gestita con Key Vault e ora si vuole clonare l'oggetto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita.
Usa il cmdlet **backup-AzKeyVaultManagedStorageAccount** per recuperare l'account di archiviazione gestita in formato crittografato e quindi usa il cmdlet **Restore-AzKeyVaultManagedStorageAccount** e specifica un Vault chiave nella seconda area.

## ESEMPI

### Esempio 1: eseguire il backup di un account di archiviazione gestita con un nome file generato automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Questo comando Recupera l'account di archiviazione gestita denominato MyMSAK dal Vault chiave denominato MyKeyVault e salva una copia di backup dell'account di archiviazione gestita in un file denominato automaticamente e visualizza il nome del file.

### Esempio 2: eseguire il backup di un account di archiviazione gestita in un nome file specificato
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Questo comando Recupera l'account di archiviazione gestita denominato MyMSAK dal Vault chiave denominato MyKeyVault e salva una copia di backup dell'account di archiviazione gestita in un file denominato backup. blob.

### Esempio 3: eseguire il backup di un account di archiviazione gestita precedentemente recuperato in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Questo comando crea una copia di backup dell'account di archiviazione gestita denominato $msak. Nome nel Vault denominato $msak. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.

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

### -Force
Sovrascrivere il file assegnato se esiste

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
Bundle account di archiviazione di cui eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.

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

### -Nome
Nome segreto.
Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.

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
Se non specificato, verrà generato un nome file predefinito.

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

### -VAULTNAME
Nome del Vault.
Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.

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

### System. String

## Note

## COLLEGAMENTI CORRELATI
