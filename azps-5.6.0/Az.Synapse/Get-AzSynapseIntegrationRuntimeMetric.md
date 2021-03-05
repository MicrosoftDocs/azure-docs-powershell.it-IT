---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 158d4a54cdbeec0dd8cf756a3c685aede97f5bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994740"
---
# <span data-ttu-id="6c686-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="6c686-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="6c686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c686-102">SYNOPSIS</span></span>
<span data-ttu-id="6c686-103">Recupera i dati della metrica per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6c686-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="6c686-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c686-104">SYNTAX</span></span>

### <span data-ttu-id="6c686-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c686-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c686-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c686-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c686-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c686-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c686-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c686-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c686-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c686-109">DESCRIPTION</span></span>
<span data-ttu-id="6c686-110">Il cmdlet **Get-AzSynapseIntegrationRuntimeMetric** ottiene i dati della metrica sul runtime di integrazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6c686-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="6c686-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c686-111">EXAMPLES</span></span>

### <span data-ttu-id="6c686-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c686-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="6c686-113">Questo comando visualizza i dati di metrica relativi al runtime di integrazione denominato "test-selfhost-ir" nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6c686-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="6c686-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c686-114">PARAMETERS</span></span>

### <span data-ttu-id="6c686-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c686-115">-DefaultProfile</span></span>
<span data-ttu-id="6c686-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c686-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c686-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c686-117">-InputObject</span></span>
<span data-ttu-id="6c686-118">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6c686-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="6c686-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6c686-119">-Name</span></span>
<span data-ttu-id="6c686-120">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="6c686-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="6c686-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c686-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c686-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c686-122">Resource group name.</span></span>

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

### <span data-ttu-id="6c686-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c686-123">-ResourceId</span></span>
<span data-ttu-id="6c686-124">Identificatore di risorsa del runtime di integrazione di Synapse.</span><span class="sxs-lookup"><span data-stu-id="6c686-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6c686-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6c686-125">-WorkspaceName</span></span>
<span data-ttu-id="6c686-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="6c686-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6c686-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6c686-127">-WorkspaceObject</span></span>
<span data-ttu-id="6c686-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c686-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6c686-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c686-129">CommonParameters</span></span>
<span data-ttu-id="6c686-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c686-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c686-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c686-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c686-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c686-132">INPUTS</span></span>

### <span data-ttu-id="6c686-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c686-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6c686-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6c686-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6c686-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c686-135">OUTPUTS</span></span>

### <span data-ttu-id="6c686-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="6c686-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="6c686-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c686-137">NOTES</span></span>

## <span data-ttu-id="6c686-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c686-138">RELATED LINKS</span></span>
