---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339208"
---
# <span data-ttu-id="93328-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="93328-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="93328-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93328-102">SYNOPSIS</span></span>
<span data-ttu-id="93328-103">Ottiene i dati metrici per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="93328-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="93328-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93328-104">SYNTAX</span></span>

### <span data-ttu-id="93328-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93328-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93328-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93328-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93328-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93328-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93328-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93328-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93328-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93328-109">DESCRIPTION</span></span>
<span data-ttu-id="93328-110">Il cmdlet **Get-AzSynapseIntegrationRuntimeMetric** ottiene i dati metrici relativi a Integration Runtime in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="93328-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="93328-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93328-111">EXAMPLES</span></span>

### <span data-ttu-id="93328-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93328-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="93328-113">Questo comando Visualizza i dati metrici relativi al runtime di integrazione denominato "test-SelfHost-IR" nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="93328-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="93328-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93328-114">PARAMETERS</span></span>

### <span data-ttu-id="93328-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93328-115">-DefaultProfile</span></span>
<span data-ttu-id="93328-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93328-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93328-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93328-117">-InputObject</span></span>
<span data-ttu-id="93328-118">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="93328-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93328-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="93328-119">-Name</span></span>
<span data-ttu-id="93328-120">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="93328-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93328-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93328-121">-ResourceGroupName</span></span>
<span data-ttu-id="93328-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93328-122">Resource group name.</span></span>

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

### <span data-ttu-id="93328-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93328-123">-ResourceId</span></span>
<span data-ttu-id="93328-124">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="93328-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="93328-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="93328-125">-WorkspaceName</span></span>
<span data-ttu-id="93328-126">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="93328-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="93328-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="93328-127">-WorkspaceObject</span></span>
<span data-ttu-id="93328-128">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="93328-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="93328-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93328-129">CommonParameters</span></span>
<span data-ttu-id="93328-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93328-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93328-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93328-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93328-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93328-132">INPUTS</span></span>

### <span data-ttu-id="93328-133">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="93328-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="93328-134">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="93328-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="93328-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93328-135">OUTPUTS</span></span>

### <span data-ttu-id="93328-136">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="93328-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="93328-137">Note</span><span class="sxs-lookup"><span data-stu-id="93328-137">NOTES</span></span>

## <span data-ttu-id="93328-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93328-138">RELATED LINKS</span></span>
