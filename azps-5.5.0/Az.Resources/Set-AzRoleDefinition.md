---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183623"
---
# Set-AzRoleDefinition

## SYNOPSIS
Modifica un ruolo personalizzato nel controllo degli accessi in base al ruolo di Azure.
Fornire la definizione di ruolo modificata come file JSON o PSRoleDefinition.
Prima di tutto, Get-AzRoleDefinition per recuperare il ruolo personalizzato che si vuole modificare.
Modificare quindi le proprietà che si desidera modificare.
Infine, salvare la definizione del ruolo con questo comando.

## SINTASSI

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet Set-AzRoleDefinition aggiorna un ruolo personalizzato esistente in Azure Role-Based controllo dell'accesso.
Fornire la definizione di ruolo aggiornata come input del comando come file JSON o oggetto PSRoleDefinition.
La definizione del ruolo personalizzato aggiornato DEVE contenere l'ID e tutte le altre proprietà obbligatorie del ruolo anche se non vengono aggiornate: DisplayName, Description, Actions, AssignableScopes.
NotActions, DataActions, NotDataActions sono facoltativi.
Quello che segue è un json di esempio aggiornato della definizione del ruolo per Set-AzRoleDefinition { "ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Nome": "Ruolo aggiornato", "Descrizione": "Può monitorare tutte le risorse e avviare e riavviare le macchine virtuali", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## ESEMPI

### Esempio 1: Aggiornamento con PSRoleDefinitionObject
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### Esempio 2: Creare con il file JSON
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

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

### -InputFile
Nome file contenente una singola definizione di ruolo Json da aggiornare.
Includere solo le proprietà da aggiornare nel JSON.
La proprietà ID è obbligatoria.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Oggetto definizione ruolo da aggiornare

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## OUTPUT

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## NOTE
Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione

## COLLEGAMENTI CORRELATI

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

