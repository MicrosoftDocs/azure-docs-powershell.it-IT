---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182799"
---
# <span data-ttu-id="c2ab2-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="c2ab2-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="c2ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ab2-103">Ottiene le chiavi per un runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="c2ab2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2ab2-104">SYNTAX</span></span>

### <span data-ttu-id="c2ab2-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2ab2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2ab2-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ab2-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2ab2-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ab2-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2ab2-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ab2-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2ab2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c2ab2-109">DESCRIPTION</span></span>
<span data-ttu-id="c2ab2-110">Il cmdlet **Get-AzSynapseIntegrationRuntimeKey** ottiene le chiavi per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="c2ab2-111">Le chiavi vengono usate per registrare un nodo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="c2ab2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2ab2-112">EXAMPLES</span></span>

### <span data-ttu-id="c2ab2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2ab2-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="c2ab2-114">Il cmdlet recupera le chiavi per un runtime di integrazione denominato "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="c2ab2-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c2ab2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2ab2-115">PARAMETERS</span></span>

### <span data-ttu-id="c2ab2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ab2-116">-DefaultProfile</span></span>
<span data-ttu-id="c2ab2-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ab2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2ab2-118">-InputObject</span></span>
<span data-ttu-id="c2ab2-119">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="c2ab2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c2ab2-120">-Name</span></span>
<span data-ttu-id="c2ab2-121">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="c2ab2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ab2-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2ab2-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-123">Resource group name.</span></span>

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

### <span data-ttu-id="c2ab2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ab2-124">-ResourceId</span></span>
<span data-ttu-id="c2ab2-125">Identificatore di risorsa del runtime di integrazione synapse.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="c2ab2-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2ab2-126">-WorkspaceName</span></span>
<span data-ttu-id="c2ab2-127">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c2ab2-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2ab2-128">-WorkspaceObject</span></span>
<span data-ttu-id="c2ab2-129">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c2ab2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ab2-130">CommonParameters</span></span>
<span data-ttu-id="c2ab2-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ab2-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2ab2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ab2-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c2ab2-133">INPUTS</span></span>

### <span data-ttu-id="c2ab2-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2ab2-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c2ab2-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c2ab2-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c2ab2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2ab2-136">OUTPUTS</span></span>

### <span data-ttu-id="c2ab2-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="c2ab2-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="c2ab2-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c2ab2-138">NOTES</span></span>

## <span data-ttu-id="c2ab2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2ab2-139">RELATED LINKS</span></span>
