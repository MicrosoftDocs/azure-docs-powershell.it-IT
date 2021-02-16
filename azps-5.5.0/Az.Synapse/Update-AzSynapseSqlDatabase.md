---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182647"
---
# <span data-ttu-id="cfbbd-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cfbbd-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="cfbbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbbd-103">Aggiorna un database SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cfbbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfbbd-104">SYNTAX</span></span>

### <span data-ttu-id="cfbbd-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfbbd-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfbbd-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbbd-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cfbbd-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbbd-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfbbd-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfbbd-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfbbd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cfbbd-109">DESCRIPTION</span></span>
<span data-ttu-id="cfbbd-110">Il cmdlet **Update-AzSynapseSqlDatabase** aggiorna un database di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cfbbd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfbbd-111">EXAMPLES</span></span>

### <span data-ttu-id="cfbbd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cfbbd-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="cfbbd-113">Questo comando aggiorna un database SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="cfbbd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfbbd-114">PARAMETERS</span></span>

### <span data-ttu-id="cfbbd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfbbd-115">-AsJob</span></span>
<span data-ttu-id="cfbbd-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cfbbd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfbbd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbbd-117">-DefaultProfile</span></span>
<span data-ttu-id="cfbbd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfbbd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfbbd-119">-InputObject</span></span>
<span data-ttu-id="cfbbd-120">SQL di input di database, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfbbd-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="cfbbd-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="cfbbd-122">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbbd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cfbbd-123">-Name</span></span>
<span data-ttu-id="cfbbd-124">Nome del database SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-124">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbbd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfbbd-125">-PassThru</span></span>
<span data-ttu-id="cfbbd-126">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cfbbd-127">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cfbbd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfbbd-128">-ResourceGroupName</span></span>
<span data-ttu-id="cfbbd-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbbd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfbbd-130">-ResourceId</span></span>
<span data-ttu-id="cfbbd-131">Identificatore di risorsa della SQL database.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-131">Resource identifier of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbbd-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="cfbbd-132">-Tag</span></span>
<span data-ttu-id="cfbbd-133">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="cfbbd-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cfbbd-134">-WorkspaceName</span></span>
<span data-ttu-id="cfbbd-135">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-135">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbbd-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cfbbd-136">-WorkspaceObject</span></span>
<span data-ttu-id="cfbbd-137">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-137">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfbbd-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfbbd-138">-Confirm</span></span>
<span data-ttu-id="cfbbd-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfbbd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfbbd-140">-WhatIf</span></span>
<span data-ttu-id="cfbbd-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfbbd-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfbbd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbbd-143">CommonParameters</span></span>
<span data-ttu-id="cfbbd-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbbd-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cfbbd-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbbd-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="cfbbd-146">INPUTS</span></span>

### <span data-ttu-id="cfbbd-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cfbbd-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cfbbd-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cfbbd-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="cfbbd-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfbbd-149">OUTPUTS</span></span>

### <span data-ttu-id="cfbbd-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cfbbd-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="cfbbd-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="cfbbd-151">NOTES</span></span>

## <span data-ttu-id="cfbbd-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfbbd-152">RELATED LINKS</span></span>
