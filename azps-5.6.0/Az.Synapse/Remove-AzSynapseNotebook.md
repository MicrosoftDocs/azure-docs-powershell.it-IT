---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 6203143eb2d386b627d0208730987709b1dd68c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983949"
---
# <span data-ttu-id="9afed-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="9afed-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="9afed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9afed-102">SYNOPSIS</span></span>
<span data-ttu-id="9afed-103">Rimuove un blocco appunti da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9afed-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="9afed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9afed-104">SYNTAX</span></span>

### <span data-ttu-id="9afed-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9afed-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9afed-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9afed-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9afed-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9afed-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9afed-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9afed-108">DESCRIPTION</span></span>
<span data-ttu-id="9afed-109">Il cmdlet **Remove-AzSynapseNotebook** rimuove un blocco appunti da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9afed-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="9afed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9afed-110">EXAMPLES</span></span>

### <span data-ttu-id="9afed-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9afed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="9afed-112">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9afed-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9afed-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9afed-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="9afed-114">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9afed-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="9afed-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9afed-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="9afed-116">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9afed-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9afed-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9afed-117">PARAMETERS</span></span>

### <span data-ttu-id="9afed-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9afed-118">-AsJob</span></span>
<span data-ttu-id="9afed-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9afed-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9afed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afed-120">-DefaultProfile</span></span>
<span data-ttu-id="9afed-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9afed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9afed-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9afed-122">-Force</span></span>
<span data-ttu-id="9afed-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9afed-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9afed-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9afed-124">-InputObject</span></span>
<span data-ttu-id="9afed-125">Oggetto blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="9afed-125">The notebook object.</span></span>

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

### <span data-ttu-id="9afed-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9afed-126">-Name</span></span>
<span data-ttu-id="9afed-127">Nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="9afed-127">The notebook name.</span></span>

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

### <span data-ttu-id="9afed-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9afed-128">-PassThru</span></span>
<span data-ttu-id="9afed-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9afed-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9afed-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9afed-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9afed-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9afed-131">-WorkspaceName</span></span>
<span data-ttu-id="9afed-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="9afed-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9afed-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9afed-133">-WorkspaceObject</span></span>
<span data-ttu-id="9afed-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9afed-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9afed-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9afed-135">-Confirm</span></span>
<span data-ttu-id="9afed-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9afed-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9afed-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9afed-137">-WhatIf</span></span>
<span data-ttu-id="9afed-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9afed-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9afed-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9afed-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9afed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afed-140">CommonParameters</span></span>
<span data-ttu-id="9afed-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9afed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afed-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9afed-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afed-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="9afed-143">INPUTS</span></span>

### <span data-ttu-id="9afed-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9afed-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9afed-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="9afed-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="9afed-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9afed-146">OUTPUTS</span></span>

### <span data-ttu-id="9afed-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9afed-147">System.Boolean</span></span>

## <span data-ttu-id="9afed-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="9afed-148">NOTES</span></span>

## <span data-ttu-id="9afed-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9afed-149">RELATED LINKS</span></span>
