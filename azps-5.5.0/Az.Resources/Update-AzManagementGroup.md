---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdef58db8dcda735a7a8c08350b806c9fd00cf21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178686"
---
# <span data-ttu-id="9d47a-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9d47a-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="9d47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d47a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d47a-103">Aggiorna un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9d47a-103">Updates a Management Group</span></span>

## <span data-ttu-id="9d47a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d47a-104">SYNTAX</span></span>

### <span data-ttu-id="9d47a-105">GroupOperations (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d47a-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d47a-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="9d47a-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d47a-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="9d47a-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d47a-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="9d47a-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d47a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d47a-109">DESCRIPTION</span></span>
<span data-ttu-id="9d47a-110">Il cmdlet **Update-AzManagementGroup** aggiorna **ParentId** o **DisplayName** per un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="9d47a-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="9d47a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d47a-111">EXAMPLES</span></span>

### <span data-ttu-id="9d47a-112">Esempio 1: Aggiornare il nome visualizzato di un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9d47a-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="9d47a-113">Esempio 2: Aggiornare il padre di un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9d47a-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="9d47a-114">Esempio 3: Aggiornare un gruppo di gestione con l'oggetto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9d47a-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="9d47a-115">Esempio 4: Aggiornare l'elemento padre di un gruppo di gestione usando ParentObject</span><span class="sxs-lookup"><span data-stu-id="9d47a-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="9d47a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d47a-116">PARAMETERS</span></span>

### <span data-ttu-id="9d47a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d47a-117">-DefaultProfile</span></span>
<span data-ttu-id="9d47a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d47a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d47a-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9d47a-119">-DisplayName</span></span>
<span data-ttu-id="9d47a-120">Nome visualizzato del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9d47a-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="9d47a-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="9d47a-121">-GroupName</span></span>
<span data-ttu-id="9d47a-122">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9d47a-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d47a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d47a-123">-InputObject</span></span>
<span data-ttu-id="9d47a-124">Oggetto di input dalla chiamata Get</span><span class="sxs-lookup"><span data-stu-id="9d47a-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d47a-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="9d47a-125">-ParentId</span></span>
<span data-ttu-id="9d47a-126">ID padre del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9d47a-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d47a-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9d47a-127">-ParentObject</span></span>
<span data-ttu-id="9d47a-128">Oggetto di input dalla chiamata Get</span><span class="sxs-lookup"><span data-stu-id="9d47a-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d47a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d47a-129">-Confirm</span></span>
<span data-ttu-id="9d47a-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d47a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d47a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d47a-131">-WhatIf</span></span>
<span data-ttu-id="9d47a-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d47a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d47a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d47a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d47a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d47a-134">CommonParameters</span></span>
<span data-ttu-id="9d47a-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d47a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d47a-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d47a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d47a-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d47a-137">INPUTS</span></span>

### <span data-ttu-id="9d47a-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9d47a-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="9d47a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d47a-139">OUTPUTS</span></span>

### <span data-ttu-id="9d47a-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9d47a-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="9d47a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d47a-141">NOTES</span></span>

## <span data-ttu-id="9d47a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d47a-142">RELATED LINKS</span></span>
