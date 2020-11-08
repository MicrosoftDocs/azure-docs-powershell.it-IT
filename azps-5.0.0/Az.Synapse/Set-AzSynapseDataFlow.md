---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203216"
---
# <span data-ttu-id="7e0a6-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="7e0a6-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="7e0a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0a6-103">Crea o aggiorna un flusso di dati nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="7e0a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e0a6-104">SYNTAX</span></span>

### <span data-ttu-id="7e0a6-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e0a6-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e0a6-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="7e0a6-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e0a6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e0a6-107">DESCRIPTION</span></span>
<span data-ttu-id="7e0a6-108">Il cmdlet **set-AzSynapseDataFlow** crea un flusso di dati o aggiorna un flusso di dati esistente nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="7e0a6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e0a6-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0a6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e0a6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="7e0a6-111">Questo comando crea un flusso di dati denominato ContosoDataFlow nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="7e0a6-112">Il comando basa il flusso di dati sulle informazioni nella DataFlow.jssu file.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="7e0a6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e0a6-113">PARAMETERS</span></span>

### <span data-ttu-id="7e0a6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e0a6-114">-AsJob</span></span>
<span data-ttu-id="7e0a6-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7e0a6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e0a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0a6-116">-DefaultProfile</span></span>
<span data-ttu-id="7e0a6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0a6-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7e0a6-118">-DefinitionFile</span></span>
<span data-ttu-id="7e0a6-119">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-119">The JSON file path.</span></span>

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

### <span data-ttu-id="7e0a6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e0a6-120">-Name</span></span>
<span data-ttu-id="7e0a6-121">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0a6-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e0a6-122">-WorkspaceName</span></span>
<span data-ttu-id="7e0a6-123">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7e0a6-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7e0a6-124">-WorkspaceObject</span></span>
<span data-ttu-id="7e0a6-125">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7e0a6-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e0a6-126">-Confirm</span></span>
<span data-ttu-id="7e0a6-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e0a6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e0a6-128">-WhatIf</span></span>
<span data-ttu-id="7e0a6-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e0a6-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e0a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0a6-131">CommonParameters</span></span>
<span data-ttu-id="7e0a6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0a6-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e0a6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0a6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e0a6-134">INPUTS</span></span>

### <span data-ttu-id="7e0a6-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e0a6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7e0a6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e0a6-136">OUTPUTS</span></span>

### <span data-ttu-id="7e0a6-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="7e0a6-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="7e0a6-138">Note</span><span class="sxs-lookup"><span data-stu-id="7e0a6-138">NOTES</span></span>

## <span data-ttu-id="7e0a6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e0a6-139">RELATED LINKS</span></span>
