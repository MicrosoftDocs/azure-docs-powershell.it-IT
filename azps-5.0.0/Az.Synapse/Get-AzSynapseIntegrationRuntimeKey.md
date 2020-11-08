---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193954"
---
# <span data-ttu-id="f4974-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f4974-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="f4974-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4974-102">SYNOPSIS</span></span>
<span data-ttu-id="f4974-103">Ottiene le chiavi per un runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="f4974-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="f4974-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4974-104">SYNTAX</span></span>

### <span data-ttu-id="f4974-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4974-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4974-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4974-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4974-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4974-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4974-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4974-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4974-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4974-109">DESCRIPTION</span></span>
<span data-ttu-id="f4974-110">Il cmdlet **Get-AzSynapseIntegrationRuntimeKey** ottiene le chiavi per un runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f4974-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="f4974-111">I tasti vengono usati per registrare un nodo runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="f4974-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="f4974-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4974-112">EXAMPLES</span></span>

### <span data-ttu-id="f4974-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4974-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="f4974-114">Il cmdlet recupera le chiavi per un runtime di integrazione denominato "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="f4974-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f4974-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4974-115">PARAMETERS</span></span>

### <span data-ttu-id="f4974-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4974-116">-DefaultProfile</span></span>
<span data-ttu-id="f4974-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4974-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4974-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4974-118">-InputObject</span></span>
<span data-ttu-id="f4974-119">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="f4974-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="f4974-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4974-120">-Name</span></span>
<span data-ttu-id="f4974-121">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="f4974-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="f4974-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4974-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4974-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4974-123">Resource group name.</span></span>

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

### <span data-ttu-id="f4974-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4974-124">-ResourceId</span></span>
<span data-ttu-id="f4974-125">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f4974-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="f4974-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f4974-126">-WorkspaceName</span></span>
<span data-ttu-id="f4974-127">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f4974-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f4974-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f4974-128">-WorkspaceObject</span></span>
<span data-ttu-id="f4974-129">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4974-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f4974-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4974-130">CommonParameters</span></span>
<span data-ttu-id="f4974-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4974-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4974-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4974-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4974-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4974-133">INPUTS</span></span>

### <span data-ttu-id="f4974-134">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f4974-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f4974-135">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f4974-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f4974-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4974-136">OUTPUTS</span></span>

### <span data-ttu-id="f4974-137">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="f4974-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="f4974-138">Note</span><span class="sxs-lookup"><span data-stu-id="f4974-138">NOTES</span></span>

## <span data-ttu-id="f4974-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4974-139">RELATED LINKS</span></span>
