---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: d5fce3a4c70593b9478c0efa8afef29021797bb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861326"
---
# Backup-AzKeyVaultKey

## Sinossi
Eseguire il backup di una chiave in un Vault chiave.

## SINTASSI

### ByKeyName (impostazione predefinita)
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **backup-AzKeyVaultKey** consente di eseguire il download di una chiave specificata in un Vault chiave e di archiviarla in un file.
Se sono presenti più versioni della chiave, tutte le versioni verranno incluse nel backup.
Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.
È possibile ripristinare una chiave di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.

I motivi tipici per usare questo cmdlet sono i seguenti: 

- Si vuole depositare una copia della chiave, in modo da avere una copia offline nel caso in cui si elimini accidentalmente la chiave in un caveau chiave.
 
- È stata creata una chiave con Key Vault e ora si vuole clonare la chiave in un'altra area di Azure, in modo da poterla usare in tutte le istanze dell'applicazione distribuita.
Usa il cmdlet **backup-AzKeyVaultKey** per recuperare la chiave in formato crittografato e quindi usa il cmdlet Restore-AzKeyVaultKey e specifica un Vault chiave nella seconda area geografica.

## ESEMPI

### Esempio 1: eseguire il backup di una chiave con un nome file generato automaticamente
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

Questo comando Recupera la chiave denominata MyKey dal Vault chiave denominata MyKeyVault e salva una copia di backup di tale chiave in un file denominato automaticamente e visualizza il nome del file.

### Esempio 2: eseguire il backup di una chiave in un nome file specificato
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

Questo comando Recupera la chiave denominata MyKey dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale chiave in un file denominato backup. blob.

### Esempio 3: eseguire il backup di una chiave recuperata in precedenza in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.
```
PS C:\>$key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

Questo comando crea una copia di backup della chiave denominata $key. Nome nel Vault denominato $key. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.

## PARAMETRI

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

### -Force
Sovrascrivere il file assegnato se esiste

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Key
Specifica una chiave recuperata in precedenza di cui eseguire il backup.

```yaml
Type: KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome della chiave a cui eseguire il backup.

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputFile
Specifica il file di output in cui è archiviato il BLOB di backup.
Se non specifichi questo parametro, questo cmdlet genera un nome file.
Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VAULTNAME
Specifica il nome del Vault chiave che contiene la chiave per eseguire il backup.

```yaml
Type: String
Parameter Sets: ByKeyName
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

### Stringa
Il cmdlet restituisce il percorso del file di output contenente il backup della chiave.

## Note

## COLLEGAMENTI CORRELATI

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Ripristinare-AzKeyVaultKey](./Restore-AzKeyVaultKey.md)

