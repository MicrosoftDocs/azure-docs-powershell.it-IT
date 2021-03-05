---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 73664b619670f17a92bd915f6e4d8501a8ac9f6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976061"
---
# <span data-ttu-id="5b195-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b195-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="5b195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b195-102">SYNOPSIS</span></span>
<span data-ttu-id="5b195-103">Crea un database SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5b195-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5b195-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b195-104">SYNTAX</span></span>

### <span data-ttu-id="5b195-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b195-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b195-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b195-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b195-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5b195-107">DESCRIPTION</span></span>
<span data-ttu-id="5b195-108">Il cmdlet **Get-AzSynapseSqlDatabase** ottiene informazioni su un database di Azure Synapse Analytics SQL database.</span><span class="sxs-lookup"><span data-stu-id="5b195-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5b195-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b195-109">EXAMPLES</span></span>

### <span data-ttu-id="5b195-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5b195-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="5b195-111">Questo comando crea un database SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5b195-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5b195-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b195-112">PARAMETERS</span></span>

### <span data-ttu-id="5b195-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b195-113">-AsJob</span></span>
<span data-ttu-id="5b195-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5b195-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b195-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="5b195-115">-Collation</span></span>
<span data-ttu-id="5b195-116">Le regole di confronto definiscono le regole per ordinare e confrontare i dati e non possono essere modificate dopo la SQL del pool.</span><span class="sxs-lookup"><span data-stu-id="5b195-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="5b195-117">La fascicolazione predefinita SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="5b195-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="5b195-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b195-118">-DefaultProfile</span></span>
<span data-ttu-id="5b195-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b195-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b195-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="5b195-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="5b195-121">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="5b195-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b195-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5b195-122">-Name</span></span>
<span data-ttu-id="5b195-123">Nome del database SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5b195-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="5b195-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b195-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b195-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b195-125">Resource group name.</span></span>

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

### <span data-ttu-id="5b195-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b195-126">-Tag</span></span>
<span data-ttu-id="5b195-127">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="5b195-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5b195-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b195-128">-WorkspaceName</span></span>
<span data-ttu-id="5b195-129">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="5b195-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5b195-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5b195-130">-WorkspaceObject</span></span>
<span data-ttu-id="5b195-131">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="5b195-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5b195-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b195-132">-Confirm</span></span>
<span data-ttu-id="5b195-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b195-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b195-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b195-134">-WhatIf</span></span>
<span data-ttu-id="5b195-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b195-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b195-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5b195-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b195-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b195-137">CommonParameters</span></span>
<span data-ttu-id="5b195-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b195-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b195-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b195-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b195-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="5b195-140">INPUTS</span></span>

### <span data-ttu-id="5b195-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5b195-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5b195-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b195-142">OUTPUTS</span></span>

### <span data-ttu-id="5b195-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5b195-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="5b195-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="5b195-144">NOTES</span></span>

## <span data-ttu-id="5b195-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b195-145">RELATED LINKS</span></span>
