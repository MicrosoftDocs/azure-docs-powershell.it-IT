---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863042"
---
# Get-AzKeyVaultSecret

## Sinossi
Ottiene i segreti in un caveau chiave.

## SINTASSI

### ByVaultName (impostazione predefinita)
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretName
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BySecretVersions
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedSecrets
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzKeyVaultSecret** ottiene segreti in un caveau chiave.
Questo cmdlet ottiene un segreto specifico o tutti i segreti in un Vault chiave.

## ESEMPI

### Esempio 1: ottenere tutte le versioni correnti di tutti i segreti in un Vault chiave
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

Questo comando consente di ottenere le versioni correnti di tutti i segreti nel caveau della chiave denominato contoso.

### Esempio 2: ottenere tutte le versioni di un segreto specifico
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

Questo comando consente di ottenere tutte le versioni del segreto denominato ITSecret nel caveau della chiave denominato contoso.

### Esempio 3: ottenere la versione corrente di un segreto specifico
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

Questo comando consente di ottenere la versione corrente del segreto denominato ITSecret nel caveau della chiave denominato contoso.

### Esempio 4: ottenere una versione specifica di un segreto specifico
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

Questo comando consente di ottenere una versione specifica del segreto denominata ITSecret nel caveau della chiave denominato contoso.

### Esempio 5: ottenere il valore di testo normale della versione corrente di un segreto specifico
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

Questi comandi ottengono la versione corrente di un segreto denominato ITSecret e quindi Visualizza il valore di testo normale di tale segreto.

### Esempio 6: ottenere tutti i segreti eliminati ma non eliminati per il Vault chiave.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

Questo comando ottiene tutti i segreti eliminati in precedenza, ma non eliminati, nel caveau della chiave denominato contoso.

### Esempio 7: Ottiene il ITSecret segreto che è stato eliminato ma non eliminato per questo Vault chiave.
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

Questo comando ottiene il ITSecret segreto che è stato eliminato in precedenza, ma non è stato eliminato, nel caveau della chiave denominato contoso.
Questo comando restituirà metadati come la data di eliminazione e la data di eliminazione pianificata di questo segreto eliminato.

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

### -IncludeVersions
Indica che questo cmdlet ottiene tutte le versioni di un segreto.
La versione corrente di un segreto è la prima nell'elenco.
Se specifichi questo parametro devi anche specificare i parametri *Name* e *VAULTNAME* .

Se non specifichi il parametro *includeVersions* , questo cmdlet ottiene la versione corrente del segreto con il *nome* specificato.

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Specifica se visualizzare i segreti eliminati in precedenza nell'output

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del segreto da ottenere.

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VAULTNAME
Specifica il nome del Vault chiave a cui appartiene il segreto.
Questo cmdlet costruisce il nome di dominio completo (FQDN) di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.

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

### -Versione
Specifica la versione segreta.
Questo cmdlet crea l'FQDN di un segreto in base al nome del Vault chiave, all'ambiente selezionato, al nome segreto e alla versione segreta.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Stringa

## OUTPUT

### Elenco<Microsoft. Azure. Commands. Vault. Models. SecretIdentityItem>, Microsoft. Azure. Commands. Vault. Models. Secret, List<Microsoft. Azure. Commands. Vault. Models. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. Vault. Models. DeletedSecret

## Note

## COLLEGAMENTI CORRELATI

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Undo-AzKeyVaultSecretRemoval](./Undo-AzKeyVaultSecretRemoval.md)

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

