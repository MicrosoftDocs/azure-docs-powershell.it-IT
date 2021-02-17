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
# <span data-ttu-id="653e5-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="653e5-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="653e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="653e5-102">SYNOPSIS</span></span>
<span data-ttu-id="653e5-103">Crea un ruolo personalizzato nel controllo degli accessi in base al ruolo di Azure.</span><span class="sxs-lookup"><span data-stu-id="653e5-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="653e5-104">Specificare un file di definizione del ruolo JSON o un oggetto PSRoleDefinition come input.</span><span class="sxs-lookup"><span data-stu-id="653e5-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="653e5-105">Prima di tutto, usare il Get-AzRoleDefinition riferimento per generare un oggetto definizione di ruolo di previsione.</span><span class="sxs-lookup"><span data-stu-id="653e5-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="653e5-106">Modificare quindi le proprietà in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="653e5-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="653e5-107">Infine, usare questo comando per creare un ruolo personalizzato usando la definizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="653e5-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="653e5-108">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="653e5-108">SYNTAX</span></span>

### <span data-ttu-id="653e5-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="653e5-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="653e5-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="653e5-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="653e5-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="653e5-111">DESCRIPTION</span></span>
<span data-ttu-id="653e5-112">Il cmdlet New-AzRoleDefinition crea un ruolo personalizzato in Azure Role-Based controllo dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="653e5-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="653e5-113">Fornire una definizione di ruolo come input per il comando come file JSON o oggetto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="653e5-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="653e5-114">La definizione del ruolo di input DEVE contenere le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="653e5-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="653e5-115">DisplayName: nome del ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="653e5-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="653e5-116">Descrizione: una breve descrizione del ruolo che riepiloga l'accesso concesso dal ruolo.</span><span class="sxs-lookup"><span data-stu-id="653e5-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="653e5-117">Azioni: insieme di operazioni a cui il ruolo personalizzato concede l'accesso.</span><span class="sxs-lookup"><span data-stu-id="653e5-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="653e5-118">Usare Get-AzProviderOperation per ottenere l'operazione per i provider di risorse di Azure che possono essere protetti con il controllo degli accessi in base al ruolo di Azure.</span><span class="sxs-lookup"><span data-stu-id="653e5-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="653e5-119">Di seguito sono riportate alcune stringhe di operazioni valide:</span><span class="sxs-lookup"><span data-stu-id="653e5-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="653e5-120">"\*/read" concede l'accesso alle operazioni di lettura di tutti i provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="653e5-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="653e5-121">"Microsoft.Network/\*/read" concede l'accesso alle operazioni di lettura per tutti i tipi di risorse nel provider di risorse Microsoft.Network di Azure.</span><span class="sxs-lookup"><span data-stu-id="653e5-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="653e5-122">"Microsoft.Compute/virtualMachines/\*" concede l'accesso a tutte le operazioni di macchine virtuali e ai relativi tipi di risorse figlio.</span><span class="sxs-lookup"><span data-stu-id="653e5-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="653e5-123">AssignableScopes: il set di ambiti (sottoscrizioni di Azure o gruppi di risorse) in cui il ruolo personalizzato sarà disponibile per l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="653e5-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="653e5-124">Con AssignableScopes è possibile rendere disponibile il ruolo personalizzato per l'assegnazione solo nelle sottoscrizioni o nei gruppi di risorse che ne hanno bisogno e non ingombrare l'esperienza utente per il resto delle sottoscrizioni o dei gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="653e5-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="653e5-125">Di seguito sono riportati alcuni ambiti assegnabili validi:</span><span class="sxs-lookup"><span data-stu-id="653e5-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="653e5-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rende disponibile il ruolo per l'assegnazione in due abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="653e5-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="653e5-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": rende disponibile il ruolo per l'assegnazione in un singolo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="653e5-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="653e5-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rende il ruolo disponibile per l'assegnazione solo nel gruppo di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="653e5-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="653e5-129">La definizione del ruolo di input MAY contiene le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="653e5-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="653e5-130">NotActions: set di operazioni che è necessario escludere dalle azioni per determinare le azioni effettive per il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="653e5-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="653e5-131">Se è presente un'operazione specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è utile usare NotActions per escluderla, invece di specificare tutte le operazioni diverse da quella specifica in Azioni.</span><span class="sxs-lookup"><span data-stu-id="653e5-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="653e5-132">DataActions: set di operazioni dati a cui il ruolo personalizzato concede l'accesso.</span><span class="sxs-lookup"><span data-stu-id="653e5-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="653e5-133">NotDataActions: set di operazioni che è necessario escludere da DataActions per determinare le azioni dei dati effettive per il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="653e5-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="653e5-134">Se è presente un'operazione dati specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è utile usare NotDataActions per escluderla, invece di specificare tutte le operazioni diverse da quella specifica in Azioni.</span><span class="sxs-lookup"><span data-stu-id="653e5-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="653e5-135">NOTA: se a un utente è assegnato un ruolo che specifica un'operazione in NotActions e anche a un altro ruolo viene concesso l'accesso alla stessa operazione, l'utente potrà eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="653e5-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="653e5-136">NotActions non è una regola di negazione, ma semplicemente un modo pratico per creare un set di operazioni consentite quando è necessario escludere specifiche operazioni.</span><span class="sxs-lookup"><span data-stu-id="653e5-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="653e5-137">Ecco una definizione di ruolo JSON di esempio che può essere fornita come input { "Nome": "Ruolo aggiornato", "Descrizione": "Può monitorare tutte le risorse e avviare e riavviare macchine virtuali", "Azioni": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers//blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="653e5-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="653e5-138">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="653e5-138">EXAMPLES</span></span>

### <span data-ttu-id="653e5-139">Esempio 1: Creare con PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="653e5-139">Example 1: Create using PSRoleDefinitionObject</span></span>
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

### <span data-ttu-id="653e5-140">Esempio 2: Creare con il file JSON</span><span class="sxs-lookup"><span data-stu-id="653e5-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="653e5-141">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="653e5-141">PARAMETERS</span></span>

### <span data-ttu-id="653e5-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="653e5-142">-DefaultProfile</span></span>
<span data-ttu-id="653e5-143">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="653e5-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="653e5-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="653e5-144">-InputFile</span></span>
<span data-ttu-id="653e5-145">Nome file contenente una singola definizione di ruolo Json.</span><span class="sxs-lookup"><span data-stu-id="653e5-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="653e5-146">-Role</span><span class="sxs-lookup"><span data-stu-id="653e5-146">-Role</span></span>
<span data-ttu-id="653e5-147">Oggetto definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="653e5-147">Role definition object.</span></span>

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

### <span data-ttu-id="653e5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="653e5-148">CommonParameters</span></span>
<span data-ttu-id="653e5-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="653e5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="653e5-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="653e5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="653e5-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="653e5-151">INPUTS</span></span>

### <span data-ttu-id="653e5-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="653e5-152">None</span></span>

## <span data-ttu-id="653e5-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="653e5-153">OUTPUTS</span></span>

### <span data-ttu-id="653e5-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="653e5-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="653e5-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="653e5-155">NOTES</span></span>
<span data-ttu-id="653e5-156">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="653e5-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="653e5-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="653e5-157">RELATED LINKS</span></span>

[<span data-ttu-id="653e5-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="653e5-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="653e5-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="653e5-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="653e5-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="653e5-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="653e5-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="653e5-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

