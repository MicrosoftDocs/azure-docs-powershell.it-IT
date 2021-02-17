---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183655"
---
# New-AzRoleDefinition

## SYNOPSIS
Crea un ruolo personalizzato nel controllo degli accessi in base al ruolo di Azure.
Specificare un file di definizione del ruolo JSON o un oggetto PSRoleDefinition come input.
Prima di tutto, usare il Get-AzRoleDefinition riferimento per generare un oggetto definizione di ruolo di previsione.
Modificare quindi le proprietà in base alle esigenze.
Infine, usare questo comando per creare un ruolo personalizzato usando la definizione del ruolo.

## SINTASSI

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet New-AzRoleDefinition crea un ruolo personalizzato in Azure Role-Based controllo dell'accesso.
Fornire una definizione di ruolo come input per il comando come file JSON o oggetto PSRoleDefinition.
La definizione del ruolo di input DEVE contenere le proprietà seguenti:
1) DisplayName: nome del ruolo personalizzato
2) Descrizione: una breve descrizione del ruolo che riepiloga l'accesso concesso dal ruolo.
3) Azioni: insieme di operazioni a cui il ruolo personalizzato concede l'accesso.
Usare Get-AzProviderOperation per ottenere l'operazione per i provider di risorse di Azure che possono essere protetti con il controllo degli accessi in base al ruolo di Azure.
Di seguito sono riportate alcune stringhe di operazioni valide:
 - "*/read" concede l'accesso alle operazioni di lettura di tutti i provider di risorse di Azure.
 - "Microsoft.Network/*/read" concede l'accesso alle operazioni di lettura per tutti i tipi di risorse nel provider di risorse Microsoft.Network di Azure.
 - "Microsoft.Compute/virtualMachines/*" concede l'accesso a tutte le operazioni di macchine virtuali e ai relativi tipi di risorse figlio.
4) AssignableScopes: il set di ambiti (sottoscrizioni di Azure o gruppi di risorse) in cui il ruolo personalizzato sarà disponibile per l'assegnazione.
Con AssignableScopes è possibile rendere disponibile il ruolo personalizzato per l'assegnazione solo nelle sottoscrizioni o nei gruppi di risorse che ne hanno bisogno e non ingombrare l'esperienza utente per il resto delle sottoscrizioni o dei gruppi di risorse.
Di seguito sono riportati alcuni ambiti assegnabili validi:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rende disponibile il ruolo per l'assegnazione in due abbonamenti.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": rende disponibile il ruolo per l'assegnazione in un singolo abbonamento.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rende il ruolo disponibile per l'assegnazione solo nel gruppo di risorse di rete.
La definizione del ruolo di input MAY contiene le proprietà seguenti:
1) NotActions: set di operazioni che è necessario escludere dalle azioni per determinare le azioni effettive per il ruolo personalizzato.
Se è presente un'operazione specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è utile usare NotActions per escluderla, invece di specificare tutte le operazioni diverse da quella specifica in Azioni.
2) DataActions: set di operazioni dati a cui il ruolo personalizzato concede l'accesso.
3) NotDataActions: set di operazioni che è necessario escludere da DataActions per determinare le azioni dei dati effettive per il ruolo personalizzato.
Se è presente un'operazione dati specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è utile usare NotDataActions per escluderla, invece di specificare tutte le operazioni diverse da quella specifica in Azioni.
NOTA: se a un utente è assegnato un ruolo che specifica un'operazione in NotActions e anche a un altro ruolo viene concesso l'accesso alla stessa operazione, l'utente potrà eseguire l'operazione.
NotActions non è una regola di negazione, ma semplicemente un modo pratico per creare un set di operazioni consentite quando è necessario escludere specifiche operazioni.
Ecco una definizione di ruolo JSON di esempio che può essere fornita come input { "Nome": "Ruolo aggiornato", "Descrizione": "Può monitorare tutte le risorse e avviare e riavviare macchine virtuali", "Azioni": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers//blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## ESEMPI

### Esempio 1: Creare con PSRoleDefinitionObject
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### Esempio 2: Creare con il file JSON
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
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
Nome file contenente una singola definizione di ruolo Json.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Oggetto definizione ruolo.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## NOTE
Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione

## COLLEGAMENTI CORRELATI

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

