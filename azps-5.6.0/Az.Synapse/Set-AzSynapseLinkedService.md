---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 1e05754245b4179d02c144538473fa586531f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007485"
---
# <span data-ttu-id="ce0c2-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="ce0c2-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="ce0c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0c2-103">Collega un archivio dati o un servizio cloud all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="ce0c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce0c2-104">SYNTAX</span></span>

### <span data-ttu-id="ce0c2-105">SetByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce0c2-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0c2-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="ce0c2-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce0c2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce0c2-107">DESCRIPTION</span></span>
<span data-ttu-id="ce0c2-108">Il cmdlet **Set-AzSynapseLinkedService** collega un archivio dati o un servizio cloud all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="ce0c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce0c2-109">EXAMPLES</span></span>

### <span data-ttu-id="ce0c2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce0c2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="ce0c2-111">Questo comando crea un servizio collegato denominato ContosoLinkedService nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ce0c2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ce0c2-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="ce0c2-113">Questo comando crea un servizio collegato denominato ContosoLinkedService nell'area di lavoro contosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ce0c2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce0c2-114">PARAMETERS</span></span>

### <span data-ttu-id="ce0c2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce0c2-115">-AsJob</span></span>
<span data-ttu-id="ce0c2-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ce0c2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce0c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0c2-117">-DefaultProfile</span></span>
<span data-ttu-id="ce0c2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce0c2-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ce0c2-119">-DefinitionFile</span></span>
<span data-ttu-id="ce0c2-120">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-120">The JSON file path.</span></span>

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

### <span data-ttu-id="ce0c2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ce0c2-121">-Name</span></span>
<span data-ttu-id="ce0c2-122">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0c2-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce0c2-123">-WorkspaceName</span></span>
<span data-ttu-id="ce0c2-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0c2-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ce0c2-125">-WorkspaceObject</span></span>
<span data-ttu-id="ce0c2-126">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0c2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce0c2-127">-Confirm</span></span>
<span data-ttu-id="ce0c2-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0c2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0c2-129">-WhatIf</span></span>
<span data-ttu-id="ce0c2-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0c2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0c2-132">CommonParameters</span></span>
<span data-ttu-id="ce0c2-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0c2-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce0c2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0c2-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce0c2-135">INPUTS</span></span>

### <span data-ttu-id="ce0c2-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce0c2-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ce0c2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce0c2-137">OUTPUTS</span></span>

### <span data-ttu-id="ce0c2-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="ce0c2-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="ce0c2-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce0c2-139">NOTES</span></span>

## <span data-ttu-id="ce0c2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce0c2-140">RELATED LINKS</span></span>
