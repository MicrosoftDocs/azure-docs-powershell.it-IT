---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201375"
---
# <span data-ttu-id="53b0a-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="53b0a-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="53b0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="53b0a-103">Rimuove un servizio collegato dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="53b0a-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="53b0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53b0a-104">SYNTAX</span></span>

### <span data-ttu-id="53b0a-105">RemoveByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53b0a-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b0a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="53b0a-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53b0a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="53b0a-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53b0a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53b0a-108">DESCRIPTION</span></span>
<span data-ttu-id="53b0a-109">Il cmdlet **Remove-AzSynapseLinkedService** rimuove un servizio collegato dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="53b0a-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="53b0a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53b0a-110">EXAMPLES</span></span>

### <span data-ttu-id="53b0a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53b0a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="53b0a-112">Questo comando rimuove il servizio collegato denominato ContosoLinkedService dall'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="53b0a-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="53b0a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="53b0a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="53b0a-114">Questo comando rimuove il servizio collegato denominato ContosoLinkedService dall'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="53b0a-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="53b0a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="53b0a-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="53b0a-116">Questo comando rimuove il servizio collegato denominato ContosoLinkedService dall'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="53b0a-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="53b0a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53b0a-117">PARAMETERS</span></span>

### <span data-ttu-id="53b0a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53b0a-118">-AsJob</span></span>
<span data-ttu-id="53b0a-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="53b0a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53b0a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b0a-120">-DefaultProfile</span></span>
<span data-ttu-id="53b0a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53b0a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b0a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53b0a-122">-InputObject</span></span>
<span data-ttu-id="53b0a-123">Oggetto servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="53b0a-123">The linked service object.</span></span>

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

### <span data-ttu-id="53b0a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="53b0a-124">-Name</span></span>
<span data-ttu-id="53b0a-125">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="53b0a-125">The linked service name.</span></span>

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

### <span data-ttu-id="53b0a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53b0a-126">-PassThru</span></span>
<span data-ttu-id="53b0a-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="53b0a-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="53b0a-128">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="53b0a-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="53b0a-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53b0a-129">-WorkspaceName</span></span>
<span data-ttu-id="53b0a-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="53b0a-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="53b0a-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53b0a-131">-WorkspaceObject</span></span>
<span data-ttu-id="53b0a-132">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="53b0a-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="53b0a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53b0a-133">-Confirm</span></span>
<span data-ttu-id="53b0a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53b0a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b0a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b0a-135">-WhatIf</span></span>
<span data-ttu-id="53b0a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53b0a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53b0a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53b0a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53b0a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b0a-138">CommonParameters</span></span>
<span data-ttu-id="53b0a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b0a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b0a-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53b0a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b0a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53b0a-141">INPUTS</span></span>

### <span data-ttu-id="53b0a-142">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="53b0a-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="53b0a-143">Microsoft. Azure. Commands. sinapsi. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="53b0a-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="53b0a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53b0a-144">OUTPUTS</span></span>

### <span data-ttu-id="53b0a-145">Microsoft. Azure. Commands. sinapsi. Models. PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="53b0a-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="53b0a-146">Note</span><span class="sxs-lookup"><span data-stu-id="53b0a-146">NOTES</span></span>

## <span data-ttu-id="53b0a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53b0a-147">RELATED LINKS</span></span>
