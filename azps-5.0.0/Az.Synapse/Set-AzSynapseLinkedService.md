---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199622"
---
# <span data-ttu-id="0de21-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="0de21-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="0de21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0de21-102">SYNOPSIS</span></span>
<span data-ttu-id="0de21-103">Collega un archivio dati o un servizio cloud all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0de21-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="0de21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0de21-104">SYNTAX</span></span>

### <span data-ttu-id="0de21-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0de21-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0de21-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="0de21-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0de21-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0de21-107">DESCRIPTION</span></span>
<span data-ttu-id="0de21-108">Il cmdlet **set-AzSynapseLinkedService** collega un archivio dati o un servizio cloud all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0de21-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="0de21-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0de21-109">EXAMPLES</span></span>

### <span data-ttu-id="0de21-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0de21-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="0de21-111">Questo comando crea un servizio collegato denominato ContosoLinkedService nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0de21-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0de21-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0de21-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="0de21-113">Questo comando crea un servizio collegato denominato ContosoLinkedService nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="0de21-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0de21-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0de21-114">PARAMETERS</span></span>

### <span data-ttu-id="0de21-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0de21-115">-AsJob</span></span>
<span data-ttu-id="0de21-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0de21-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0de21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de21-117">-DefaultProfile</span></span>
<span data-ttu-id="0de21-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0de21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0de21-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0de21-119">-DefinitionFile</span></span>
<span data-ttu-id="0de21-120">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="0de21-120">The JSON file path.</span></span>

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

### <span data-ttu-id="0de21-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0de21-121">-Name</span></span>
<span data-ttu-id="0de21-122">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="0de21-122">The linked service name.</span></span>

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

### <span data-ttu-id="0de21-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0de21-123">-WorkspaceName</span></span>
<span data-ttu-id="0de21-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="0de21-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0de21-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0de21-125">-WorkspaceObject</span></span>
<span data-ttu-id="0de21-126">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="0de21-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0de21-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0de21-127">-Confirm</span></span>
<span data-ttu-id="0de21-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0de21-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0de21-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0de21-129">-WhatIf</span></span>
<span data-ttu-id="0de21-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0de21-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0de21-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0de21-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0de21-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de21-132">CommonParameters</span></span>
<span data-ttu-id="0de21-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de21-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de21-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0de21-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de21-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0de21-135">INPUTS</span></span>

### <span data-ttu-id="0de21-136">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0de21-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0de21-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0de21-137">OUTPUTS</span></span>

### <span data-ttu-id="0de21-138">Microsoft. Azure. Commands. sinapsi. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="0de21-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="0de21-139">Note</span><span class="sxs-lookup"><span data-stu-id="0de21-139">NOTES</span></span>

## <span data-ttu-id="0de21-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0de21-140">RELATED LINKS</span></span>