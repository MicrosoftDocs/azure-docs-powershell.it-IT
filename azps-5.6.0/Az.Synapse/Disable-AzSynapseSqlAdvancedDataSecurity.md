---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 58b2aa2f62de5cc47a9319c9cf36b0d2c8d55975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961134"
---
# <span data-ttu-id="3d1ef-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="3d1ef-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="3d1ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1ef-103">Disabilita Advanced Data Security in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="3d1ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d1ef-104">SYNTAX</span></span>

### <span data-ttu-id="3d1ef-105">DisableByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d1ef-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d1ef-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d1ef-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d1ef-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d1ef-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d1ef-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d1ef-108">DESCRIPTION</span></span>
<span data-ttu-id="3d1ef-109">Il cmdlet **Disable-AzSynapseSqlAdvancedDataSecurity** disabilita Advanced Data Security in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="3d1ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d1ef-110">EXAMPLES</span></span>

### <span data-ttu-id="3d1ef-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d1ef-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3d1ef-112">Questo comando disabilita Advanced Data Security nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3d1ef-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d1ef-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="3d1ef-114">Questo comando disabilita Advanced Data Security nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3d1ef-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d1ef-115">PARAMETERS</span></span>

### <span data-ttu-id="3d1ef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d1ef-116">-AsJob</span></span>
<span data-ttu-id="3d1ef-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3d1ef-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d1ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1ef-118">-DefaultProfile</span></span>
<span data-ttu-id="3d1ef-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d1ef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d1ef-120">-InputObject</span></span>
<span data-ttu-id="3d1ef-121">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d1ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d1ef-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ef-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d1ef-124">-ResourceId</span></span>
<span data-ttu-id="3d1ef-125">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ef-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3d1ef-126">-WorkspaceName</span></span>
<span data-ttu-id="3d1ef-127">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ef-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d1ef-128">-Confirm</span></span>
<span data-ttu-id="3d1ef-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d1ef-130">-WhatIf</span></span>
<span data-ttu-id="3d1ef-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d1ef-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1ef-133">CommonParameters</span></span>
<span data-ttu-id="3d1ef-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1ef-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d1ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1ef-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d1ef-136">INPUTS</span></span>

### <span data-ttu-id="3d1ef-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3d1ef-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3d1ef-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d1ef-138">OUTPUTS</span></span>

### <span data-ttu-id="3d1ef-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="3d1ef-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="3d1ef-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d1ef-140">NOTES</span></span>

## <span data-ttu-id="3d1ef-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d1ef-141">RELATED LINKS</span></span>
