---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 23bba16ea6e80d784a9de9bfb10a3a127f53b3f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519530"
---
# <span data-ttu-id="d7f11-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d7f11-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="d7f11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7f11-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f11-103">Crea un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="d7f11-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="d7f11-104">Fornisci un file di definizione del ruolo JSON o un oggetto PSRoleDefinition come input.</span><span class="sxs-lookup"><span data-stu-id="d7f11-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="d7f11-105">Prima di tutto, usa il comando Get-AzureRmRoleDefinition per generare un oggetto di definizione del ruolo previsto.</span><span class="sxs-lookup"><span data-stu-id="d7f11-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="d7f11-106">Modifica quindi le proprietà necessarie.</span><span class="sxs-lookup"><span data-stu-id="d7f11-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="d7f11-107">Infine, usa questo comando per creare un ruolo personalizzato usando la definizione di ruolo.</span><span class="sxs-lookup"><span data-stu-id="d7f11-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7f11-108">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7f11-108">SYNTAX</span></span>

### <span data-ttu-id="d7f11-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7f11-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7f11-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7f11-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7f11-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7f11-111">DESCRIPTION</span></span>
<span data-ttu-id="d7f11-112">Il cmdlet New-AzureRmRoleDefinition crea un ruolo personalizzato in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="d7f11-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="d7f11-113">Fornisci una definizione di ruolo come input per il comando come file JSON o un oggetto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="d7f11-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>

<span data-ttu-id="d7f11-114">La definizione del ruolo di input deve contenere le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7f11-114">The input role definition MUST contain the following properties:</span></span>

1) <span data-ttu-id="d7f11-115">DisplayName: nome del ruolo personalizzato</span><span class="sxs-lookup"><span data-stu-id="d7f11-115">DisplayName: the name of the custom role</span></span>

2) <span data-ttu-id="d7f11-116">Descrizione: breve descrizione del ruolo che riepiloga l'accesso concesso dal ruolo.</span><span class="sxs-lookup"><span data-stu-id="d7f11-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>

3) <span data-ttu-id="d7f11-117">Actions: set di operazioni a cui il ruolo personalizzato concede l'accesso.</span><span class="sxs-lookup"><span data-stu-id="d7f11-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="d7f11-118">USA Get-AzureRmProviderOperations per ottenere l'operazione per i provider di risorse Azure che possono essere protetti con Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="d7f11-118">Use Get-AzureRmProviderOperations to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="d7f11-119">Di seguito sono elencate alcune stringhe di operazione valide:</span><span class="sxs-lookup"><span data-stu-id="d7f11-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="d7f11-120">"\*/Read" concede l'accesso alle operazioni di lettura di tutti i provider di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f11-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="d7f11-121">"Microsoft. Network/\*/Read" concede l'accesso alle operazioni di lettura per tutti i tipi di risorsa nel provider di risorse Microsoft. network di Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f11-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="d7f11-122">"Microsoft. Compute/virtualMachines/\*" concede l'accesso a tutte le operazioni delle macchine virtuali e dei relativi tipi di risorse figlio.</span><span class="sxs-lookup"><span data-stu-id="d7f11-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>

4) <span data-ttu-id="d7f11-123">AssignableScopes: set di ambiti (abbonamenti Azure o gruppi di risorse) in cui il ruolo personalizzato sarà disponibile per l'assegnazione.</span><span class="sxs-lookup"><span data-stu-id="d7f11-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="d7f11-124">L'uso di AssignableScopes consente di rendere il ruolo personalizzato disponibile per l'assegnazione solo in abbonamenti o gruppi di risorse che ne hanno bisogno e non ingombrare l'esperienza utente per il resto delle sottoscrizioni o dei gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="d7f11-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="d7f11-125">Di seguito sono riportati alcuni ambiti assegnabili validi:</span><span class="sxs-lookup"><span data-stu-id="d7f11-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="d7f11-126">"/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": rende il ruolo disponibile per l'assegnazione in due abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="d7f11-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="d7f11-127">"/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e": rende il ruolo disponibile per l'assegnazione in un singolo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d7f11-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="d7f11-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": rende il ruolo disponibile per l'assegnazione solo nel gruppo di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="d7f11-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>

<span data-ttu-id="d7f11-129">La definizione del ruolo di input può contenere le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7f11-129">The input role definition MAY contain the following properties:</span></span>

1) <span data-ttu-id="d7f11-130">Notactings: set di operazioni che devono essere escluse dalle azioni per determinare le azioni effettive per il ruolo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d7f11-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="d7f11-131">Se esiste un'operazione specifica a cui non si vuole concedere l'accesso in un ruolo personalizzato, è consigliabile usare le notaction per escluderla, invece di specificare tutte le operazioni diverse da quella specifica in azioni.</span><span class="sxs-lookup"><span data-stu-id="d7f11-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>

<span data-ttu-id="d7f11-132">Nota: se a un utente viene assegnato un ruolo che specifica un'operazione in notactings e anche un altro ruolo concede l'accesso alla stessa operazione, l'utente potrà eseguire tale operazione.</span><span class="sxs-lookup"><span data-stu-id="d7f11-132">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="d7f11-133">Notactings non è una regola di negazione, ma è semplicemente un modo comodo per creare un set di operazioni consentite quando è necessario escludere specifiche operazioni.</span><span class="sxs-lookup"><span data-stu-id="d7f11-133">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>

<span data-ttu-id="d7f11-134">Di seguito è riportato un esempio di definizione di ruolo JSON che può essere fornita come input {"Name": "contoso su chiamata", "Descrizione": "può monitorare il calcolo, la rete e lo spazio di archiviazione e riavviare le macchine virtuali", "azioni": \[ "Microsoft. Compute/ */Read", "Microsoft. Compute/virtualMachines/Start/Action", "Microsoft. Compute/virtualMachines/restart/Action", "Microsoft. Compute/VirtualMachines/downloadRemoteDesktopConnectionFile/Action", "Microsoft. Network/* /Read", "Microsoft. storage/ */Read", "Microsoft. Authorization/* /Read", "Microsoft. resources/subscriptions/resourceGroups/Read", "Microsoft. resources/subscriptions/resourceGroups/Resources/Read", "Microsoft. Insights/AlertRules/ *", "Microsoft. support/* " \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \]</span><span class="sxs-lookup"><span data-stu-id="d7f11-134">Following is a sample json role definition that can be provided as input { "Name": "Contoso On-call", "Description": "Can monitor compute, network and storage, and restart virtual machines", "Actions": \[ "Microsoft.Compute/ */read", "Microsoft.Compute/virtualMachines/start/action", "Microsoft.Compute/virtualMachines/restart/action", "Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action", "Microsoft.Network/* /read", "Microsoft.Storage/ */read", "Microsoft.Authorization/* /read", "Microsoft.Resources/subscriptions/resourceGroups/read", "Microsoft.Resources/subscriptions/resourceGroups/resources/read", "Microsoft.Insights/alertRules/ *", "Microsoft.Support/* " \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx","/subscriptions/yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy"\] }</span></span>

## <span data-ttu-id="d7f11-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7f11-135">EXAMPLES</span></span>

### <span data-ttu-id="d7f11-136">--------------------------Creare usando PSRoleDefinitionObject--------------------------</span><span class="sxs-lookup"><span data-stu-id="d7f11-136">--------------------------  Create using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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
          PS C:\> $role.AssignableScopes.Add("/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e")

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="d7f11-137">--------------------------Creare l'uso di file JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="d7f11-137">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="d7f11-138">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7f11-138">PARAMETERS</span></span>

### <span data-ttu-id="d7f11-139">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d7f11-139">-InputFile</span></span>
<span data-ttu-id="d7f11-140">Nome file che contiene una singola definizione di ruolo JSON.</span><span class="sxs-lookup"><span data-stu-id="d7f11-140">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="d7f11-141">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="d7f11-141">-Role</span></span>
<span data-ttu-id="d7f11-142">Oggetto definizione ruolo.</span><span class="sxs-lookup"><span data-stu-id="d7f11-142">Role definition object.</span></span>

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

### <span data-ttu-id="d7f11-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f11-143">-DefaultProfile</span></span>
<span data-ttu-id="d7f11-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f11-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f11-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f11-145">CommonParameters</span></span>
<span data-ttu-id="d7f11-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f11-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f11-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f11-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f11-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7f11-148">INPUTS</span></span>

## <span data-ttu-id="d7f11-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7f11-149">OUTPUTS</span></span>

### <span data-ttu-id="d7f11-150">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d7f11-150">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="d7f11-151">Note</span><span class="sxs-lookup"><span data-stu-id="d7f11-151">NOTES</span></span>
<span data-ttu-id="d7f11-152">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="d7f11-152">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d7f11-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7f11-153">RELATED LINKS</span></span>

[<span data-ttu-id="d7f11-154">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d7f11-154">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="d7f11-155">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d7f11-155">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="d7f11-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d7f11-156">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="d7f11-157">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="d7f11-157">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

