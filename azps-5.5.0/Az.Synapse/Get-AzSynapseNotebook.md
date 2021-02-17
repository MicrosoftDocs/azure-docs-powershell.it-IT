---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207682"
---
# <span data-ttu-id="c9595-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="c9595-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="c9595-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9595-102">SYNOPSIS</span></span>
<span data-ttu-id="c9595-103">Recupera informazioni sui blocchi appunti in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9595-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="c9595-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9595-104">SYNTAX</span></span>

### <span data-ttu-id="c9595-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9595-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9595-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="c9595-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9595-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c9595-107">DESCRIPTION</span></span>
<span data-ttu-id="c9595-108">Il cmdlet **Get-AzSynapseNotebook** ottiene informazioni sui blocchi appunti in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9595-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="c9595-109">Se si specifica il nome di un blocco appunti, il cmdlet riceverà informazioni sul blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="c9595-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="c9595-110">Se non si specifica un nome, il cmdlet riceve informazioni su tutti i blocchi appunti nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9595-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="c9595-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9595-111">EXAMPLES</span></span>

### <span data-ttu-id="c9595-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9595-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="c9595-113">Ottiene un elenco di tutti i blocchi appunti nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c9595-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c9595-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c9595-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="c9595-115">Ottiene un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c9595-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c9595-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c9595-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="c9595-117">Ottiene un singolo blocco appunti denominato ContosoNotebook nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9595-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c9595-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9595-118">PARAMETERS</span></span>

### <span data-ttu-id="c9595-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9595-119">-DefaultProfile</span></span>
<span data-ttu-id="c9595-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9595-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9595-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c9595-121">-Name</span></span>
<span data-ttu-id="c9595-122">Nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="c9595-122">The notebook name.</span></span>

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

### <span data-ttu-id="c9595-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9595-123">-WorkspaceName</span></span>
<span data-ttu-id="c9595-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c9595-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9595-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c9595-125">-WorkspaceObject</span></span>
<span data-ttu-id="c9595-126">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9595-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9595-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9595-127">CommonParameters</span></span>
<span data-ttu-id="c9595-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9595-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9595-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9595-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9595-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="c9595-130">INPUTS</span></span>

### <span data-ttu-id="c9595-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9595-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c9595-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9595-132">OUTPUTS</span></span>

### <span data-ttu-id="c9595-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="c9595-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="c9595-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="c9595-134">NOTES</span></span>

## <span data-ttu-id="c9595-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9595-135">RELATED LINKS</span></span>
