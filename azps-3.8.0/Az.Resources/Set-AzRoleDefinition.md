---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 9fbf7b753d5a277166670c337396c0dcd824448d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019675"
---
# <span data-ttu-id="6ab07-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab07-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="6ab07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ab07-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab07-103">Modifica un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="6ab07-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="6ab07-104">Fornisci la definizione di ruolo modificata sia come file JSON che come PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="6ab07-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="6ab07-105">Prima di tutto, usare il comando Get-AzRoleDefinition per recuperare il ruolo personalizzato che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="6ab07-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="6ab07-106">Modificare quindi le proprietà che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="6ab07-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="6ab07-107">Infine, salva la definizione del ruolo usando questo comando.</span><span class="sxs-lookup"><span data-stu-id="6ab07-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="6ab07-108">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ab07-108">SYNTAX</span></span>

### <span data-ttu-id="6ab07-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ab07-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab07-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ab07-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ab07-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ab07-111">DESCRIPTION</span></span>
<span data-ttu-id="6ab07-112">Il cmdlet Set-AzRoleDefinition aggiorna un ruolo personalizzato esistente in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="6ab07-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="6ab07-113">Fornisci la definizione di ruolo aggiornata come input per il comando come file JSON o un oggetto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="6ab07-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="6ab07-114">La definizione del ruolo per il ruolo personalizzato aggiornato deve contenere l'ID e tutte le altre proprietà necessarie del ruolo anche se non vengono aggiornate: DisplayName, Description, actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="6ab07-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="6ab07-115">I notactings, dataactions, NotDataActions sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="6ab07-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="6ab07-116">Di seguito è riportato un esempio di definizione del ruolo aggiornata JSON per Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-A39B-2a8205c3087e", "nome": "ruolo aggiornato", "Descrizione": "può monitorare tutte le risorse e avviare e riavviare le macchine virtuali", "azioni": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "notacttions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Read" \] , "NotDataActions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="6ab07-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="6ab07-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ab07-117">EXAMPLES</span></span>

### <span data-ttu-id="6ab07-118">Aggiornamento con PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="6ab07-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="6ab07-119">Creare usando un file JSON</span><span class="sxs-lookup"><span data-stu-id="6ab07-119">Create using JSON file</span></span>
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="6ab07-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ab07-120">PARAMETERS</span></span>

### <span data-ttu-id="6ab07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab07-121">-DefaultProfile</span></span>
<span data-ttu-id="6ab07-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6ab07-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ab07-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6ab07-123">-InputFile</span></span>
<span data-ttu-id="6ab07-124">Nome file che contiene una singola definizione di ruolo JSON da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="6ab07-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="6ab07-125">Includi solo le proprietà che devono essere aggiornate in JSON.</span><span class="sxs-lookup"><span data-stu-id="6ab07-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="6ab07-126">La proprietà ID è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="6ab07-126">Id property is Required.</span></span>

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

### <span data-ttu-id="6ab07-127">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="6ab07-127">-Role</span></span>
<span data-ttu-id="6ab07-128">Oggetto definizione ruolo da aggiornare</span><span class="sxs-lookup"><span data-stu-id="6ab07-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="6ab07-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab07-129">CommonParameters</span></span>
<span data-ttu-id="6ab07-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab07-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab07-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ab07-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab07-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ab07-132">INPUTS</span></span>

### <span data-ttu-id="6ab07-133">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab07-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="6ab07-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ab07-134">OUTPUTS</span></span>

### <span data-ttu-id="6ab07-135">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab07-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="6ab07-136">Note</span><span class="sxs-lookup"><span data-stu-id="6ab07-136">NOTES</span></span>
<span data-ttu-id="6ab07-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="6ab07-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6ab07-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ab07-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ab07-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="6ab07-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="6ab07-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab07-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="6ab07-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab07-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="6ab07-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6ab07-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

