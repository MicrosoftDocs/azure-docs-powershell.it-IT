---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 712aa1012269c6207b078fefa3a04a46bea4c573
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202751"
---
# <span data-ttu-id="60ac2-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="60ac2-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="60ac2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="60ac2-103">Rimuove un DataSet dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="60ac2-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="60ac2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60ac2-104">SYNTAX</span></span>

### <span data-ttu-id="60ac2-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60ac2-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60ac2-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="60ac2-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60ac2-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="60ac2-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60ac2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60ac2-108">DESCRIPTION</span></span>
<span data-ttu-id="60ac2-109">Il cmdlet **Remove-AzSynapseDataset** rimuove un DataSet dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="60ac2-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="60ac2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60ac2-110">EXAMPLES</span></span>

### <span data-ttu-id="60ac2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60ac2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="60ac2-112">Questo comando rimuove il DataSet denominato ContosoDataset dall'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="60ac2-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="60ac2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60ac2-113">PARAMETERS</span></span>

### <span data-ttu-id="60ac2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60ac2-114">-AsJob</span></span>
<span data-ttu-id="60ac2-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="60ac2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60ac2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ac2-116">-DefaultProfile</span></span>
<span data-ttu-id="60ac2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60ac2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ac2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60ac2-118">-InputObject</span></span>
<span data-ttu-id="60ac2-119">Oggetto DataSet.</span><span class="sxs-lookup"><span data-stu-id="60ac2-119">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ac2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="60ac2-120">-Name</span></span>
<span data-ttu-id="60ac2-121">Nome del DataSet.</span><span class="sxs-lookup"><span data-stu-id="60ac2-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ac2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60ac2-122">-PassThru</span></span>
<span data-ttu-id="60ac2-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="60ac2-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="60ac2-124">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="60ac2-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="60ac2-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="60ac2-125">-WorkspaceName</span></span>
<span data-ttu-id="60ac2-126">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="60ac2-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="60ac2-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="60ac2-127">-WorkspaceObject</span></span>
<span data-ttu-id="60ac2-128">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="60ac2-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="60ac2-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60ac2-129">-Confirm</span></span>
<span data-ttu-id="60ac2-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60ac2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60ac2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60ac2-131">-WhatIf</span></span>
<span data-ttu-id="60ac2-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60ac2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60ac2-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60ac2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60ac2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ac2-134">CommonParameters</span></span>
<span data-ttu-id="60ac2-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60ac2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ac2-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60ac2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ac2-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60ac2-137">INPUTS</span></span>

### <span data-ttu-id="60ac2-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="60ac2-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="60ac2-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="60ac2-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="60ac2-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60ac2-140">OUTPUTS</span></span>

### <span data-ttu-id="60ac2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60ac2-141">System.Boolean</span></span>

## <span data-ttu-id="60ac2-142">Note</span><span class="sxs-lookup"><span data-stu-id="60ac2-142">NOTES</span></span>

## <span data-ttu-id="60ac2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60ac2-143">RELATED LINKS</span></span>
