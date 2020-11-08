---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189193"
---
# <span data-ttu-id="542bb-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="542bb-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="542bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="542bb-102">SYNOPSIS</span></span>
<span data-ttu-id="542bb-103">Esporta notbooks.</span><span class="sxs-lookup"><span data-stu-id="542bb-103">Exports notbooks.</span></span>

## <span data-ttu-id="542bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="542bb-104">SYNTAX</span></span>

### <span data-ttu-id="542bb-105">ExportByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="542bb-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542bb-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="542bb-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="542bb-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="542bb-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="542bb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="542bb-108">DESCRIPTION</span></span>
<span data-ttu-id="542bb-109">Il cmdlet **Export-AzSynapseNotebook** esporta un blocco appunti di Azure sinapsi in un file di blocco appunti (ipynb).</span><span class="sxs-lookup"><span data-stu-id="542bb-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="542bb-110">Il nome del blocco appunti diventa il nome del file esportato.</span><span class="sxs-lookup"><span data-stu-id="542bb-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="542bb-111">Se specifichi il nome di un blocco appunti, il cmdlet Esporta il blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="542bb-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="542bb-112">Se non si specifica un nome, il cmdlet Esporta tutti i blocchi appunti nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="542bb-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="542bb-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="542bb-113">EXAMPLES</span></span>

### <span data-ttu-id="542bb-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="542bb-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="542bb-115">Esporta tutti i blocchi appunti nell'area di lavoro ContosoWorkspace nella cartella "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="542bb-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="542bb-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="542bb-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="542bb-117">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="542bb-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="542bb-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="542bb-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="542bb-119">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Notebook" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="542bb-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="542bb-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="542bb-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="542bb-121">Esporta un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace nella cartella "C:\Notebook" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="542bb-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="542bb-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="542bb-122">PARAMETERS</span></span>

### <span data-ttu-id="542bb-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="542bb-123">-AsJob</span></span>
<span data-ttu-id="542bb-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="542bb-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="542bb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542bb-125">-DefaultProfile</span></span>
<span data-ttu-id="542bb-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="542bb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="542bb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="542bb-127">-InputObject</span></span>
<span data-ttu-id="542bb-128">Oggetto blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="542bb-128">The notebook object.</span></span>

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

### <span data-ttu-id="542bb-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="542bb-129">-Name</span></span>
<span data-ttu-id="542bb-130">Il nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="542bb-130">The notebook name.</span></span>

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

### <span data-ttu-id="542bb-131">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="542bb-131">-OutputFolder</span></span>
<span data-ttu-id="542bb-132">Cartella in cui deve essere posizionato il blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="542bb-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="542bb-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="542bb-133">-WorkspaceName</span></span>
<span data-ttu-id="542bb-134">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="542bb-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="542bb-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="542bb-135">-WorkspaceObject</span></span>
<span data-ttu-id="542bb-136">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="542bb-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="542bb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542bb-137">CommonParameters</span></span>
<span data-ttu-id="542bb-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="542bb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542bb-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="542bb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542bb-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="542bb-140">INPUTS</span></span>

### <span data-ttu-id="542bb-141">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="542bb-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="542bb-142">Microsoft. Azure. Commands. sinapsi. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="542bb-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="542bb-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="542bb-143">OUTPUTS</span></span>

### <span data-ttu-id="542bb-144">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="542bb-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="542bb-145">Note</span><span class="sxs-lookup"><span data-stu-id="542bb-145">NOTES</span></span>

## <span data-ttu-id="542bb-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="542bb-146">RELATED LINKS</span></span>
