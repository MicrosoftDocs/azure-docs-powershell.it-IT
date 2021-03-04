---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: 110d72f0a73a6a710e014a08c64cadf3b8be7d0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981869"
---
# <span data-ttu-id="30143-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="30143-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="30143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30143-102">SYNOPSIS</span></span>
<span data-ttu-id="30143-103">Esporta notbook.</span><span class="sxs-lookup"><span data-stu-id="30143-103">Exports notbooks.</span></span>

## <span data-ttu-id="30143-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30143-104">SYNTAX</span></span>

### <span data-ttu-id="30143-105">ExportByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30143-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30143-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="30143-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30143-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="30143-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30143-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30143-108">DESCRIPTION</span></span>
<span data-ttu-id="30143-109">Il cmdlet **Export-AzSynapseNotebook** esporta un blocco appunti Azure Synapse in un file del blocco appunti (con estensione ipynb).</span><span class="sxs-lookup"><span data-stu-id="30143-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="30143-110">Il nome del blocco appunti diventa il nome del file esportato.</span><span class="sxs-lookup"><span data-stu-id="30143-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="30143-111">Se si specifica il nome di un blocco appunti, il cmdlet esporta il blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="30143-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="30143-112">Se non si specifica un nome, il cmdlet esporta tutti i blocchi appunti nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="30143-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="30143-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30143-113">EXAMPLES</span></span>

### <span data-ttu-id="30143-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30143-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="30143-115">Esporta tutti i blocchi appunti nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti".</span><span class="sxs-lookup"><span data-stu-id="30143-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="30143-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="30143-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="30143-117">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti".</span><span class="sxs-lookup"><span data-stu-id="30143-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="30143-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="30143-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="30143-119">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="30143-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="30143-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="30143-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="30143-121">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="30143-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="30143-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30143-122">PARAMETERS</span></span>

### <span data-ttu-id="30143-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30143-123">-AsJob</span></span>
<span data-ttu-id="30143-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="30143-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30143-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30143-125">-DefaultProfile</span></span>
<span data-ttu-id="30143-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30143-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30143-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30143-127">-InputObject</span></span>
<span data-ttu-id="30143-128">Oggetto blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="30143-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30143-129">-Name</span><span class="sxs-lookup"><span data-stu-id="30143-129">-Name</span></span>
<span data-ttu-id="30143-130">Nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="30143-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30143-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="30143-131">-OutputFolder</span></span>
<span data-ttu-id="30143-132">La cartella in cui deve essere inserito il blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="30143-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="30143-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="30143-133">-WorkspaceName</span></span>
<span data-ttu-id="30143-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="30143-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30143-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="30143-135">-WorkspaceObject</span></span>
<span data-ttu-id="30143-136">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="30143-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30143-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30143-137">CommonParameters</span></span>
<span data-ttu-id="30143-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30143-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30143-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30143-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30143-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="30143-140">INPUTS</span></span>

### <span data-ttu-id="30143-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="30143-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="30143-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="30143-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="30143-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30143-143">OUTPUTS</span></span>

### <span data-ttu-id="30143-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="30143-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="30143-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="30143-145">NOTES</span></span>

## <span data-ttu-id="30143-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30143-146">RELATED LINKS</span></span>
