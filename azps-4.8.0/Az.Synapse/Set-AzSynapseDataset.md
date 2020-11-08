---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191416"
---
# <span data-ttu-id="cd9bb-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="cd9bb-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="cd9bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9bb-103">Crea o aggiorna un DataSet nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="cd9bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd9bb-104">SYNTAX</span></span>

### <span data-ttu-id="cd9bb-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd9bb-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9bb-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="cd9bb-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd9bb-107">DESCRIPTION</span></span>
<span data-ttu-id="cd9bb-108">Il cmdlet **set-AzSynapseDataset** crea un DataSet o aggiorna un set di dati esistente nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="cd9bb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd9bb-109">EXAMPLES</span></span>

### <span data-ttu-id="cd9bb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd9bb-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="cd9bb-111">Questo comando crea un DataSet denominato ContosoDataset nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="cd9bb-112">Il comando basa il DataSet sulle informazioni nella Dataset.jssu file.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="cd9bb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd9bb-113">PARAMETERS</span></span>

### <span data-ttu-id="cd9bb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd9bb-114">-AsJob</span></span>
<span data-ttu-id="cd9bb-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd9bb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd9bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9bb-116">-DefaultProfile</span></span>
<span data-ttu-id="cd9bb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd9bb-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="cd9bb-118">-DefinitionFile</span></span>
<span data-ttu-id="cd9bb-119">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-119">The JSON file path.</span></span>

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

### <span data-ttu-id="cd9bb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd9bb-120">-Name</span></span>
<span data-ttu-id="cd9bb-121">Nome del DataSet.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9bb-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cd9bb-122">-WorkspaceName</span></span>
<span data-ttu-id="cd9bb-123">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cd9bb-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cd9bb-124">-WorkspaceObject</span></span>
<span data-ttu-id="cd9bb-125">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cd9bb-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd9bb-126">-Confirm</span></span>
<span data-ttu-id="cd9bb-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9bb-128">-WhatIf</span></span>
<span data-ttu-id="cd9bb-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9bb-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9bb-131">CommonParameters</span></span>
<span data-ttu-id="cd9bb-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd9bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9bb-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd9bb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9bb-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd9bb-134">INPUTS</span></span>

### <span data-ttu-id="cd9bb-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd9bb-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cd9bb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd9bb-136">OUTPUTS</span></span>

### <span data-ttu-id="cd9bb-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="cd9bb-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="cd9bb-138">Note</span><span class="sxs-lookup"><span data-stu-id="cd9bb-138">NOTES</span></span>

## <span data-ttu-id="cd9bb-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd9bb-139">RELATED LINKS</span></span>