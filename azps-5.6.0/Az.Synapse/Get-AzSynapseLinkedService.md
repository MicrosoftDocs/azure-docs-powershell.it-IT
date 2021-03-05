---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: 61ddc7c6a71dcc5545b8bdc2751e619d7da8e3bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967214"
---
# <span data-ttu-id="0b011-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="0b011-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="0b011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b011-102">SYNOPSIS</span></span>
<span data-ttu-id="0b011-103">Recupera informazioni sui servizi collegati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0b011-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="0b011-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b011-104">SYNTAX</span></span>

### <span data-ttu-id="0b011-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b011-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b011-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="0b011-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b011-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b011-107">DESCRIPTION</span></span>
<span data-ttu-id="0b011-108">Il cmdlet **Get-AzSynapseLinkedService** ottiene informazioni sui servizi collegati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0b011-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="0b011-109">Se si specifica il nome di un servizio collegato, questo cmdlet ottiene informazioni sul servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="0b011-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="0b011-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti i servizi collegati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0b011-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="0b011-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b011-111">EXAMPLES</span></span>

### <span data-ttu-id="0b011-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b011-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0b011-113">Questo comando recupera informazioni su tutti i servizi collegati nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0b011-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0b011-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0b011-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="0b011-115">Questo comando recupera informazioni sul servizio collegato denominato ContosoLinkedService nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0b011-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0b011-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0b011-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="0b011-117">Questo comando recupera informazioni sul servizio collegato denominato ContosoLinkedService nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b011-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0b011-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b011-118">PARAMETERS</span></span>

### <span data-ttu-id="0b011-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b011-119">-DefaultProfile</span></span>
<span data-ttu-id="0b011-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b011-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b011-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0b011-121">-Name</span></span>
<span data-ttu-id="0b011-122">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="0b011-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b011-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0b011-123">-WorkspaceName</span></span>
<span data-ttu-id="0b011-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="0b011-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0b011-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0b011-125">-WorkspaceObject</span></span>
<span data-ttu-id="0b011-126">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b011-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0b011-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b011-127">CommonParameters</span></span>
<span data-ttu-id="0b011-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b011-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b011-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b011-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b011-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b011-130">INPUTS</span></span>

### <span data-ttu-id="0b011-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0b011-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0b011-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b011-132">OUTPUTS</span></span>

### <span data-ttu-id="0b011-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="0b011-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="0b011-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b011-134">NOTES</span></span>

## <span data-ttu-id="0b011-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b011-135">RELATED LINKS</span></span>
