---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202756"
---
# <span data-ttu-id="0a69a-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a69a-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="0a69a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a69a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a69a-103">Crea un pool di analisi delle sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="0a69a-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a69a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a69a-104">SYNTAX</span></span>

### <span data-ttu-id="0a69a-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a69a-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a69a-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a69a-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a69a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a69a-107">DESCRIPTION</span></span>
<span data-ttu-id="0a69a-108">Il cmdlet **New-AzSynapseSqlPool** crea un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a69a-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a69a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a69a-109">EXAMPLES</span></span>

### <span data-ttu-id="0a69a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0a69a-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="0a69a-111">Questo comando crea un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a69a-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a69a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a69a-112">PARAMETERS</span></span>

### <span data-ttu-id="0a69a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a69a-113">-AsJob</span></span>
<span data-ttu-id="0a69a-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0a69a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a69a-115">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="0a69a-115">-Collation</span></span>
<span data-ttu-id="0a69a-116">La fascicolatura definisce le regole di ordinamento e confronto dei dati e non può essere modificata dopo la creazione del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="0a69a-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="0a69a-117">Le regole di confronto predefinite sono SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="0a69a-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="0a69a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a69a-118">-DefaultProfile</span></span>
<span data-ttu-id="0a69a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a69a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a69a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a69a-120">-Name</span></span>
<span data-ttu-id="0a69a-121">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="0a69a-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="0a69a-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="0a69a-122">-PerformanceLevel</span></span>
<span data-ttu-id="0a69a-123">Livello di prestazioni e livelli di servizio SQL da assegnare al pool SQL.</span><span class="sxs-lookup"><span data-stu-id="0a69a-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="0a69a-124">Ad esempio, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="0a69a-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="0a69a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a69a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a69a-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a69a-126">Resource group name.</span></span>

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

### <span data-ttu-id="0a69a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a69a-127">-Tag</span></span>
<span data-ttu-id="0a69a-128">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a69a-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="0a69a-129">-Versione</span><span class="sxs-lookup"><span data-stu-id="0a69a-129">-Version</span></span>
<span data-ttu-id="0a69a-130">Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="0a69a-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="0a69a-131">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="0a69a-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="0a69a-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a69a-132">-WorkspaceName</span></span>
<span data-ttu-id="0a69a-133">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="0a69a-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0a69a-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a69a-134">-WorkspaceObject</span></span>
<span data-ttu-id="0a69a-135">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a69a-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a69a-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a69a-136">-Confirm</span></span>
<span data-ttu-id="0a69a-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a69a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a69a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a69a-138">-WhatIf</span></span>
<span data-ttu-id="0a69a-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a69a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a69a-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a69a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a69a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a69a-141">CommonParameters</span></span>
<span data-ttu-id="0a69a-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a69a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a69a-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a69a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a69a-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a69a-144">INPUTS</span></span>

### <span data-ttu-id="0a69a-145">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a69a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0a69a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a69a-146">OUTPUTS</span></span>

### <span data-ttu-id="0a69a-147">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a69a-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0a69a-148">Note</span><span class="sxs-lookup"><span data-stu-id="0a69a-148">NOTES</span></span>

## <span data-ttu-id="0a69a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a69a-149">RELATED LINKS</span></span>
