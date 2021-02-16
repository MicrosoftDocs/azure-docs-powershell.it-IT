---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195631"
---
# <span data-ttu-id="19f99-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="19f99-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="19f99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19f99-102">SYNOPSIS</span></span>
<span data-ttu-id="19f99-103">Recupera i dati della metrica per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="19f99-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="19f99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19f99-104">SYNTAX</span></span>

### <span data-ttu-id="19f99-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19f99-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19f99-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f99-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19f99-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f99-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19f99-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19f99-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19f99-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="19f99-109">DESCRIPTION</span></span>
<span data-ttu-id="19f99-110">Il cmdlet **Get-AzSynapseIntegrationRuntimeMetric** ottiene i dati della metrica sul runtime di integrazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19f99-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="19f99-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19f99-111">EXAMPLES</span></span>

### <span data-ttu-id="19f99-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19f99-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="19f99-113">Questo comando visualizza i dati di metrica relativi al runtime di integrazione denominato "test-selfhost-ir" nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="19f99-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="19f99-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19f99-114">PARAMETERS</span></span>

### <span data-ttu-id="19f99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f99-115">-DefaultProfile</span></span>
<span data-ttu-id="19f99-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19f99-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19f99-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19f99-117">-InputObject</span></span>
<span data-ttu-id="19f99-118">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="19f99-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="19f99-119">-Name</span><span class="sxs-lookup"><span data-stu-id="19f99-119">-Name</span></span>
<span data-ttu-id="19f99-120">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="19f99-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="19f99-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19f99-121">-ResourceGroupName</span></span>
<span data-ttu-id="19f99-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="19f99-122">Resource group name.</span></span>

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

### <span data-ttu-id="19f99-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19f99-123">-ResourceId</span></span>
<span data-ttu-id="19f99-124">Identificatore di risorsa del runtime di integrazione synapse.</span><span class="sxs-lookup"><span data-stu-id="19f99-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="19f99-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="19f99-125">-WorkspaceName</span></span>
<span data-ttu-id="19f99-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="19f99-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="19f99-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="19f99-127">-WorkspaceObject</span></span>
<span data-ttu-id="19f99-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="19f99-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="19f99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f99-129">CommonParameters</span></span>
<span data-ttu-id="19f99-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f99-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="19f99-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f99-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="19f99-132">INPUTS</span></span>

### <span data-ttu-id="19f99-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="19f99-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="19f99-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="19f99-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="19f99-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19f99-135">OUTPUTS</span></span>

### <span data-ttu-id="19f99-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="19f99-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="19f99-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="19f99-137">NOTES</span></span>

## <span data-ttu-id="19f99-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19f99-138">RELATED LINKS</span></span>
