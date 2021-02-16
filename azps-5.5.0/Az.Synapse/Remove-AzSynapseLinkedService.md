---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195590"
---
# <span data-ttu-id="9e643-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="9e643-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="9e643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e643-102">SYNOPSIS</span></span>
<span data-ttu-id="9e643-103">Rimuove un servizio collegato dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9e643-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="9e643-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e643-104">SYNTAX</span></span>

### <span data-ttu-id="9e643-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e643-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e643-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9e643-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e643-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e643-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e643-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e643-108">DESCRIPTION</span></span>
<span data-ttu-id="9e643-109">Il cmdlet **Remove-AzSynapseLinkedService** rimuove un servizio collegato dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9e643-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="9e643-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e643-110">EXAMPLES</span></span>

### <span data-ttu-id="9e643-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e643-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="9e643-112">Questo comando rimuove il servizio collegato denominato ContosoLinkedService dall'area di lavoro contosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9e643-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9e643-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9e643-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="9e643-114">Questo comando rimuove il servizio collegato denominato ContosoLinkedService dall'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e643-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="9e643-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9e643-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="9e643-116">Questo comando rimuove il servizio collegato denominato ContosoLinkedService dall'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e643-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9e643-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e643-117">PARAMETERS</span></span>

### <span data-ttu-id="9e643-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e643-118">-AsJob</span></span>
<span data-ttu-id="9e643-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9e643-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e643-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e643-120">-DefaultProfile</span></span>
<span data-ttu-id="9e643-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e643-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e643-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9e643-122">-Force</span></span>
<span data-ttu-id="9e643-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9e643-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9e643-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e643-124">-InputObject</span></span>
<span data-ttu-id="9e643-125">Oggetto servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="9e643-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e643-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9e643-126">-Name</span></span>
<span data-ttu-id="9e643-127">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="9e643-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e643-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e643-128">-PassThru</span></span>
<span data-ttu-id="9e643-129">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9e643-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9e643-130">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9e643-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9e643-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e643-131">-WorkspaceName</span></span>
<span data-ttu-id="9e643-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e643-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e643-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9e643-133">-WorkspaceObject</span></span>
<span data-ttu-id="9e643-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e643-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e643-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e643-135">-Confirm</span></span>
<span data-ttu-id="9e643-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e643-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e643-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e643-137">-WhatIf</span></span>
<span data-ttu-id="9e643-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e643-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e643-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e643-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e643-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e643-140">CommonParameters</span></span>
<span data-ttu-id="9e643-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e643-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e643-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e643-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e643-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e643-143">INPUTS</span></span>

### <span data-ttu-id="9e643-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e643-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9e643-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="9e643-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="9e643-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e643-146">OUTPUTS</span></span>

### <span data-ttu-id="9e643-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="9e643-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="9e643-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e643-148">NOTES</span></span>

## <span data-ttu-id="9e643-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e643-149">RELATED LINKS</span></span>
