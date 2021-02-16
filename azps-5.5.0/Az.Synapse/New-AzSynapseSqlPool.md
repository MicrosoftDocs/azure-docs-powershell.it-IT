---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182751"
---
# <span data-ttu-id="60f45-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="60f45-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="60f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60f45-102">SYNOPSIS</span></span>
<span data-ttu-id="60f45-103">Crea un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="60f45-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="60f45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60f45-104">SYNTAX</span></span>

### <span data-ttu-id="60f45-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60f45-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60f45-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60f45-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f45-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60f45-107">DESCRIPTION</span></span>
<span data-ttu-id="60f45-108">Il cmdlet **New-AzSynapseSqlPool** crea un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="60f45-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="60f45-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60f45-109">EXAMPLES</span></span>

### <span data-ttu-id="60f45-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60f45-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="60f45-111">Questo comando crea un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="60f45-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="60f45-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60f45-112">PARAMETERS</span></span>

### <span data-ttu-id="60f45-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60f45-113">-AsJob</span></span>
<span data-ttu-id="60f45-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60f45-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60f45-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="60f45-115">-Collation</span></span>
<span data-ttu-id="60f45-116">La fascicolazione definisce le regole per ordinare e confrontare i dati e non può essere modificata dopo la SQL del pool.</span><span class="sxs-lookup"><span data-stu-id="60f45-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="60f45-117">La fascicolazione predefinita SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="60f45-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f45-118">-DefaultProfile</span></span>
<span data-ttu-id="60f45-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60f45-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60f45-120">-Name</span><span class="sxs-lookup"><span data-stu-id="60f45-120">-Name</span></span>
<span data-ttu-id="60f45-121">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="60f45-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f45-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="60f45-122">-PerformanceLevel</span></span>
<span data-ttu-id="60f45-123">Il SQL servizio e il livello di prestazioni da assegnare al pool SQL locale.</span><span class="sxs-lookup"><span data-stu-id="60f45-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="60f45-124">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="60f45-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="60f45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f45-125">-ResourceGroupName</span></span>
<span data-ttu-id="60f45-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60f45-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f45-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="60f45-127">-Tag</span></span>
<span data-ttu-id="60f45-128">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="60f45-128">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f45-129">-Version</span><span class="sxs-lookup"><span data-stu-id="60f45-129">-Version</span></span>
<span data-ttu-id="60f45-130">Versione di Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="60f45-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="60f45-131">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="60f45-131">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f45-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="60f45-132">-WorkspaceName</span></span>
<span data-ttu-id="60f45-133">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="60f45-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f45-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="60f45-134">-WorkspaceObject</span></span>
<span data-ttu-id="60f45-135">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="60f45-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60f45-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60f45-136">-Confirm</span></span>
<span data-ttu-id="60f45-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60f45-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f45-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f45-138">-WhatIf</span></span>
<span data-ttu-id="60f45-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f45-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f45-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60f45-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f45-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f45-141">CommonParameters</span></span>
<span data-ttu-id="60f45-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f45-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f45-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60f45-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f45-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="60f45-144">INPUTS</span></span>

### <span data-ttu-id="60f45-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="60f45-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="60f45-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60f45-146">OUTPUTS</span></span>

### <span data-ttu-id="60f45-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="60f45-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="60f45-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="60f45-148">NOTES</span></span>

## <span data-ttu-id="60f45-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60f45-149">RELATED LINKS</span></span>
