---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191421"
---
# <span data-ttu-id="54d48-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54d48-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="54d48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54d48-102">SYNOPSIS</span></span>
<span data-ttu-id="54d48-103">Elimina un'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="54d48-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="54d48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54d48-104">SYNTAX</span></span>

### <span data-ttu-id="54d48-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54d48-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d48-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54d48-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d48-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54d48-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d48-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54d48-108">DESCRIPTION</span></span>
<span data-ttu-id="54d48-109">Il cmdlet **Remove-AzSynapseWorkspace** Elimina definitivamente un'area di lavoro di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="54d48-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="54d48-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54d48-110">EXAMPLES</span></span>

### <span data-ttu-id="54d48-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54d48-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="54d48-112">Questo comando Elimina un'area di lavoro di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="54d48-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="54d48-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="54d48-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="54d48-114">Questo comando Elimina un'area di lavoro di analisi di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="54d48-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="54d48-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="54d48-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="54d48-116">Questo comando Elimina un'area di lavoro di analisi di Azure sinapsi tramite pipeline con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="54d48-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="54d48-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54d48-117">PARAMETERS</span></span>

### <span data-ttu-id="54d48-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54d48-118">-AsJob</span></span>
<span data-ttu-id="54d48-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="54d48-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54d48-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d48-120">-DefaultProfile</span></span>
<span data-ttu-id="54d48-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54d48-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54d48-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54d48-122">-InputObject</span></span>
<span data-ttu-id="54d48-123">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="54d48-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54d48-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="54d48-124">-Name</span></span>
<span data-ttu-id="54d48-125">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="54d48-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d48-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54d48-126">-PassThru</span></span>
<span data-ttu-id="54d48-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="54d48-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="54d48-128">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="54d48-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="54d48-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d48-129">-ResourceGroupName</span></span>
<span data-ttu-id="54d48-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54d48-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d48-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54d48-131">-ResourceId</span></span>
<span data-ttu-id="54d48-132">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="54d48-132">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d48-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54d48-133">-Confirm</span></span>
<span data-ttu-id="54d48-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d48-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d48-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d48-135">-WhatIf</span></span>
<span data-ttu-id="54d48-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54d48-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54d48-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54d48-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d48-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d48-138">CommonParameters</span></span>
<span data-ttu-id="54d48-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d48-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d48-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54d48-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d48-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54d48-141">INPUTS</span></span>

### <span data-ttu-id="54d48-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54d48-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="54d48-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54d48-143">OUTPUTS</span></span>

### <span data-ttu-id="54d48-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54d48-144">System.Boolean</span></span>

## <span data-ttu-id="54d48-145">Note</span><span class="sxs-lookup"><span data-stu-id="54d48-145">NOTES</span></span>

## <span data-ttu-id="54d48-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54d48-146">RELATED LINKS</span></span>
