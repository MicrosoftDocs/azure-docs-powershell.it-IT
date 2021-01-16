---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339247"
---
# <span data-ttu-id="1676b-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1676b-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="1676b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1676b-102">SYNOPSIS</span></span>
<span data-ttu-id="1676b-103">Ottiene informazioni sulle risorse di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="1676b-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="1676b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1676b-104">SYNTAX</span></span>

### <span data-ttu-id="1676b-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1676b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1676b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1676b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1676b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1676b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1676b-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1676b-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1676b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1676b-109">DESCRIPTION</span></span>
<span data-ttu-id="1676b-110">Il cmdlet **Get-AzSynapseIntegrationRuntime** ottiene le informazioni sui runtime di integrazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1676b-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="1676b-111">Se specifichi il nome di un runtime di integrazione, questo cmdlet ottiene le informazioni su tale runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1676b-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="1676b-112">Se non specifichi un nome, questo cmdlet recupera informazioni su tutti i runtime di integrazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1676b-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="1676b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1676b-113">EXAMPLES</span></span>

### <span data-ttu-id="1676b-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1676b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1676b-115">Elenca tutti i runtime di integrazione nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1676b-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1676b-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1676b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="1676b-117">Questo comando Visualizza le informazioni sul runtime di integrazione denominato "test-SelfHost-IR" nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1676b-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="1676b-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1676b-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="1676b-119">Questo comando Visualizza lo stato dei dettagli relativi al runtime di integrazione denominato "test-SelfHost-IR" nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1676b-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1676b-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1676b-120">PARAMETERS</span></span>

### <span data-ttu-id="1676b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1676b-121">-DefaultProfile</span></span>
<span data-ttu-id="1676b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1676b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1676b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1676b-123">-InputObject</span></span>
<span data-ttu-id="1676b-124">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="1676b-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="1676b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1676b-125">-Name</span></span>
<span data-ttu-id="1676b-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1676b-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1676b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1676b-127">-ResourceGroupName</span></span>
<span data-ttu-id="1676b-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1676b-128">Resource group name.</span></span>

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

### <span data-ttu-id="1676b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1676b-129">-ResourceId</span></span>
<span data-ttu-id="1676b-130">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="1676b-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="1676b-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="1676b-131">-Status</span></span>
<span data-ttu-id="1676b-132">Stato di dettaglio di Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="1676b-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="1676b-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1676b-133">-WorkspaceName</span></span>
<span data-ttu-id="1676b-134">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="1676b-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1676b-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1676b-135">-WorkspaceObject</span></span>
<span data-ttu-id="1676b-136">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1676b-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1676b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1676b-137">CommonParameters</span></span>
<span data-ttu-id="1676b-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1676b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1676b-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1676b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1676b-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1676b-140">INPUTS</span></span>

### <span data-ttu-id="1676b-141">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1676b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1676b-142">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1676b-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1676b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1676b-143">OUTPUTS</span></span>

### <span data-ttu-id="1676b-144">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1676b-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1676b-145">Note</span><span class="sxs-lookup"><span data-stu-id="1676b-145">NOTES</span></span>

## <span data-ttu-id="1676b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1676b-146">RELATED LINKS</span></span>
