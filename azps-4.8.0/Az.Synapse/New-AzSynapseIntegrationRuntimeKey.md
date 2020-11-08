---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188679"
---
# <span data-ttu-id="61bf3-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="61bf3-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="61bf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="61bf3-103">Rigenera automaticamente la chiave di runtime di integrazione ospitata.</span><span class="sxs-lookup"><span data-stu-id="61bf3-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="61bf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61bf3-104">SYNTAX</span></span>

### <span data-ttu-id="61bf3-105">NewByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61bf3-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61bf3-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bf3-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bf3-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bf3-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bf3-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bf3-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bf3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61bf3-109">DESCRIPTION</span></span>
<span data-ttu-id="61bf3-110">Il cmdlet **New-AzSynapseIntegrationRuntimeKey** rigenera la chiave di runtime Integration con il nome della chiave specificato dal parametro "Key Name".</span><span class="sxs-lookup"><span data-stu-id="61bf3-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="61bf3-111">La chiave precedente non è valida.</span><span class="sxs-lookup"><span data-stu-id="61bf3-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="61bf3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61bf3-112">EXAMPLES</span></span>

### <span data-ttu-id="61bf3-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="61bf3-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="61bf3-114">Il cmdlet rigenera la chiave "authKey2" per Integration runtime denominata "test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="61bf3-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="61bf3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61bf3-115">PARAMETERS</span></span>

### <span data-ttu-id="61bf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bf3-116">-DefaultProfile</span></span>
<span data-ttu-id="61bf3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61bf3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61bf3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="61bf3-118">-Force</span></span>
<span data-ttu-id="61bf3-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="61bf3-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="61bf3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61bf3-120">-InputObject</span></span>
<span data-ttu-id="61bf3-121">Oggetto runtime di Integration.</span><span class="sxs-lookup"><span data-stu-id="61bf3-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="61bf3-122">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="61bf3-122">-KeyName</span></span>
<span data-ttu-id="61bf3-123">Nome della chiave di autenticazione del runtime di integrazione ospitata autonomamente.</span><span class="sxs-lookup"><span data-stu-id="61bf3-123">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="61bf3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="61bf3-124">-Name</span></span>
<span data-ttu-id="61bf3-125">Nome del runtime di integrazione.</span><span class="sxs-lookup"><span data-stu-id="61bf3-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="61bf3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bf3-126">-ResourceGroupName</span></span>
<span data-ttu-id="61bf3-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="61bf3-127">Resource group name.</span></span>

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

### <span data-ttu-id="61bf3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61bf3-128">-ResourceId</span></span>
<span data-ttu-id="61bf3-129">Identificatore delle risorse del runtime di integrazione delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="61bf3-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="61bf3-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61bf3-130">-WorkspaceName</span></span>
<span data-ttu-id="61bf3-131">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="61bf3-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="61bf3-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="61bf3-132">-WorkspaceObject</span></span>
<span data-ttu-id="61bf3-133">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="61bf3-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="61bf3-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61bf3-134">-Confirm</span></span>
<span data-ttu-id="61bf3-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61bf3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bf3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bf3-136">-WhatIf</span></span>
<span data-ttu-id="61bf3-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61bf3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bf3-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61bf3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bf3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bf3-139">CommonParameters</span></span>
<span data-ttu-id="61bf3-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61bf3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bf3-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61bf3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bf3-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61bf3-142">INPUTS</span></span>

### <span data-ttu-id="61bf3-143">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="61bf3-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="61bf3-144">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="61bf3-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="61bf3-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61bf3-145">OUTPUTS</span></span>

### <span data-ttu-id="61bf3-146">Microsoft. Azure. Commands. sinapsi. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="61bf3-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="61bf3-147">Note</span><span class="sxs-lookup"><span data-stu-id="61bf3-147">NOTES</span></span>

## <span data-ttu-id="61bf3-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61bf3-148">RELATED LINKS</span></span>