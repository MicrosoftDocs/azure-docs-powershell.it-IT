---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340144"
---
# <span data-ttu-id="61a91-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="61a91-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="61a91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61a91-102">SYNOPSIS</span></span>
<span data-ttu-id="61a91-103">Rimuove un flusso di dati dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61a91-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="61a91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61a91-104">SYNTAX</span></span>

### <span data-ttu-id="61a91-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61a91-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a91-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="61a91-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a91-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="61a91-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a91-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61a91-108">DESCRIPTION</span></span>
<span data-ttu-id="61a91-109">Il cmdlet **Remove-AzSynapseDataFlow** rimuove un flusso di dati dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="61a91-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="61a91-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61a91-110">EXAMPLES</span></span>

### <span data-ttu-id="61a91-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61a91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="61a91-112">Questo comando rimuove il flusso di dati denominato ContosoDataFlow dall'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="61a91-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="61a91-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61a91-113">PARAMETERS</span></span>

### <span data-ttu-id="61a91-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61a91-114">-AsJob</span></span>
<span data-ttu-id="61a91-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="61a91-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61a91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a91-116">-DefaultProfile</span></span>
<span data-ttu-id="61a91-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61a91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a91-118">-Force</span><span class="sxs-lookup"><span data-stu-id="61a91-118">-Force</span></span>
<span data-ttu-id="61a91-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="61a91-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="61a91-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61a91-120">-InputObject</span></span>
<span data-ttu-id="61a91-121">Oggetto flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="61a91-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61a91-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="61a91-122">-Name</span></span>
<span data-ttu-id="61a91-123">Nome del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="61a91-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a91-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61a91-124">-PassThru</span></span>
<span data-ttu-id="61a91-125">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="61a91-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="61a91-126">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="61a91-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="61a91-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61a91-127">-WorkspaceName</span></span>
<span data-ttu-id="61a91-128">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="61a91-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a91-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="61a91-129">-WorkspaceObject</span></span>
<span data-ttu-id="61a91-130">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="61a91-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61a91-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61a91-131">-Confirm</span></span>
<span data-ttu-id="61a91-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61a91-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a91-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a91-133">-WhatIf</span></span>
<span data-ttu-id="61a91-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a91-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a91-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61a91-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a91-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a91-136">CommonParameters</span></span>
<span data-ttu-id="61a91-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a91-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a91-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61a91-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a91-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61a91-139">INPUTS</span></span>

### <span data-ttu-id="61a91-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="61a91-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="61a91-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="61a91-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="61a91-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61a91-142">OUTPUTS</span></span>

### <span data-ttu-id="61a91-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61a91-143">System.Boolean</span></span>

## <span data-ttu-id="61a91-144">Note</span><span class="sxs-lookup"><span data-stu-id="61a91-144">NOTES</span></span>

## <span data-ttu-id="61a91-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61a91-145">RELATED LINKS</span></span>
