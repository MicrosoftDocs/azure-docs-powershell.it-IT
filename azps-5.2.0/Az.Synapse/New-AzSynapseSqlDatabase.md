---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356534"
---
# <span data-ttu-id="495c9-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="495c9-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="495c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="495c9-102">SYNOPSIS</span></span>
<span data-ttu-id="495c9-103">Crea un database SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="495c9-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="495c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="495c9-104">SYNTAX</span></span>

### <span data-ttu-id="495c9-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="495c9-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="495c9-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="495c9-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="495c9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="495c9-107">DESCRIPTION</span></span>
<span data-ttu-id="495c9-108">Il cmdlet **Get-AzSynapseSqlDatabase** ottiene le informazioni su un database SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="495c9-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="495c9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="495c9-109">EXAMPLES</span></span>

### <span data-ttu-id="495c9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="495c9-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="495c9-111">Questo comando crea un database SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="495c9-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="495c9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="495c9-112">PARAMETERS</span></span>

### <span data-ttu-id="495c9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="495c9-113">-AsJob</span></span>
<span data-ttu-id="495c9-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="495c9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="495c9-115">-Regole di confronto</span><span class="sxs-lookup"><span data-stu-id="495c9-115">-Collation</span></span>
<span data-ttu-id="495c9-116">La fascicolatura definisce le regole di ordinamento e confronto dei dati e non può essere modificata dopo la creazione del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="495c9-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="495c9-117">Le regole di confronto predefinite sono SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="495c9-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="495c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495c9-118">-DefaultProfile</span></span>
<span data-ttu-id="495c9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="495c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495c9-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="495c9-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="495c9-121">Specifica la dimensione massima del database in byte.</span><span class="sxs-lookup"><span data-stu-id="495c9-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="495c9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="495c9-122">-Name</span></span>
<span data-ttu-id="495c9-123">Nome del database SQL di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="495c9-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="495c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="495c9-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="495c9-125">Resource group name.</span></span>

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

### <span data-ttu-id="495c9-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="495c9-126">-Tag</span></span>
<span data-ttu-id="495c9-127">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="495c9-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="495c9-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="495c9-128">-WorkspaceName</span></span>
<span data-ttu-id="495c9-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="495c9-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="495c9-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="495c9-130">-WorkspaceObject</span></span>
<span data-ttu-id="495c9-131">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="495c9-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="495c9-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="495c9-132">-Confirm</span></span>
<span data-ttu-id="495c9-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="495c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="495c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495c9-134">-WhatIf</span></span>
<span data-ttu-id="495c9-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="495c9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="495c9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="495c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="495c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495c9-137">CommonParameters</span></span>
<span data-ttu-id="495c9-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495c9-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="495c9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495c9-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="495c9-140">INPUTS</span></span>

### <span data-ttu-id="495c9-141">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="495c9-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="495c9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="495c9-142">OUTPUTS</span></span>

### <span data-ttu-id="495c9-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="495c9-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="495c9-144">Note</span><span class="sxs-lookup"><span data-stu-id="495c9-144">NOTES</span></span>

## <span data-ttu-id="495c9-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="495c9-145">RELATED LINKS</span></span>
