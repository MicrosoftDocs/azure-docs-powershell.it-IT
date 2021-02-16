---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195575"
---
# <span data-ttu-id="9b1bf-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="9b1bf-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="9b1bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1bf-103">Rimuove un blocco appunti da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="9b1bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b1bf-104">SYNTAX</span></span>

### <span data-ttu-id="9b1bf-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b1bf-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b1bf-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9b1bf-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b1bf-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b1bf-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b1bf-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b1bf-108">DESCRIPTION</span></span>
<span data-ttu-id="9b1bf-109">Il cmdlet **Remove-AzSynapseNotebook** rimuove un blocco appunti da un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="9b1bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b1bf-110">EXAMPLES</span></span>

### <span data-ttu-id="9b1bf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b1bf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="9b1bf-112">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9b1bf-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9b1bf-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="9b1bf-114">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="9b1bf-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9b1bf-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="9b1bf-116">Rimuovere un blocco appunti denominato ContosoNotebook dall'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9b1bf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b1bf-117">PARAMETERS</span></span>

### <span data-ttu-id="9b1bf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b1bf-118">-AsJob</span></span>
<span data-ttu-id="9b1bf-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9b1bf-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b1bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1bf-120">-DefaultProfile</span></span>
<span data-ttu-id="9b1bf-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b1bf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9b1bf-122">-Force</span></span>
<span data-ttu-id="9b1bf-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9b1bf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b1bf-124">-InputObject</span></span>
<span data-ttu-id="9b1bf-125">Oggetto blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-125">The notebook object.</span></span>

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

### <span data-ttu-id="9b1bf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9b1bf-126">-Name</span></span>
<span data-ttu-id="9b1bf-127">Nome del blocco appunti.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-127">The notebook name.</span></span>

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

### <span data-ttu-id="9b1bf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b1bf-128">-PassThru</span></span>
<span data-ttu-id="9b1bf-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9b1bf-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9b1bf-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b1bf-131">-WorkspaceName</span></span>
<span data-ttu-id="9b1bf-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9b1bf-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9b1bf-133">-WorkspaceObject</span></span>
<span data-ttu-id="9b1bf-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9b1bf-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b1bf-135">-Confirm</span></span>
<span data-ttu-id="9b1bf-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b1bf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b1bf-137">-WhatIf</span></span>
<span data-ttu-id="9b1bf-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b1bf-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b1bf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1bf-140">CommonParameters</span></span>
<span data-ttu-id="9b1bf-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1bf-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b1bf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1bf-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b1bf-143">INPUTS</span></span>

### <span data-ttu-id="9b1bf-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9b1bf-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9b1bf-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="9b1bf-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="9b1bf-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b1bf-146">OUTPUTS</span></span>

### <span data-ttu-id="9b1bf-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b1bf-147">System.Boolean</span></span>

## <span data-ttu-id="9b1bf-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b1bf-148">NOTES</span></span>

## <span data-ttu-id="9b1bf-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b1bf-149">RELATED LINKS</span></span>
