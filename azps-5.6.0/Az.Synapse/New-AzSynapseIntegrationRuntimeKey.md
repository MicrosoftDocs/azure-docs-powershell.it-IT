---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 143238bfcc8dffc209150a675af0a982d20663bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976078"
---
# <span data-ttu-id="8b274-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="8b274-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="8b274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b274-102">SYNOPSIS</span></span>
<span data-ttu-id="8b274-103">Rigenerare la chiave di runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="8b274-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="8b274-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b274-104">SYNTAX</span></span>

### <span data-ttu-id="8b274-105">NewByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b274-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b274-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b274-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b274-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b274-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b274-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b274-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b274-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b274-109">DESCRIPTION</span></span>
<span data-ttu-id="8b274-110">Il cmdlet **New-AzSynapseIntegrationRuntimeKey** rigenera la chiave di runtime di integrazione con il nome di chiave specificato dal parametro 'KeyName'.</span><span class="sxs-lookup"><span data-stu-id="8b274-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="8b274-111">La chiave precedente non è valida.</span><span class="sxs-lookup"><span data-stu-id="8b274-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="8b274-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b274-112">EXAMPLES</span></span>

### <span data-ttu-id="8b274-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b274-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="8b274-114">Il cmdlet rigenera la chiave "authKey2" per il runtime di integrazione denominato "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="8b274-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="8b274-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b274-115">PARAMETERS</span></span>

### <span data-ttu-id="8b274-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b274-116">-DefaultProfile</span></span>
<span data-ttu-id="8b274-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b274-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b274-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8b274-118">-Force</span></span>
<span data-ttu-id="8b274-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8b274-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8b274-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b274-120">-InputObject</span></span>
<span data-ttu-id="8b274-121">Oggetto runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8b274-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8b274-122">-KeyName</span></span>
<span data-ttu-id="8b274-123">Nome della chiave di autenticazione del runtime di integrazione self-hosted.</span><span class="sxs-lookup"><span data-stu-id="8b274-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8b274-124">-Name</span></span>
<span data-ttu-id="8b274-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="8b274-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b274-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b274-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b274-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b274-128">-ResourceId</span></span>
<span data-ttu-id="8b274-129">Identificatore di risorsa del runtime di integrazione di Synapse.</span><span class="sxs-lookup"><span data-stu-id="8b274-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b274-130">-WorkspaceName</span></span>
<span data-ttu-id="8b274-131">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="8b274-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8b274-132">-WorkspaceObject</span></span>
<span data-ttu-id="8b274-133">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b274-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b274-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b274-134">-Confirm</span></span>
<span data-ttu-id="8b274-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b274-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b274-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b274-136">-WhatIf</span></span>
<span data-ttu-id="8b274-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b274-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b274-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b274-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b274-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b274-139">CommonParameters</span></span>
<span data-ttu-id="8b274-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b274-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b274-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b274-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b274-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b274-142">INPUTS</span></span>

### <span data-ttu-id="8b274-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b274-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8b274-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8b274-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8b274-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b274-145">OUTPUTS</span></span>

### <span data-ttu-id="8b274-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="8b274-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="8b274-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b274-147">NOTES</span></span>

## <span data-ttu-id="8b274-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b274-148">RELATED LINKS</span></span>
