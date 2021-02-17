---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: f21a6d641e06916ce70c71338b539ef0909db6de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178815"
---
# <span data-ttu-id="255ae-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="255ae-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="255ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="255ae-102">SYNOPSIS</span></span>
<span data-ttu-id="255ae-103">Ottiene i gruppi di gestione</span><span class="sxs-lookup"><span data-stu-id="255ae-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="255ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="255ae-104">SYNTAX</span></span>

### <span data-ttu-id="255ae-105">ListOperation (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="255ae-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="255ae-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="255ae-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="255ae-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="255ae-107">DESCRIPTION</span></span>
<span data-ttu-id="255ae-108">Il Get-AzManagementGroup cmdlet di gestione ottiene tutto o un gruppo di gestione specifico.</span><span class="sxs-lookup"><span data-stu-id="255ae-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="255ae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="255ae-109">EXAMPLES</span></span>

### <span data-ttu-id="255ae-110">Esempio 1: Ottenere tutti i gruppi di gestione</span><span class="sxs-lookup"><span data-stu-id="255ae-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="255ae-111">Esempio 2: Ottenere un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="255ae-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="255ae-112">Esempio 3: Ottenere un gruppo di gestione specifico e il primo livello di gerarchia</span><span class="sxs-lookup"><span data-stu-id="255ae-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="255ae-113">Con il `Expand` contrassegno, è possibile spostarsi nella `Children` matrice e ottenere i dettagli per ogni elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="255ae-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="255ae-114">Ad esempio, `Children[0]` verranno fornite informazioni dettagliate sul gruppo con il nome `TestGroup1DisplayName` visualizzato.</span><span class="sxs-lookup"><span data-stu-id="255ae-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="255ae-115">Esempio 4: Ottenere un gruppo di gestione specifico e tutti i livelli di gerarchia</span><span class="sxs-lookup"><span data-stu-id="255ae-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="255ae-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="255ae-116">PARAMETERS</span></span>

### <span data-ttu-id="255ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255ae-117">-DefaultProfile</span></span>
<span data-ttu-id="255ae-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="255ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="255ae-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="255ae-119">-Expand</span></span>
<span data-ttu-id="255ae-120">Espandere l'output per elencare gli elementi figlio del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="255ae-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255ae-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="255ae-121">-GroupName</span></span>
<span data-ttu-id="255ae-122">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="255ae-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255ae-123">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="255ae-123">-Recurse</span></span>
<span data-ttu-id="255ae-124">Elencare in modo ricorsivo gli elementi figlio del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="255ae-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255ae-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="255ae-125">-Confirm</span></span>
<span data-ttu-id="255ae-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="255ae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="255ae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="255ae-127">-WhatIf</span></span>
<span data-ttu-id="255ae-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="255ae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="255ae-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="255ae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="255ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255ae-130">CommonParameters</span></span>
<span data-ttu-id="255ae-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255ae-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="255ae-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255ae-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="255ae-133">INPUTS</span></span>

### <span data-ttu-id="255ae-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="255ae-134">None</span></span>

## <span data-ttu-id="255ae-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="255ae-135">OUTPUTS</span></span>

### <span data-ttu-id="255ae-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="255ae-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="255ae-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="255ae-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="255ae-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="255ae-138">NOTES</span></span>

## <span data-ttu-id="255ae-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="255ae-139">RELATED LINKS</span></span>
