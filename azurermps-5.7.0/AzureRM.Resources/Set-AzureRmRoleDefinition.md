---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 2282bdef70f6352caa535b4d7a68d5e4046f831e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507975"
---
# <span data-ttu-id="f1f3a-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1f3a-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="f1f3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f3a-103">Modifica un ruolo personalizzato in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="f1f3a-104">Fornisci la definizione di ruolo modificata sia come file JSON che come PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="f1f3a-105">Prima di tutto, usare il comando Get-AzureRmRoleDefinition per recuperare il ruolo personalizzato che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="f1f3a-106">Modificare quindi le proprietà che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="f1f3a-107">Infine, salva la definizione del ruolo usando questo comando.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1f3a-108">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1f3a-108">SYNTAX</span></span>

### <span data-ttu-id="f1f3a-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f3a-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1f3a-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1f3a-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f3a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1f3a-111">DESCRIPTION</span></span>
<span data-ttu-id="f1f3a-112">Il cmdlet Set-AzureRmRoleDefinition aggiorna un ruolo personalizzato esistente in Azure Role-Based controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="f1f3a-113">Fornisci la definizione di ruolo aggiornata come input per il comando come file JSON o un oggetto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="f1f3a-114">La definizione del ruolo per il ruolo personalizzato aggiornato deve contenere l'ID e tutte le altre proprietà necessarie del ruolo anche se non vengono aggiornate: DisplayName, Description, actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="f1f3a-115">I notactings, dataactions, NotDataActions sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-115">NotActions, DataActions, NotDataActions are optional.</span></span>

<span data-ttu-id="f1f3a-116">Di seguito è riportato un esempio di codice JSON di definizione del ruolo aggiornato per Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1f3a-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="f1f3a-117">{"ID": "52a6cc13-ff92-47a8-A39B-2a8205c3087e", "nome": "ruolo aggiornato", "Descrizione": "può monitorare tutte le risorse e avviare e riavviare le macchine virtuali", "azioni": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "notacttions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Read" \] , "NotDataActions": \[ "Microsoft. storage/storageAccounts/blobServices/Containers/Blobs/Write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="f1f3a-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="f1f3a-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1f3a-118">EXAMPLES</span></span>

### <span data-ttu-id="f1f3a-119">Aggiornamento con PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="f1f3a-119">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="f1f3a-120">Creare usando un file JSON</span><span class="sxs-lookup"><span data-stu-id="f1f3a-120">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="f1f3a-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1f3a-121">PARAMETERS</span></span>

### <span data-ttu-id="f1f3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f3a-122">-DefaultProfile</span></span>
<span data-ttu-id="f1f3a-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f1f3a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f3a-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f1f3a-124">-InputFile</span></span>
<span data-ttu-id="f1f3a-125">Nome file che contiene una singola definizione di ruolo JSON da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-125">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="f1f3a-126">Includi solo le proprietà che devono essere aggiornate in JSON.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-126">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="f1f3a-127">La proprietà ID è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-127">Id property is Required.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f3a-128">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="f1f3a-128">-Role</span></span>
<span data-ttu-id="f1f3a-129">Oggetto definizione ruolo da aggiornare</span><span class="sxs-lookup"><span data-stu-id="f1f3a-129">Role definition object to be updated</span></span>

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1f3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f3a-130">CommonParameters</span></span>
<span data-ttu-id="f1f3a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1f3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f3a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f3a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f3a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1f3a-133">INPUTS</span></span>

### <span data-ttu-id="f1f3a-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1f3a-134">PSRoleDefinition</span></span>
<span data-ttu-id="f1f3a-135">Il parametro "ruolo" accetta il valore di tipo "PSRoleDefinition" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f1f3a-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="f1f3a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1f3a-136">OUTPUTS</span></span>

### <span data-ttu-id="f1f3a-137">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1f3a-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f1f3a-138">Note</span><span class="sxs-lookup"><span data-stu-id="f1f3a-138">NOTES</span></span>
<span data-ttu-id="f1f3a-139">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="f1f3a-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f1f3a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1f3a-140">RELATED LINKS</span></span>

[<span data-ttu-id="f1f3a-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="f1f3a-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="f1f3a-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1f3a-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="f1f3a-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1f3a-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="f1f3a-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f1f3a-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

