---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384058"
---
# <span data-ttu-id="fa456-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="fa456-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="fa456-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa456-102">SYNOPSIS</span></span>
<span data-ttu-id="fa456-103">Ottiene le informazioni sul nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="fa456-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="fa456-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa456-104">SYNTAX</span></span>

### <span data-ttu-id="fa456-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa456-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa456-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa456-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa456-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa456-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa456-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa456-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa456-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa456-109">DESCRIPTION</span></span>
<span data-ttu-id="fa456-110">Il cmdlet **Get-AzSynapseIntegrationRuntimeNode** ottiene le informazioni dettagliate di un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="fa456-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="fa456-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa456-111">EXAMPLES</span></span>

### <span data-ttu-id="fa456-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa456-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="fa456-113">Il cmdlet ottiene le informazioni del nodo denominato "Node_1" in self-hosted Integration Runtime "test-SelfHost-IR" nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="fa456-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="fa456-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fa456-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="fa456-115">Il cmdlet ottiene le informazioni del nodo denominato "Node_1" in self-hosted Integration Runtime "test-SelfHost-IR" nell'area di lavoro "test-DF-EU2", incluso l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="fa456-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="fa456-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa456-116">PARAMETERS</span></span>

### <span data-ttu-id="fa456-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa456-117">-DefaultProfile</span></span>
<span data-ttu-id="fa456-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa456-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa456-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa456-119">-InputObject</span></span>
<span data-ttu-id="fa456-120">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="fa456-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="fa456-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="fa456-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="fa456-122">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="fa456-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="fa456-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="fa456-123">-IpAddress</span></span>
<span data-ttu-id="fa456-124">Indirizzo IP del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="fa456-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="fa456-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa456-125">-Name</span></span>
<span data-ttu-id="fa456-126">Nome del nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="fa456-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="fa456-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa456-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa456-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fa456-128">Resource group name.</span></span>

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

### <span data-ttu-id="fa456-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa456-129">-ResourceId</span></span>
<span data-ttu-id="fa456-130">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="fa456-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="fa456-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fa456-131">-WorkspaceName</span></span>
<span data-ttu-id="fa456-132">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="fa456-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fa456-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fa456-133">-WorkspaceObject</span></span>
<span data-ttu-id="fa456-134">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="fa456-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fa456-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa456-135">CommonParameters</span></span>
<span data-ttu-id="fa456-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa456-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa456-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa456-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa456-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa456-138">INPUTS</span></span>

### <span data-ttu-id="fa456-139">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa456-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fa456-140">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fa456-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fa456-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa456-141">OUTPUTS</span></span>

### <span data-ttu-id="fa456-142">Microsoft. Azure. Commands. sinapsi. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="fa456-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="fa456-143">Microsoft. Azure. Commands. sinapsi. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="fa456-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="fa456-144">Note</span><span class="sxs-lookup"><span data-stu-id="fa456-144">NOTES</span></span>

## <span data-ttu-id="fa456-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa456-145">RELATED LINKS</span></span>
