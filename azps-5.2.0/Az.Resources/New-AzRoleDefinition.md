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
# <span data-ttu-id="88728-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="88728-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="88728-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88728-102">SYNOPSIS</span></span>
<span data-ttu-id="88728-103">Crea un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="88728-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="88728-104">Fornisci un file di definizione del ruolo JSON o un oggetto PSRoleDefinition come input.</span><span class="sxs-lookup"><span data-stu-id="88728-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="88728-105">Prima di tutto, usa il comando Get-AzRoleDefinition per generare un oggetto di definizione del ruolo previsto.</span><span class="sxs-lookup"><span data-stu-id="88728-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="88728-106">Modifica quindi le proprietà necessarie.</span><span class="sxs-lookup"><span data-stu-id="88728-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="88728-107">Infine, usa questo comando per creare un ruolo personalizzato usando la definizione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="88728-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="88728-108">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88728-108">SYNTAX</span></span>

### <span data-ttu-id="88728-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="88728-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88728-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="88728-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88728-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88728-111">DESCRIPTION</span></span>
<span data-ttu-id="88728-112">Il cmdlet New-AzRoleDefinition crea un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="88728-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="88728-113">Fornisci una definizione di ruolo come input per il comando come file JSON o un oggetto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="88728-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="88728-114">La definizione del ruolo di input deve contenere le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="88728-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="88728-115">DisplayName: nome del ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="88728-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="88728-116">Descrizione: breve descrizione del ruolo che riepiloga l'accesso concesso dal ruolo.</span><span class="sxs-lookup"><span data-stu-id="88728-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="88728-117">Actions: set di operazioni a cui il ruolo personalizzato concede l'accesso.</span><span class="sxs-lookup"><span data-stu-id="88728-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="88728-118">USA Get-AzProviderOperation per ottenere l'operazione per i provider di risorse Azure che possono essere protetti con Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="88728-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="88728-119">Di seguito sono elencate alcune stringhe di operazione valide:</span><span class="sxs-lookup"><span data-stu-id="88728-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="88728-120">"\*/Read" concede l'accesso alle operazioni di lettura di tutti i provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="88728-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="88728-121">"Microsoft. Network/\*/Read" concede l'accesso alle operazioni di lettura per tutti i tipi di risorsa nel provider di risorse Microsoft. network di Azure.</span><span class="sxs-lookup"><span data-stu-id="88728-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="88728-122">"Microsoft. Compute/virtualMachines/\*" concede l'accesso a tutte le operazioni delle macchine virtuali e dei relativi tipi di risorse figlio.</span><span class="sxs-lookup"><span data-stu-id="88728-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="88728-123">AssignableScopes: set di ambiti (abbonamenti Azure o gruppi di risorse) in cui il ruolo personalizzato sarà disponibile per l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="88728-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="88728-124">L'uso di AssignableScopes consente di rendere il ruolo personalizzato disponibile per l'assegnazione solo in abbonamenti o gruppi di risorse che ne hanno bisogno e non ingombrare l'esperienza utente per il resto delle sottoscrizioni o dei gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="88728-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="88728-125">Di seguito sono riportati alcuni ambiti assegnabili validi:</span><span class="sxs-lookup"><span data-stu-id="88728-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="88728-126">"/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rende il ruolo disponibile per l'assegnazione in due abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="88728-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="88728-127">"/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e": rende il ruolo disponibile per l'assegnazione in un singolo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="88728-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="88728-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rende il ruolo disponibile per l'assegnazione solo nel gruppo di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="88728-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="88728-129">La definizione del ruolo di input può contenere le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="88728-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="88728-130">Notactings: set di operazioni che devono essere escluse dalle azioni per determinare le azioni effettive per il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="88728-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="88728-131">Se esiste un'operazione specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è consigliabile usare le notaction per escluderla, invece di specificare tutte le operazioni diverse da quella specifica in azioni.</span><span class="sxs-lookup"><span data-stu-id="88728-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="88728-132">Dataactions: set di operazioni sui dati a cui il ruolo personalizzato concede l'accesso.</span><span class="sxs-lookup"><span data-stu-id="88728-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="88728-133">NotDataActions: il set di operazioni che deve essere escluso dalle azioni dataactions per determinare le azioni di dati efficaci per il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="88728-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="88728-134">Se è presente un'operazione dati specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è consigliabile usare NotDataActions per escluderla, anziché specificare tutte le operazioni diverse da quella specifica in azioni.</span><span class="sxs-lookup"><span data-stu-id="88728-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="88728-135">Nota: se a un utente viene assegnato un ruolo che specifica un'operazione in notactings e anche un altro ruolo concede l'accesso alla stessa operazione, l'utente potrà eseguire tale operazione.</span><span class="sxs-lookup"><span data-stu-id="88728-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="88728-136">Notactings non è una regola di negazione, ma è semplicemente un modo comodo per creare un set di operazioni consentite quando è necessario escludere specifiche operazioni.</span><span class="sxs-lookup"><span data-stu-id="88728-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="88728-137">Di seguito è riportato un esempio di definizione del ruolo JSON che può essere fornita come input {"Name": "resourced Role", "Description": "può monitorare tutte le risorse e avviare e riavviare le macchine virtuali", "Actions": \[ "*/Read", "Microsoft. ClassicCompute/VirtualMachines/restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "notacttions": \[ "*/Write" \] , "dataactions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Read" \] , "NotDataActions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="88728-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="88728-138">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88728-138">EXAMPLES</span></span>

### <span data-ttu-id="88728-139">Esempio 1: creare usando PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="88728-139">Example 1: Create using PSRoleDefinitionObject</span></span>
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

### <span data-ttu-id="88728-140">Esempio 2: creare usando un file JSON</span><span class="sxs-lookup"><span data-stu-id="88728-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="88728-141">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88728-141">PARAMETERS</span></span>

### <span data-ttu-id="88728-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88728-142">-DefaultProfile</span></span>
<span data-ttu-id="88728-143">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88728-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88728-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="88728-144">-InputFile</span></span>
<span data-ttu-id="88728-145">Nome file che contiene una singola definizione di ruolo JSON.</span><span class="sxs-lookup"><span data-stu-id="88728-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="88728-146">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="88728-146">-Role</span></span>
<span data-ttu-id="88728-147">Oggetto definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="88728-147">Role definition object.</span></span>

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

### <span data-ttu-id="88728-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88728-148">CommonParameters</span></span>
<span data-ttu-id="88728-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88728-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88728-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88728-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88728-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88728-151">INPUTS</span></span>

### <span data-ttu-id="88728-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="88728-152">None</span></span>

## <span data-ttu-id="88728-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88728-153">OUTPUTS</span></span>

### <span data-ttu-id="88728-154">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="88728-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="88728-155">Note</span><span class="sxs-lookup"><span data-stu-id="88728-155">NOTES</span></span>
<span data-ttu-id="88728-156">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="88728-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="88728-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88728-157">RELATED LINKS</span></span>

[<span data-ttu-id="88728-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="88728-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="88728-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="88728-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="88728-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="88728-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="88728-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="88728-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

