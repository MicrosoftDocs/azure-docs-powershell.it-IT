---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 07272df9b1892373d23b89447f1c21a5a4fb53c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183679"
---
# <span data-ttu-id="0c72f-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0c72f-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="0c72f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c72f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c72f-103">Crea un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="0c72f-103">Creates a Management Group</span></span>

## <span data-ttu-id="0c72f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c72f-104">SYNTAX</span></span>

### <span data-ttu-id="0c72f-105">GroupOperations (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c72f-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c72f-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="0c72f-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c72f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0c72f-107">DESCRIPTION</span></span>
<span data-ttu-id="0c72f-108">Il cmdlet **New-AzManagementGroup** crea un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="0c72f-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="0c72f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c72f-109">EXAMPLES</span></span>

### <span data-ttu-id="0c72f-110">Esempio 1: Creare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="0c72f-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

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

<span data-ttu-id="0c72f-111">Creazione di un nuovo gruppo con `DisplayName` e `ParentId` impostato su `null` .</span><span class="sxs-lookup"><span data-stu-id="0c72f-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="0c72f-112">Il tenant sarà uguale a quello del gruppo e il padre del `DisplayName` `GroupName` gruppo sarà il tenant.</span><span class="sxs-lookup"><span data-stu-id="0c72f-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="0c72f-113">Esempio 2: Creare un gruppo di gestione con un nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="0c72f-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

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

<span data-ttu-id="0c72f-114">In questo caso, l'elemento padre del gruppo sarà il tenant e sarà `DisplayName` impostato sul valore assegnato.</span><span class="sxs-lookup"><span data-stu-id="0c72f-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="0c72f-115">Esempio 3: Creare un gruppo di gestione con un padre e un nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="0c72f-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="0c72f-116">Esempio 4: Creare un gruppo di gestione con un oggetto padre (usando un oggetto padre)</span><span class="sxs-lookup"><span data-stu-id="0c72f-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="0c72f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c72f-117">PARAMETERS</span></span>

### <span data-ttu-id="0c72f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c72f-118">-DefaultProfile</span></span>
<span data-ttu-id="0c72f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c72f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c72f-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c72f-120">-DisplayName</span></span>
<span data-ttu-id="0c72f-121">Nome visualizzato del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="0c72f-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="0c72f-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="0c72f-122">-GroupName</span></span>
<span data-ttu-id="0c72f-123">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="0c72f-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c72f-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="0c72f-124">-ParentId</span></span>
<span data-ttu-id="0c72f-125">ID padre del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="0c72f-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="0c72f-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0c72f-126">-ParentObject</span></span>
<span data-ttu-id="0c72f-127">Oggetto padre</span><span class="sxs-lookup"><span data-stu-id="0c72f-127">Parent Object</span></span>

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

### <span data-ttu-id="0c72f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c72f-128">-Confirm</span></span>
<span data-ttu-id="0c72f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c72f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c72f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c72f-130">-WhatIf</span></span>
<span data-ttu-id="0c72f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c72f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c72f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c72f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c72f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c72f-133">CommonParameters</span></span>
<span data-ttu-id="0c72f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c72f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c72f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c72f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c72f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0c72f-136">INPUTS</span></span>

### <span data-ttu-id="0c72f-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c72f-137">None</span></span>

## <span data-ttu-id="0c72f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c72f-138">OUTPUTS</span></span>

### <span data-ttu-id="0c72f-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0c72f-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="0c72f-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="0c72f-140">NOTES</span></span>

## <span data-ttu-id="0c72f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c72f-141">RELATED LINKS</span></span>

[<span data-ttu-id="0c72f-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0c72f-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="0c72f-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0c72f-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="0c72f-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0c72f-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)