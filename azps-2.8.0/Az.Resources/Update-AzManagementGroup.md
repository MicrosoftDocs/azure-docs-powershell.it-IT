---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdccb01293f60c876470d2ac443c8e85f354e2d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854766"
---
# <span data-ttu-id="5a573-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5a573-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="5a573-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a573-102">SYNOPSIS</span></span>
<span data-ttu-id="5a573-103">Aggiorna un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a573-103">Updates a Management Group</span></span>

## <span data-ttu-id="5a573-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a573-104">SYNTAX</span></span>

### <span data-ttu-id="5a573-105">GroupOperations (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a573-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a573-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="5a573-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a573-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="5a573-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a573-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="5a573-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a573-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a573-109">DESCRIPTION</span></span>
<span data-ttu-id="5a573-110">Il cmdlet **Update-AzManagementGroup** aggiorna il **parentID** o **DisplayName** per un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="5a573-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="5a573-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a573-111">EXAMPLES</span></span>

### <span data-ttu-id="5a573-112">Esempio 1: aggiornare il nome visualizzato di un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a573-112">Example 1: Update a Management Group's Display Name</span></span>
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

### <span data-ttu-id="5a573-113">Esempio 2: aggiornare l'elemento padre di un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a573-113">Example 2: Update a Management Group's Parent</span></span>
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

### <span data-ttu-id="5a573-114">Esempio 3: aggiornare un gruppo di gestione eseguendo il piping di un oggetto PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5a573-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
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

### <span data-ttu-id="5a573-115">Esempio 4: aggiornare l'elemento padre di un gruppo di gestione con ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a573-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
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

## <span data-ttu-id="5a573-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a573-116">PARAMETERS</span></span>

### <span data-ttu-id="5a573-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a573-117">-DefaultProfile</span></span>
<span data-ttu-id="5a573-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a573-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a573-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a573-119">-DisplayName</span></span>
<span data-ttu-id="5a573-120">Nome visualizzato del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a573-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="5a573-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="5a573-121">-GroupName</span></span>
<span data-ttu-id="5a573-122">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a573-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a573-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a573-123">-InputObject</span></span>
<span data-ttu-id="5a573-124">Oggetto di input dalla chiamata Get</span><span class="sxs-lookup"><span data-stu-id="5a573-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="5a573-125">-ParentID</span><span class="sxs-lookup"><span data-stu-id="5a573-125">-ParentId</span></span>
<span data-ttu-id="5a573-126">ID padre del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a573-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="5a573-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a573-127">-ParentObject</span></span>
<span data-ttu-id="5a573-128">Oggetto di input dalla chiamata Get</span><span class="sxs-lookup"><span data-stu-id="5a573-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="5a573-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a573-129">-Confirm</span></span>
<span data-ttu-id="5a573-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a573-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a573-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a573-131">-WhatIf</span></span>
<span data-ttu-id="5a573-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a573-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a573-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a573-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a573-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a573-134">CommonParameters</span></span>
<span data-ttu-id="5a573-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a573-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a573-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a573-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a573-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a573-137">INPUTS</span></span>

### <span data-ttu-id="5a573-138">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5a573-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="5a573-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a573-139">OUTPUTS</span></span>

### <span data-ttu-id="5a573-140">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="5a573-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="5a573-141">Note</span><span class="sxs-lookup"><span data-stu-id="5a573-141">NOTES</span></span>

## <span data-ttu-id="5a573-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a573-142">RELATED LINKS</span></span>
