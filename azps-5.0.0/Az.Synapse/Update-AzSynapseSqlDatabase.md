---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: 8f555b18605156aa3394ac02539b7b464feb3ab9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199621"
---
# <span data-ttu-id="ea9e3-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea9e3-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="ea9e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9e3-103">Aggiorna un database SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ea9e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea9e3-104">SYNTAX</span></span>

### <span data-ttu-id="ea9e3-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea9e3-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9e3-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea9e3-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea9e3-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea9e3-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9e3-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea9e3-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea9e3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea9e3-109">DESCRIPTION</span></span>
<span data-ttu-id="ea9e3-110">Il cmdlet **Update-AzSynapseSqlDatabase** aggiorna un database SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ea9e3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea9e3-111">EXAMPLES</span></span>

### <span data-ttu-id="ea9e3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea9e3-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="ea9e3-113">Questo comando aggiorna un database SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ea9e3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea9e3-114">PARAMETERS</span></span>

### <span data-ttu-id="ea9e3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea9e3-115">-AsJob</span></span>
<span data-ttu-id="ea9e3-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ea9e3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea9e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9e3-117">-DefaultProfile</span></span>
<span data-ttu-id="ea9e3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea9e3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea9e3-119">-InputObject</span></span>
<span data-ttu-id="ea9e3-120">Oggetto di input di database SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-120">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea9e3-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="ea9e3-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="ea9e3-122">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-122">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="ea9e3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea9e3-123">-Name</span></span>
<span data-ttu-id="ea9e3-124">Nome del database SQL di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="ea9e3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea9e3-125">-PassThru</span></span>
<span data-ttu-id="ea9e3-126">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ea9e3-127">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ea9e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="ea9e3-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-129">Resource group name.</span></span>

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

### <span data-ttu-id="ea9e3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea9e3-130">-ResourceId</span></span>
<span data-ttu-id="ea9e3-131">Identificatore delle risorse del database SQL di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="ea9e3-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea9e3-132">-Tag</span></span>
<span data-ttu-id="ea9e3-133">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="ea9e3-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ea9e3-134">-WorkspaceName</span></span>
<span data-ttu-id="ea9e3-135">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ea9e3-136">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ea9e3-136">-WorkspaceObject</span></span>
<span data-ttu-id="ea9e3-137">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea9e3-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea9e3-138">-Confirm</span></span>
<span data-ttu-id="ea9e3-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9e3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9e3-140">-WhatIf</span></span>
<span data-ttu-id="ea9e3-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9e3-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9e3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9e3-143">CommonParameters</span></span>
<span data-ttu-id="ea9e3-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9e3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9e3-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea9e3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9e3-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea9e3-146">INPUTS</span></span>

### <span data-ttu-id="ea9e3-147">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea9e3-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ea9e3-148">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea9e3-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="ea9e3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea9e3-149">OUTPUTS</span></span>

### <span data-ttu-id="ea9e3-150">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ea9e3-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="ea9e3-151">Note</span><span class="sxs-lookup"><span data-stu-id="ea9e3-151">NOTES</span></span>

## <span data-ttu-id="ea9e3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea9e3-152">RELATED LINKS</span></span>