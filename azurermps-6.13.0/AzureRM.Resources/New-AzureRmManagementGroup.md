---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
ms.openlocfilehash: 20cfc2ef6b4b59e8cdd605dd14302aa1a172acb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507320"
---
# <span data-ttu-id="8e99c-101">New-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e99c-101">New-AzureRmManagementGroup</span></span>

## <span data-ttu-id="8e99c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e99c-102">SYNOPSIS</span></span>
<span data-ttu-id="8e99c-103">Crea un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8e99c-103">Creates a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e99c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e99c-104">SYNTAX</span></span>

### <span data-ttu-id="8e99c-105">GroupOperations (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e99c-105">GroupOperations (Default)</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e99c-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="8e99c-106">ParentGroupObject</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e99c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e99c-107">DESCRIPTION</span></span>
<span data-ttu-id="8e99c-108">Il cmdlet **New-AzureRMManagementGroup** crea un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="8e99c-108">The **New-AzureRMManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="8e99c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e99c-109">EXAMPLES</span></span>

### <span data-ttu-id="8e99c-110">Esempio 1: creare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8e99c-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="8e99c-111">Creazione di un nuovo gruppo con `DisplayName` e `ParentId` impostato su `null` .</span><span class="sxs-lookup"><span data-stu-id="8e99c-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="8e99c-112">L'oggetto `DisplayName` sarà uguale a `GroupName` e il padre del gruppo sarà il tenant.</span><span class="sxs-lookup"><span data-stu-id="8e99c-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="8e99c-113">Esempio 2: creare un gruppo di gestione con un nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="8e99c-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="8e99c-114">In questo caso, l'elemento padre del gruppo sarà il tenant e l' `DisplayName` impostazione verrà impostata sul valore assegnato.</span><span class="sxs-lookup"><span data-stu-id="8e99c-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="8e99c-115">Esempio 3: creare un gruppo di gestione con un elemento padre e un nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="8e99c-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="8e99c-116">Esempio 4: creare un gruppo di gestione con un elemento padre (tramite un oggetto padre)</span><span class="sxs-lookup"><span data-stu-id="8e99c-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzureRmManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="8e99c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e99c-117">PARAMETERS</span></span>

### <span data-ttu-id="8e99c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e99c-118">-DefaultProfile</span></span>
<span data-ttu-id="8e99c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e99c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e99c-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e99c-120">-DisplayName</span></span>
<span data-ttu-id="8e99c-121">Nome visualizzato del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8e99c-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="8e99c-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="8e99c-122">-GroupName</span></span>
<span data-ttu-id="8e99c-123">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8e99c-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e99c-124">-ParentID</span><span class="sxs-lookup"><span data-stu-id="8e99c-124">-ParentId</span></span>
<span data-ttu-id="8e99c-125">ID padre del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8e99c-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e99c-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e99c-126">-ParentObject</span></span>
<span data-ttu-id="8e99c-127">Oggetto padre</span><span class="sxs-lookup"><span data-stu-id="8e99c-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e99c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e99c-128">-Confirm</span></span>
<span data-ttu-id="8e99c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e99c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e99c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e99c-130">-WhatIf</span></span>
<span data-ttu-id="8e99c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e99c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e99c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e99c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e99c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e99c-133">CommonParameters</span></span>
<span data-ttu-id="8e99c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e99c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e99c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e99c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e99c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e99c-136">INPUTS</span></span>

### <span data-ttu-id="8e99c-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8e99c-137">None</span></span>

## <span data-ttu-id="8e99c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e99c-138">OUTPUTS</span></span>

### <span data-ttu-id="8e99c-139">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e99c-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="8e99c-140">Note</span><span class="sxs-lookup"><span data-stu-id="8e99c-140">NOTES</span></span>

## <span data-ttu-id="8e99c-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e99c-141">RELATED LINKS</span></span>

[<span data-ttu-id="8e99c-142">Remove-AzureRMManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e99c-142">Remove-AzureRMManagementGroup</span></span>](./Remove-AzureRMManagementGroup.md)

[<span data-ttu-id="8e99c-143">Update-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e99c-143">Update-AzureRmManagementGroup</span></span>](./Update-AzureRmManagementGroup.md)

[<span data-ttu-id="8e99c-144">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e99c-144">Get-AzureRmManagementGroup</span></span>](./Get-AzureRmManagementGroup.md)
