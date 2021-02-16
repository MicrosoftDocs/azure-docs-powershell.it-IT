---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185366"
---
# Update-AzKeyVaultSecret

## SYNOPSIS
Aggiorna gli attributi di un segreto in un vault delle chiavi.

## SINTASSI

### Predefinito (impostazione predefinita)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Update-AzKeyVaultSecret** aggiorna gli attributi modificabili di un segreto in un vault delle chiavi.

## ESEMPI

### Esempio 1: Modificare gli attributi di un segreto
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

I primi quattro comandi definiscono gli attributi per la data di scadenza, la data notBefore, i tag e il tipo di contesto e archiviano gli attributi nelle variabili.
Il comando finale modifica gli attributi per il segreto denominato HR nella chiave vault denominata ContosoVault, usando le variabili archiviate.

### Esempio 2: Eliminare i tag e il tipo di contenuto per un segreto
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Questo comando elimina i tag e il tipo di contenuto per la versione specificata del segreto denominato HR nella chiave vault denominata Contoso.

### Esempio 3: Disabilitare la versione corrente dei segreti il cui nome inizia con l'IT
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

Il primo comando archivia il valore stringa Contoso nella $Vault variabile.
Il secondo comando archivia il valore stringa IT nella $Prefix variabile.
Il terzo comando usa il cmdlet Get-AzKeyVaultSecret per ottenere i segreti nel vault delle chiavi specificato e quindi passa tali informazioni al cmdlet **Where-Object.** Il cmdlet **Where-Object** filtra i segreti per i nomi che iniziano con i caratteri IT. Il comando consente di determinare i segreti che corrispondono al filtro Update-AzKeyVaultSecret cmdlet, disabilitandoli così.

### Esempio 4: Impostare ContentType per tutte le versioni di un segreto
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

I primi tre comandi definiscono le variabili stringa da usare per i parametri *VaultName,* *Name* *e ContentType.* Il quarto comando usa il cmdlet Get-AzKeyVaultKey per ottenere le chiavi specificate e le pipe al cmdlet Update-AzKeyVaultSecret per impostare il tipo di contenuto su XML.

## PARAMETERS

### -ContentType
Tipo di contenuto segreto.
Se non viene specificato, il valore esistente del tipo di contenuto del segreto rimarrà invariato.
Rimuovere il valore del tipo di contenuto esistente specificando una stringa vuota.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Enable
Se presente, abilitare un segreto se il valore è vero.
Disabilitare un segreto se il valore è falso.
Se non viene specificato, il valore esistente dello stato abilitato/disabilitato del segreto rimane invariato.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scadenza
Ora di scadenza di un segreto in ora UTC.
Se non viene specificato, il valore esistente della scadenza del segreto rimane invariato.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oggetto segreto

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

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
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Ora UTC prima di cui non è possibile usare il segreto.
Se non viene specificato, il valore esistente dell'attributo NotBefore del segreto rimane invariato.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Il cmdlet non restituisce l'oggetto per impostazione predefinita.
Se questa opzione è specificata, restituisce l'oggetto Segreto.

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

### -Tag
Tabella hash che rappresenta i tag del segreto.
Se non viene specificato, i tag esistenti del segreto rimangono invariati.
Rimuovere un tag specificando una tabella hash vuota.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

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
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Versione segreta.
Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato, il nome segreto e la versione segreta.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## OUTPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret

## NOTE

## COLLEGAMENTI CORRELATI
