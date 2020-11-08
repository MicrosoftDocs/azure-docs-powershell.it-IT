---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94030941"
---
# <span data-ttu-id="07f15-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="07f15-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="07f15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07f15-102">SYNOPSIS</span></span>
<span data-ttu-id="07f15-103">Ottiene un pool di scintille di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="07f15-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="07f15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07f15-104">SYNTAX</span></span>

### <span data-ttu-id="07f15-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07f15-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f15-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f15-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f15-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f15-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f15-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07f15-108">DESCRIPTION</span></span>
<span data-ttu-id="07f15-109">Il cmdlet **Get-AzSynapseSparkPool** ottiene le informazioni su un pool di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="07f15-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="07f15-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07f15-110">EXAMPLES</span></span>

### <span data-ttu-id="07f15-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07f15-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="07f15-112">Questo comando consente di ottenere tutti i pool di scintille in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="07f15-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="07f15-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="07f15-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="07f15-114">Questo comando consente di ottenere il pool di scintille in area di lavoro ContosoWorkspace con nome ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="07f15-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="07f15-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="07f15-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="07f15-116">Questo comando consente di ottenere tutti i pool di scintille in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="07f15-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="07f15-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="07f15-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="07f15-118">Questo comando consente di ottenere il pool di scintille con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="07f15-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="07f15-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07f15-119">PARAMETERS</span></span>

### <span data-ttu-id="07f15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f15-120">-DefaultProfile</span></span>
<span data-ttu-id="07f15-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07f15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f15-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="07f15-122">-Name</span></span>
<span data-ttu-id="07f15-123">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="07f15-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="07f15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f15-124">-ResourceGroupName</span></span>
<span data-ttu-id="07f15-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07f15-125">Resource group name.</span></span>

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

### <span data-ttu-id="07f15-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f15-126">-ResourceId</span></span>
<span data-ttu-id="07f15-127">Identificatore delle risorse del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="07f15-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="07f15-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07f15-128">-WorkspaceName</span></span>
<span data-ttu-id="07f15-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="07f15-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="07f15-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="07f15-130">-WorkspaceObject</span></span>
<span data-ttu-id="07f15-131">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="07f15-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="07f15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f15-132">CommonParameters</span></span>
<span data-ttu-id="07f15-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f15-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f15-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f15-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07f15-135">INPUTS</span></span>

### <span data-ttu-id="07f15-136">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07f15-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="07f15-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07f15-137">OUTPUTS</span></span>

### <span data-ttu-id="07f15-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="07f15-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="07f15-139">Note</span><span class="sxs-lookup"><span data-stu-id="07f15-139">NOTES</span></span>

## <span data-ttu-id="07f15-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07f15-140">RELATED LINKS</span></span>
