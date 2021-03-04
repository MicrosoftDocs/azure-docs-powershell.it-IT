---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: dbd791b3ab77889e8c78279b576b614c4d86b4b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994739"
---
# <span data-ttu-id="1e6a1-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1e6a1-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="1e6a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6a1-103">Recupera le informazioni sul nodo di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="1e6a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e6a1-104">SYNTAX</span></span>

### <span data-ttu-id="1e6a1-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e6a1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e6a1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6a1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6a1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6a1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6a1-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6a1-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e6a1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e6a1-109">DESCRIPTION</span></span>
<span data-ttu-id="1e6a1-110">Il cmdlet **Get-AzSynapseIntegrationRuntimeNode** ottiene le informazioni dettagliate di un nodo di runtime dell'integrazione.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="1e6a1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e6a1-111">EXAMPLES</span></span>

### <span data-ttu-id="1e6a1-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e6a1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="1e6a1-113">Il cmdlet ottiene le informazioni sul nodo denominato "Node_1" nel runtime di integrazione self-hosted 'test-selfhost-ir' nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="1e6a1-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1e6a1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="1e6a1-115">Il cmdlet ottiene informazioni sul nodo denominato "Node_1" nel runtime di integrazione self-hosted 'test-selfhost-ir' nell'area di lavoro 'test-df-eu2', incluso l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="1e6a1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e6a1-116">PARAMETERS</span></span>

### <span data-ttu-id="1e6a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6a1-117">-DefaultProfile</span></span>
<span data-ttu-id="1e6a1-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e6a1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e6a1-119">-InputObject</span></span>
<span data-ttu-id="1e6a1-120">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="1e6a1-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1e6a1-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="1e6a1-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a1-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="1e6a1-123">-IpAddress</span></span>
<span data-ttu-id="1e6a1-124">Indirizzo IP del nodo di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-124">The IP Address of integration runtime node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1e6a1-125">-Name</span></span>
<span data-ttu-id="1e6a1-126">Nome del nodo di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6a1-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e6a1-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-128">Resource group name.</span></span>

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

### <span data-ttu-id="1e6a1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e6a1-129">-ResourceId</span></span>
<span data-ttu-id="1e6a1-130">Identificatore di risorsa del runtime di integrazione di Synapse.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="1e6a1-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e6a1-131">-WorkspaceName</span></span>
<span data-ttu-id="1e6a1-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1e6a1-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1e6a1-133">-WorkspaceObject</span></span>
<span data-ttu-id="1e6a1-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1e6a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6a1-135">CommonParameters</span></span>
<span data-ttu-id="1e6a1-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6a1-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e6a1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6a1-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e6a1-138">INPUTS</span></span>

### <span data-ttu-id="1e6a1-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e6a1-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1e6a1-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e6a1-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1e6a1-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e6a1-141">OUTPUTS</span></span>

### <span data-ttu-id="1e6a1-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1e6a1-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="1e6a1-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1e6a1-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="1e6a1-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e6a1-144">NOTES</span></span>

## <span data-ttu-id="1e6a1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e6a1-145">RELATED LINKS</span></span>
