---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: 48ecf7e0c840ca5054e19a250bc53d95de82c08d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015742"
---
# <span data-ttu-id="43d44-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="43d44-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="43d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d44-102">SYNOPSIS</span></span>
<span data-ttu-id="43d44-103">Ottiene un pool Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="43d44-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="43d44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43d44-104">SYNTAX</span></span>

### <span data-ttu-id="43d44-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43d44-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43d44-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43d44-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43d44-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43d44-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43d44-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43d44-108">DESCRIPTION</span></span>
<span data-ttu-id="43d44-109">Il cmdlet **Get-AzSynapseSparkPool** ottiene informazioni su un pool Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="43d44-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="43d44-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43d44-110">EXAMPLES</span></span>

### <span data-ttu-id="43d44-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43d44-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="43d44-112">Questo comando recupera tutti i pool di grafici Spark in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="43d44-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="43d44-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="43d44-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="43d44-114">Questo comando recupera il pool Spark nell'area di lavoro ContosoWorkspace con il nome ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="43d44-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="43d44-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="43d44-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="43d44-116">Questo comando recupera tutti i pool Spark in un'area di lavoro tramite una pipeline.</span><span class="sxs-lookup"><span data-stu-id="43d44-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="43d44-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="43d44-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="43d44-118">Questo comando recupera il pool Spark con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="43d44-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="43d44-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d44-119">PARAMETERS</span></span>

### <span data-ttu-id="43d44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d44-120">-DefaultProfile</span></span>
<span data-ttu-id="43d44-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43d44-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d44-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43d44-122">-Name</span></span>
<span data-ttu-id="43d44-123">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="43d44-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d44-124">-ResourceGroupName</span></span>
<span data-ttu-id="43d44-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43d44-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d44-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43d44-126">-ResourceId</span></span>
<span data-ttu-id="43d44-127">Identificatore di risorsa del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="43d44-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d44-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="43d44-128">-WorkspaceName</span></span>
<span data-ttu-id="43d44-129">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="43d44-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d44-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="43d44-130">-WorkspaceObject</span></span>
<span data-ttu-id="43d44-131">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="43d44-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43d44-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d44-132">CommonParameters</span></span>
<span data-ttu-id="43d44-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d44-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d44-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43d44-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d44-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="43d44-135">INPUTS</span></span>

### <span data-ttu-id="43d44-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="43d44-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="43d44-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43d44-137">OUTPUTS</span></span>

### <span data-ttu-id="43d44-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="43d44-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="43d44-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="43d44-139">NOTES</span></span>

## <span data-ttu-id="43d44-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43d44-140">RELATED LINKS</span></span>
