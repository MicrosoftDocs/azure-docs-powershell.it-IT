---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474559"
---
# <span data-ttu-id="75fd8-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="75fd8-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="75fd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="75fd8-103">Ottiene informazioni sui servizi collegati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="75fd8-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="75fd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75fd8-104">SYNTAX</span></span>

### <span data-ttu-id="75fd8-105">GetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75fd8-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75fd8-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="75fd8-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75fd8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75fd8-107">DESCRIPTION</span></span>
<span data-ttu-id="75fd8-108">Il cmdlet **Get-AzSynapseLinkedService** ottiene le informazioni sui servizi collegati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="75fd8-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="75fd8-109">Se specifichi il nome di un servizio collegato, questo cmdlet ottiene le informazioni sul servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="75fd8-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="75fd8-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti i servizi collegati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="75fd8-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="75fd8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75fd8-111">EXAMPLES</span></span>

### <span data-ttu-id="75fd8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75fd8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="75fd8-113">Questo comando consente di ottenere informazioni su tutti i servizi collegati nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="75fd8-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="75fd8-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75fd8-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="75fd8-115">Questo comando consente di ottenere informazioni sul servizio collegato denominato ContosoLinkedService nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="75fd8-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="75fd8-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="75fd8-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="75fd8-117">Questo comando ottiene le informazioni sul servizio collegato denominato ContosoLinkedService nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="75fd8-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="75fd8-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75fd8-118">PARAMETERS</span></span>

### <span data-ttu-id="75fd8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75fd8-119">-DefaultProfile</span></span>
<span data-ttu-id="75fd8-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75fd8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75fd8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="75fd8-121">-Name</span></span>
<span data-ttu-id="75fd8-122">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="75fd8-122">The linked service name.</span></span>

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

### <span data-ttu-id="75fd8-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="75fd8-123">-WorkspaceName</span></span>
<span data-ttu-id="75fd8-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="75fd8-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="75fd8-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="75fd8-125">-WorkspaceObject</span></span>
<span data-ttu-id="75fd8-126">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="75fd8-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="75fd8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75fd8-127">CommonParameters</span></span>
<span data-ttu-id="75fd8-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75fd8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75fd8-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75fd8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75fd8-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75fd8-130">INPUTS</span></span>

### <span data-ttu-id="75fd8-131">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="75fd8-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="75fd8-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75fd8-132">OUTPUTS</span></span>

### <span data-ttu-id="75fd8-133">Microsoft. Azure. Commands. sinapsi. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="75fd8-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="75fd8-134">Note</span><span class="sxs-lookup"><span data-stu-id="75fd8-134">NOTES</span></span>

## <span data-ttu-id="75fd8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75fd8-135">RELATED LINKS</span></span>
