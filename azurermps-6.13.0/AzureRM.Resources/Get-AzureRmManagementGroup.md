---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
ms.openlocfilehash: 275b13efa25bbffd2c104a1e9cfa3baf04fffe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686595"
---
# <span data-ttu-id="9f80d-101">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9f80d-101">Get-AzureRmManagementGroup</span></span>

## <span data-ttu-id="9f80d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f80d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f80d-103">Ottiene i gruppi di gestione</span><span class="sxs-lookup"><span data-stu-id="9f80d-103">Gets Management Group(s)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f80d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f80d-104">SYNTAX</span></span>

### <span data-ttu-id="9f80d-105">ListOperation (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f80d-105">ListOperation (Default)</span></span>
```
Get-AzureRmManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f80d-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="9f80d-106">GetOperation</span></span>
```
Get-AzureRmManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand]
 [-Recurse] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f80d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f80d-107">DESCRIPTION</span></span>
<span data-ttu-id="9f80d-108">Il cmdlet Get-AzureRMManagementGroup ottiene tutti o un gruppo di gestione specifico.</span><span class="sxs-lookup"><span data-stu-id="9f80d-108">The Get-AzureRMManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="9f80d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f80d-109">EXAMPLES</span></span>

### <span data-ttu-id="9f80d-110">Esempio 1: ottenere tutti i gruppi di gestione</span><span class="sxs-lookup"><span data-stu-id="9f80d-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzureRmManagementGroup

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

### <span data-ttu-id="9f80d-111">Esempio 2: ottenere un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="9f80d-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzureRmManagementGroup -GroupName TestGroup

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

### <span data-ttu-id="9f80d-112">Esempio 3: ottenere un gruppo di gestione specifico e un primo livello di gerarchia</span><span class="sxs-lookup"><span data-stu-id="9f80d-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand
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

<span data-ttu-id="9f80d-113">Con il `Expand` contrassegno, si può esplorare la `Children` matrice e ottenere i dettagli per ogni bambino.</span><span class="sxs-lookup"><span data-stu-id="9f80d-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="9f80d-114">Ad esempio, fornirà i `Children[0]` Dettagli per il gruppo con il nome visualizzato `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="9f80d-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="9f80d-115">Esempio 4: ottenere un gruppo di gestione specifico e tutti i livelli di tonde</span><span class="sxs-lookup"><span data-stu-id="9f80d-115">Example 4: Get specific Management Group and all levels of hiearchy</span></span>
```
PS C:\> $response = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand -Recurse
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

## <span data-ttu-id="9f80d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f80d-116">PARAMETERS</span></span>

### <span data-ttu-id="9f80d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f80d-117">-DefaultProfile</span></span>
<span data-ttu-id="9f80d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f80d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f80d-119">-Espandi</span><span class="sxs-lookup"><span data-stu-id="9f80d-119">-Expand</span></span>
<span data-ttu-id="9f80d-120">Espandere l'output per elencare gli elementi figlio del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9f80d-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="9f80d-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="9f80d-121">-GroupName</span></span>
<span data-ttu-id="9f80d-122">ID gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9f80d-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f80d-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="9f80d-123">-Recurse</span></span>
<span data-ttu-id="9f80d-124">Elenca ricorsivamente gli elementi figlio del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="9f80d-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="9f80d-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f80d-125">-Confirm</span></span>
<span data-ttu-id="9f80d-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f80d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f80d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f80d-127">-WhatIf</span></span>
<span data-ttu-id="9f80d-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f80d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f80d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f80d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f80d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f80d-130">CommonParameters</span></span>
<span data-ttu-id="9f80d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f80d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f80d-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f80d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f80d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f80d-133">INPUTS</span></span>

### <span data-ttu-id="9f80d-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9f80d-134">None</span></span>

## <span data-ttu-id="9f80d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f80d-135">OUTPUTS</span></span>

### <span data-ttu-id="9f80d-136">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="9f80d-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="9f80d-137">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9f80d-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="9f80d-138">Note</span><span class="sxs-lookup"><span data-stu-id="9f80d-138">NOTES</span></span>

## <span data-ttu-id="9f80d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f80d-139">RELATED LINKS</span></span>