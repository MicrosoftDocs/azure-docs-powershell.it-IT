---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209066"
---
# <span data-ttu-id="75645-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="75645-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="75645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75645-102">SYNOPSIS</span></span>
<span data-ttu-id="75645-103">Esporta notbook.</span><span class="sxs-lookup"><span data-stu-id="75645-103">Exports notbooks.</span></span>

## <span data-ttu-id="75645-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75645-104">SYNTAX</span></span>

### <span data-ttu-id="75645-105">ExportByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75645-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75645-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="75645-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75645-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="75645-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75645-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75645-108">DESCRIPTION</span></span>
<span data-ttu-id="75645-109">Il cmdlet **Export-AzSynapseNotebook** esporta un blocco appunti Azure Synapse in un file del blocco appunti (con estensione ipynb).</span><span class="sxs-lookup"><span data-stu-id="75645-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="75645-110">Il nome del blocco appunti diventa il nome del file esportato.</span><span class="sxs-lookup"><span data-stu-id="75645-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="75645-111">Se si specifica il nome di un blocco appunti, il cmdlet esporta il blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="75645-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="75645-112">Se non si specifica un nome, il cmdlet esporta tutti i blocchi appunti nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="75645-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="75645-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75645-113">EXAMPLES</span></span>

### <span data-ttu-id="75645-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75645-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75645-115">Esporta tutti i blocchi appunti nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti".</span><span class="sxs-lookup"><span data-stu-id="75645-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="75645-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75645-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75645-117">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti".</span><span class="sxs-lookup"><span data-stu-id="75645-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="75645-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="75645-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75645-119">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="75645-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="75645-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="75645-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="75645-121">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Blocco appunti" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="75645-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="75645-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75645-122">PARAMETERS</span></span>

### <span data-ttu-id="75645-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75645-123">-AsJob</span></span>
<span data-ttu-id="75645-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="75645-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75645-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75645-125">-DefaultProfile</span></span>
<span data-ttu-id="75645-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75645-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75645-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75645-127">-InputObject</span></span>
<span data-ttu-id="75645-128">Oggetto blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="75645-128">The notebook object.</span></span>

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

### <span data-ttu-id="75645-129">-Name</span><span class="sxs-lookup"><span data-stu-id="75645-129">-Name</span></span>
<span data-ttu-id="75645-130">Nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="75645-130">The notebook name.</span></span>

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

### <span data-ttu-id="75645-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="75645-131">-OutputFolder</span></span>
<span data-ttu-id="75645-132">La cartella in cui deve essere inserito il blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="75645-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="75645-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75645-133">-WorkspaceName</span></span>
<span data-ttu-id="75645-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="75645-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="75645-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="75645-135">-WorkspaceObject</span></span>
<span data-ttu-id="75645-136">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="75645-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="75645-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75645-137">CommonParameters</span></span>
<span data-ttu-id="75645-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75645-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75645-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75645-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75645-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="75645-140">INPUTS</span></span>

### <span data-ttu-id="75645-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75645-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="75645-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="75645-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="75645-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75645-143">OUTPUTS</span></span>

### <span data-ttu-id="75645-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="75645-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="75645-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="75645-145">NOTES</span></span>

## <span data-ttu-id="75645-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75645-146">RELATED LINKS</span></span>
