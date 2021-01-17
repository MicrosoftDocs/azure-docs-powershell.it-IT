---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359477"
---
# <span data-ttu-id="f3fb0-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f3fb0-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="f3fb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3fb0-103">Ottiene un pool di scintille di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f3fb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-104">SYNTAX</span></span>

### <span data-ttu-id="f3fb0-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3fb0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fb0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3fb0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fb0-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3fb0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3fb0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3fb0-108">DESCRIPTION</span></span>
<span data-ttu-id="f3fb0-109">Il cmdlet **Get-AzSynapseSparkPool** ottiene le informazioni su un pool di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f3fb0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-110">EXAMPLES</span></span>

### <span data-ttu-id="f3fb0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3fb0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f3fb0-112">Questo comando consente di ottenere tutti i pool di scintille in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="f3fb0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f3fb0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="f3fb0-114">Questo comando consente di ottenere il pool di scintille in area di lavoro ContosoWorkspace con nome ContosoSparkPool.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="f3fb0-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f3fb0-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="f3fb0-116">Questo comando consente di ottenere tutti i pool di scintille in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="f3fb0-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="f3fb0-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="f3fb0-118">Questo comando consente di ottenere il pool di scintille con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="f3fb0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-119">PARAMETERS</span></span>

### <span data-ttu-id="f3fb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fb0-120">-DefaultProfile</span></span>
<span data-ttu-id="f3fb0-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3fb0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3fb0-122">-Name</span></span>
<span data-ttu-id="f3fb0-123">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-123">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f3fb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3fb0-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-125">Resource group name.</span></span>

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

### <span data-ttu-id="f3fb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3fb0-126">-ResourceId</span></span>
<span data-ttu-id="f3fb0-127">Identificatore delle risorse del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-127">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="f3fb0-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3fb0-128">-WorkspaceName</span></span>
<span data-ttu-id="f3fb0-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f3fb0-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3fb0-130">-WorkspaceObject</span></span>
<span data-ttu-id="f3fb0-131">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f3fb0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fb0-132">CommonParameters</span></span>
<span data-ttu-id="f3fb0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fb0-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3fb0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fb0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-135">INPUTS</span></span>

### <span data-ttu-id="f3fb0-136">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3fb0-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f3fb0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3fb0-137">OUTPUTS</span></span>

### <span data-ttu-id="f3fb0-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f3fb0-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f3fb0-139">Note</span><span class="sxs-lookup"><span data-stu-id="f3fb0-139">NOTES</span></span>

## <span data-ttu-id="f3fb0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-140">RELATED LINKS</span></span>
