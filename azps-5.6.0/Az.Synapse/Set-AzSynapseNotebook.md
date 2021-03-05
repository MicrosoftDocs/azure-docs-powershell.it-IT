---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: 9b960c3b671ecada8f4f24e1b5a8897de7004440
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007438"
---
# <span data-ttu-id="72dc6-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="72dc6-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="72dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="72dc6-103">Crea o aggiorna un blocco appunti in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="72dc6-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="72dc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72dc6-104">SYNTAX</span></span>

### <span data-ttu-id="72dc6-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72dc6-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dc6-106">SetByNameAndsparkPool</span><span class="sxs-lookup"><span data-stu-id="72dc6-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dc6-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="72dc6-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dc6-108">SetByObjectAndsparkPool</span><span class="sxs-lookup"><span data-stu-id="72dc6-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72dc6-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72dc6-109">DESCRIPTION</span></span>
<span data-ttu-id="72dc6-110">Il cmdlet **Set-AzSynapseNotebook** crea o aggiorna un blocco appunti in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="72dc6-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="72dc6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72dc6-111">EXAMPLES</span></span>

### <span data-ttu-id="72dc6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72dc6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="72dc6-113">Questo comando crea o aggiorna un blocco appunti dal file del blocco appunti notebook.ipynb nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="72dc6-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="72dc6-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="72dc6-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="72dc6-115">Questo comando crea o aggiorna un blocco appunti dal file del blocco appunti notebook notebook.ipynb nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="72dc6-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="72dc6-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="72dc6-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="72dc6-117">Questo comando crea o aggiorna un blocco appunti dal file del blocco appunti notebook notebook.ipynb, che si collega a ContosoSparkPool e usa 2 esecutori nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="72dc6-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="72dc6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72dc6-118">PARAMETERS</span></span>

### <span data-ttu-id="72dc6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72dc6-119">-AsJob</span></span>
<span data-ttu-id="72dc6-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="72dc6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72dc6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dc6-121">-DefaultProfile</span></span>
<span data-ttu-id="72dc6-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72dc6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72dc6-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="72dc6-123">-DefinitionFile</span></span>
<span data-ttu-id="72dc6-124">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="72dc6-124">The JSON file path.</span></span>

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

### <span data-ttu-id="72dc6-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="72dc6-125">-ExecutorCount</span></span>
<span data-ttu-id="72dc6-126">Numero di esecutori da allocare nel pool spark specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="72dc6-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="72dc6-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="72dc6-127">-ExecutorSize</span></span>
<span data-ttu-id="72dc6-128">Numero di core e memoria da usare per gli esecutori allocati nel pool Spark specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="72dc6-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="72dc6-129">-Name</span><span class="sxs-lookup"><span data-stu-id="72dc6-129">-Name</span></span>
<span data-ttu-id="72dc6-130">Nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="72dc6-130">The notebook name.</span></span>

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

### <span data-ttu-id="72dc6-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="72dc6-131">-SparkPoolName</span></span>
<span data-ttu-id="72dc6-132">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="72dc6-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="72dc6-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="72dc6-133">-WorkspaceName</span></span>
<span data-ttu-id="72dc6-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="72dc6-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="72dc6-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="72dc6-135">-WorkspaceObject</span></span>
<span data-ttu-id="72dc6-136">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="72dc6-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="72dc6-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72dc6-137">-Confirm</span></span>
<span data-ttu-id="72dc6-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dc6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72dc6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72dc6-139">-WhatIf</span></span>
<span data-ttu-id="72dc6-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72dc6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72dc6-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72dc6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72dc6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dc6-142">CommonParameters</span></span>
<span data-ttu-id="72dc6-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72dc6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dc6-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72dc6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dc6-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="72dc6-145">INPUTS</span></span>

### <span data-ttu-id="72dc6-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="72dc6-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="72dc6-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72dc6-147">OUTPUTS</span></span>

### <span data-ttu-id="72dc6-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="72dc6-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="72dc6-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="72dc6-149">NOTES</span></span>

## <span data-ttu-id="72dc6-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72dc6-150">RELATED LINKS</span></span>
