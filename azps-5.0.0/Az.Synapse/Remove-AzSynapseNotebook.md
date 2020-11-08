---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201390"
---
# <span data-ttu-id="969eb-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="969eb-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="969eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="969eb-102">SYNOPSIS</span></span>
<span data-ttu-id="969eb-103">Rimuove un blocco appunti da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="969eb-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="969eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="969eb-104">SYNTAX</span></span>

### <span data-ttu-id="969eb-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="969eb-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969eb-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="969eb-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969eb-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="969eb-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969eb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="969eb-108">DESCRIPTION</span></span>
<span data-ttu-id="969eb-109">Il cmdlet **Remove-AzSynapseNotebook** rimuove un blocco appunti da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="969eb-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="969eb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="969eb-110">EXAMPLES</span></span>

### <span data-ttu-id="969eb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="969eb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="969eb-112">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="969eb-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="969eb-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="969eb-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="969eb-114">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="969eb-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="969eb-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="969eb-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="969eb-116">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="969eb-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="969eb-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="969eb-117">PARAMETERS</span></span>

### <span data-ttu-id="969eb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="969eb-118">-AsJob</span></span>
<span data-ttu-id="969eb-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="969eb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="969eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969eb-120">-DefaultProfile</span></span>
<span data-ttu-id="969eb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="969eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="969eb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="969eb-122">-InputObject</span></span>
<span data-ttu-id="969eb-123">Oggetto blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="969eb-123">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="969eb-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="969eb-124">-Name</span></span>
<span data-ttu-id="969eb-125">Il nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="969eb-125">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969eb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="969eb-126">-PassThru</span></span>
<span data-ttu-id="969eb-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="969eb-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="969eb-128">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="969eb-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="969eb-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="969eb-129">-WorkspaceName</span></span>
<span data-ttu-id="969eb-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="969eb-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="969eb-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="969eb-131">-WorkspaceObject</span></span>
<span data-ttu-id="969eb-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="969eb-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="969eb-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="969eb-133">-Confirm</span></span>
<span data-ttu-id="969eb-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="969eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="969eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969eb-135">-WhatIf</span></span>
<span data-ttu-id="969eb-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="969eb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="969eb-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="969eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="969eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969eb-138">CommonParameters</span></span>
<span data-ttu-id="969eb-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969eb-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="969eb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969eb-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="969eb-141">INPUTS</span></span>

### <span data-ttu-id="969eb-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="969eb-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="969eb-143">Microsoft. Azure. Commands. sinapsi. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="969eb-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="969eb-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="969eb-144">OUTPUTS</span></span>

### <span data-ttu-id="969eb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="969eb-145">System.Boolean</span></span>

## <span data-ttu-id="969eb-146">Note</span><span class="sxs-lookup"><span data-stu-id="969eb-146">NOTES</span></span>

## <span data-ttu-id="969eb-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="969eb-147">RELATED LINKS</span></span>
