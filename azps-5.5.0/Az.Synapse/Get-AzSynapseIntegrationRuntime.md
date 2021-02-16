---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195638"
---
# <span data-ttu-id="9bd39-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9bd39-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="9bd39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd39-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd39-103">Ottiene informazioni sulle risorse di runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9bd39-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="9bd39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bd39-104">SYNTAX</span></span>

### <span data-ttu-id="9bd39-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bd39-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd39-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd39-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bd39-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd39-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9bd39-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd39-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bd39-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9bd39-109">DESCRIPTION</span></span>
<span data-ttu-id="9bd39-110">Il cmdlet **Get-AzSynapseIntegrationRuntime** ottiene informazioni sui runtime di integrazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9bd39-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="9bd39-111">Se si specifica il nome di un runtime di integrazione, questo cmdlet ottiene informazioni su tale runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9bd39-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="9bd39-112">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i runtime di integrazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9bd39-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="9bd39-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bd39-113">EXAMPLES</span></span>

### <span data-ttu-id="9bd39-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9bd39-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9bd39-115">Elencare tutti i runtime di integrazione nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9bd39-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9bd39-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9bd39-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="9bd39-117">Questo comando visualizza informazioni sul runtime di integrazione denominato "test-selfhost-ir" nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9bd39-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9bd39-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9bd39-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="9bd39-119">Questo comando visualizza lo stato dei dettagli sul runtime di integrazione denominato "test-selfhost-ir" nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9bd39-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9bd39-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bd39-120">PARAMETERS</span></span>

### <span data-ttu-id="9bd39-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd39-121">-DefaultProfile</span></span>
<span data-ttu-id="9bd39-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd39-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd39-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bd39-123">-InputObject</span></span>
<span data-ttu-id="9bd39-124">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9bd39-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="9bd39-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9bd39-125">-Name</span></span>
<span data-ttu-id="9bd39-126">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9bd39-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="9bd39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd39-127">-ResourceGroupName</span></span>
<span data-ttu-id="9bd39-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9bd39-128">Resource group name.</span></span>

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

### <span data-ttu-id="9bd39-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bd39-129">-ResourceId</span></span>
<span data-ttu-id="9bd39-130">Identificatore di risorsa del runtime di integrazione synapse.</span><span class="sxs-lookup"><span data-stu-id="9bd39-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="9bd39-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="9bd39-131">-Status</span></span>
<span data-ttu-id="9bd39-132">Stato dei dettagli del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="9bd39-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="9bd39-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9bd39-133">-WorkspaceName</span></span>
<span data-ttu-id="9bd39-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="9bd39-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9bd39-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9bd39-135">-WorkspaceObject</span></span>
<span data-ttu-id="9bd39-136">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9bd39-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9bd39-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd39-137">CommonParameters</span></span>
<span data-ttu-id="9bd39-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd39-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd39-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9bd39-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd39-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="9bd39-140">INPUTS</span></span>

### <span data-ttu-id="9bd39-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9bd39-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9bd39-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9bd39-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9bd39-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bd39-143">OUTPUTS</span></span>

### <span data-ttu-id="9bd39-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9bd39-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9bd39-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="9bd39-145">NOTES</span></span>

## <span data-ttu-id="9bd39-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bd39-146">RELATED LINKS</span></span>
