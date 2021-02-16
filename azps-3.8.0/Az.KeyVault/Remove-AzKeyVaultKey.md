---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 75d781527a9783c81eba5bd2aacf07d237ef4f8f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412079"
---
# Remove-AzKeyVaultKey

## SYNOPSIS
Elimina una chiave in un vault delle chiavi.

## SINTASSI

### ByVaultName (impostazione predefinita)
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il Remove-AzKeyVaultKey cmdlet elimina una chiave in un vault delle chiavi.
Se la chiave è stata eliminata accidentalmente, può essere recuperata usando Undo-AzKeyVaultKeyRemoval da un utente con speciali autorizzazioni di "recupero".
Questo cmdlet ha un valore alto per la **proprietà ConfirmImpact.**

## ESEMPI

### Esempio 1: Rimuovere una chiave da un vault delle chiavi
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

Questo comando rimuove la chiave denominata ITSoftware dalla chiave vault denominata Contoso.

### Esempio 2: Rimuovere una chiave senza conferma utente
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

Questo comando rimuove la chiave denominata ITSoftware dalla chiave vault denominata Contoso.
Il comando specifica il *parametro Force* e, di conseguenza, il cmdlet non richiede conferma.

### Esempio 3: Eliminare definitivamente una chiave eliminata dal vault delle chiavi
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

Questo comando rimuove la chiave denominata ITSoftware dalla chiave vault denominata Contoso in modo permanente.
Per l'esecuzione di questo cmdlet è necessaria l'autorizzazione di eliminazione, che deve essere stata concessa in precedenza ed esplicitamente all'utente per il vault della chiave.

### Esempio 4: Rimuovere chiavi usando l'operatore pipeline
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

Questo comando recupera tutte le chiavi nel vault delle chiavi denominato Contoso e le passa al cmdlet **Where-Object** usando l'operatore pipeline.
Questo cmdlet passa le chiavi che hanno un valore di $False per **l'attributo Enabled** al cmdlet corrente.
Questo cmdlet rimuove queste chiavi.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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
Forza l'esecuzione del comando senza chiedere conferma all'utente.

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
Oggetto KeyBundle

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InRemovedState
Rimuovere definitivamente la chiave eliminata in precedenza.

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

### -Name
Specifica il nome della chiave da rimuovere.
Questo cmdlet crea il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, al nome del vault delle chiavi e all'ambiente corrente.

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indica che questo cmdlet restituisce un **oggetto Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey.**
Per impostazione predefinita, questo cmdlet non genera alcun output.

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
Specifica il nome del vault della chiave da cui rimuovere la chiave.
Questo cmdlet crea l'FQDN di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente corrente.

```yaml
Type: System.String
Parameter Sets: ByVaultName
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem

## OUTPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey

## NOTE

## COLLEGAMENTI CORRELATI

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)


[Undo-AzKeyVaultKeyRemoval](./Undo-AzKeyVaultKeyRemoval.md)

