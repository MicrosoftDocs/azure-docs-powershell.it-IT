---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342235"
---
# New-AzRoleDefinition

## Sinossi
Crea un ruolo personalizzato in Azure RBAC.
Fornisci un file di definizione del ruolo JSON o un oggetto PSRoleDefinition come input.
Prima di tutto, usa il comando Get-AzRoleDefinition per generare un oggetto di definizione del ruolo previsto.
Modifica quindi le proprietà necessarie.
Infine, usa questo comando per creare un ruolo personalizzato usando la definizione di ruolo.

## SINTASSI

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet New-AzRoleDefinition crea un ruolo personalizzato in Azure Role-Based controllo di accesso.
Fornisci una definizione di ruolo come input per il comando come file JSON o un oggetto PSRoleDefinition.
La definizione del ruolo di input deve contenere le proprietà seguenti:
1) DisplayName: nome del ruolo personalizzato
2) Descrizione: breve descrizione del ruolo che riepiloga l'accesso concesso dal ruolo.
3) Actions: set di operazioni a cui il ruolo personalizzato concede l'accesso.
USA Get-AzProviderOperation per ottenere l'operazione per i provider di risorse Azure che possono essere protetti con Azure RBAC.
Di seguito sono elencate alcune stringhe di operazione valide:
 - "*/Read" concede l'accesso alle operazioni di lettura di tutti i provider di risorse di Azure.
 - "Microsoft. Network/*/Read" concede l'accesso alle operazioni di lettura per tutti i tipi di risorsa nel provider di risorse Microsoft. network di Azure.
 - "Microsoft. Compute/virtualMachines/*" concede l'accesso a tutte le operazioni delle macchine virtuali e dei relativi tipi di risorse figlio.
4) AssignableScopes: set di ambiti (abbonamenti Azure o gruppi di risorse) in cui il ruolo personalizzato sarà disponibile per l'assegnazione.
L'uso di AssignableScopes consente di rendere il ruolo personalizzato disponibile per l'assegnazione solo in abbonamenti o gruppi di risorse che ne hanno bisogno e non ingombrare l'esperienza utente per il resto delle sottoscrizioni o dei gruppi di risorse.
Di seguito sono riportati alcuni ambiti assegnabili validi:
 - "/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rende il ruolo disponibile per l'assegnazione in due abbonamenti.
 - "/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e": rende il ruolo disponibile per l'assegnazione in un singolo abbonamento.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rende il ruolo disponibile per l'assegnazione solo nel gruppo di risorse di rete.
La definizione del ruolo di input può contenere le proprietà seguenti:
1) Notactings: set di operazioni che devono essere escluse dalle azioni per determinare le azioni effettive per il ruolo personalizzato.
Se esiste un'operazione specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è consigliabile usare le notaction per escluderla, invece di specificare tutte le operazioni diverse da quella specifica in azioni.
2) Dataactions: set di operazioni sui dati a cui il ruolo personalizzato concede l'accesso.
3) NotDataActions: il set di operazioni che deve essere escluso dalle azioni dataactions per determinare le azioni di dati efficaci per il ruolo personalizzato.
Se è presente un'operazione dati specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è consigliabile usare NotDataActions per escluderla, anziché specificare tutte le operazioni diverse da quella specifica in azioni.
Nota: se a un utente viene assegnato un ruolo che specifica un'operazione in notactings e anche un altro ruolo concede l'accesso alla stessa operazione, l'utente potrà eseguire tale operazione.
Notactings non è una regola di negazione, ma è semplicemente un modo comodo per creare un set di operazioni consentite quando è necessario escludere specifiche operazioni.
Di seguito è riportato un esempio di definizione del ruolo JSON che può essere fornita come input {"Name": "resourced Role", "Description": "può monitorare tutte le risorse e avviare e riavviare le macchine virtuali", "Actions": \[ "*/Read", "Microsoft. ClassicCompute/VirtualMachines/restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "notacttions": \[ "*/Write" \] , "dataactions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Read" \] , "NotDataActions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## ESEMPI

### Esempio 1: creare usando PSRoleDefinitionObject
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

### Esempio 2: creare usando un file JSON
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETRI

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

### -InputFile
Nome file che contiene una singola definizione di ruolo JSON.

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

### -Ruolo
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment

## COLLEGAMENTI CORRELATI

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

