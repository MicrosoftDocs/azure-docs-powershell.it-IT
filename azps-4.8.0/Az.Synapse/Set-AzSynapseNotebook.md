---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191112"
---
# <span data-ttu-id="264e2-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="264e2-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="264e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="264e2-102">SYNOPSIS</span></span>
<span data-ttu-id="264e2-103">Crea o aggiorna un blocco appunti in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="264e2-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="264e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="264e2-104">SYNTAX</span></span>

### <span data-ttu-id="264e2-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="264e2-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="264e2-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="264e2-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="264e2-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="264e2-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="264e2-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="264e2-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="264e2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="264e2-109">DESCRIPTION</span></span>
<span data-ttu-id="264e2-110">Il cmdlet **set-AzSynapseNotebook** crea o aggiorna un blocco appunti in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="264e2-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="264e2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="264e2-111">EXAMPLES</span></span>

### <span data-ttu-id="264e2-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="264e2-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="264e2-113">Questo comando consente di creare o aggiornare un blocco appunti dal blocco appunti di file blocco appunti. ipynb nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="264e2-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="264e2-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="264e2-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="264e2-115">Questo comando consente di creare o aggiornare un blocco appunti da blocco appunti. ipynb nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="264e2-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="264e2-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="264e2-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="264e2-117">Questo comando crea o aggiorna un blocco appunti dal blocco appunti di file blocco appunti. ipynb che si connette a ContosoSparkPool e USA 2 esecutori nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="264e2-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="264e2-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="264e2-118">PARAMETERS</span></span>

### <span data-ttu-id="264e2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="264e2-119">-AsJob</span></span>
<span data-ttu-id="264e2-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="264e2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="264e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="264e2-121">-DefaultProfile</span></span>
<span data-ttu-id="264e2-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="264e2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="264e2-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="264e2-123">-DefinitionFile</span></span>
<span data-ttu-id="264e2-124">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="264e2-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e2-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="264e2-125">-ExecutorCount</span></span>
<span data-ttu-id="264e2-126">Numero di esecutori da allocare nel pool di scintille specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="264e2-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e2-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="264e2-127">-ExecutorSize</span></span>
<span data-ttu-id="264e2-128">Numero di core e memoria da usare per gli esecutori assegnati nel pool di scintille specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="264e2-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e2-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="264e2-129">-Name</span></span>
<span data-ttu-id="264e2-130">Il nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="264e2-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e2-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="264e2-131">-SparkPoolName</span></span>
<span data-ttu-id="264e2-132">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="264e2-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e2-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="264e2-133">-WorkspaceName</span></span>
<span data-ttu-id="264e2-134">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="264e2-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e2-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="264e2-135">-WorkspaceObject</span></span>
<span data-ttu-id="264e2-136">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="264e2-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="264e2-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="264e2-137">-Confirm</span></span>
<span data-ttu-id="264e2-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="264e2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="264e2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="264e2-139">-WhatIf</span></span>
<span data-ttu-id="264e2-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="264e2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="264e2-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="264e2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="264e2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264e2-142">CommonParameters</span></span>
<span data-ttu-id="264e2-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="264e2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264e2-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="264e2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264e2-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="264e2-145">INPUTS</span></span>

### <span data-ttu-id="264e2-146">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="264e2-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="264e2-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="264e2-147">OUTPUTS</span></span>

### <span data-ttu-id="264e2-148">Microsoft. Azure. Commands. sinapsi. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="264e2-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="264e2-149">Note</span><span class="sxs-lookup"><span data-stu-id="264e2-149">NOTES</span></span>

## <span data-ttu-id="264e2-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="264e2-150">RELATED LINKS</span></span>
