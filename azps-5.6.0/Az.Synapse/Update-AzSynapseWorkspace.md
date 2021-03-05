---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 60631b8d4c42ac314268453c5dedf16893281861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995846"
---
# <span data-ttu-id="3fb3a-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fb3a-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="3fb3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb3a-103">Aggiorna un'area di lavoro di Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3fb3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fb3a-104">SYNTAX</span></span>

### <span data-ttu-id="3fb3a-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fb3a-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb3a-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fb3a-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb3a-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fb3a-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fb3a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3fb3a-108">DESCRIPTION</span></span>
<span data-ttu-id="3fb3a-109">Il cmdlet **Update-AzSynapseWorkspace** aggiorna un'area di lavoro di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3fb3a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fb3a-110">EXAMPLES</span></span>

### <span data-ttu-id="3fb3a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3fb3a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="3fb3a-112">Questo comando aggiorna i tag per l'area di lavoro specifica di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="3fb3a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3fb3a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="3fb3a-114">Questo comando aggiorna i tag per l'area di lavoro specifica di Azure Synapse Analytics tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="3fb3a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3fb3a-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="3fb3a-116">Questo comando aggiorna i tag per l'area di lavoro specifica di Azure Synapse Analytics tramite pipeline con ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="3fb3a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fb3a-117">PARAMETERS</span></span>

### <span data-ttu-id="3fb3a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fb3a-118">-AsJob</span></span>
<span data-ttu-id="3fb3a-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3fb3a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fb3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb3a-120">-DefaultProfile</span></span>
<span data-ttu-id="3fb3a-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fb3a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fb3a-122">-InputObject</span></span>
<span data-ttu-id="3fb3a-123">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb3a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3fb3a-124">-Name</span></span>
<span data-ttu-id="3fb3a-125">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb3a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fb3a-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fb3a-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb3a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fb3a-128">-ResourceId</span></span>
<span data-ttu-id="3fb3a-129">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb3a-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3fb3a-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="3fb3a-131">Nuova password SQL amministratore per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb3a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fb3a-132">-Tag</span></span>
<span data-ttu-id="3fb3a-133">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb3a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fb3a-134">-Confirm</span></span>
<span data-ttu-id="3fb3a-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb3a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb3a-136">-WhatIf</span></span>
<span data-ttu-id="3fb3a-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fb3a-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb3a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb3a-139">CommonParameters</span></span>
<span data-ttu-id="3fb3a-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb3a-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3fb3a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb3a-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="3fb3a-142">INPUTS</span></span>

### <span data-ttu-id="3fb3a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fb3a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3fb3a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fb3a-144">OUTPUTS</span></span>

### <span data-ttu-id="3fb3a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3fb3a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3fb3a-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="3fb3a-146">NOTES</span></span>

## <span data-ttu-id="3fb3a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fb3a-147">RELATED LINKS</span></span>
