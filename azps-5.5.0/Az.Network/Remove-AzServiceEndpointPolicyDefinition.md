---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206563"
---
# <span data-ttu-id="f865c-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f865c-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f865c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f865c-102">SYNOPSIS</span></span>
<span data-ttu-id="f865c-103">Rimuove la definizione di un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="f865c-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="f865c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f865c-104">SYNTAX</span></span>

### <span data-ttu-id="f865c-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f865c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f865c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f865c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f865c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f865c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f865c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f865c-108">DESCRIPTION</span></span>
<span data-ttu-id="f865c-109">Il cmdlet **Remove-AzServiceEndpointPolicy** rimuove un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="f865c-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="f865c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f865c-110">EXAMPLES</span></span>

### <span data-ttu-id="f865c-111">Esempio 1: Rimuove un criterio dell'endpoint del servizio usando il nome</span><span class="sxs-lookup"><span data-stu-id="f865c-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="f865c-112">Questo comando rimuove un criterio endpoint di servizio con nome PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="f865c-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="f865c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f865c-113">PARAMETERS</span></span>

### <span data-ttu-id="f865c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f865c-114">-DefaultProfile</span></span>
<span data-ttu-id="f865c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f865c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f865c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f865c-116">-InputObject</span></span>
<span data-ttu-id="f865c-117">Oggetto definizione dei criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="f865c-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f865c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f865c-118">-Name</span></span>
<span data-ttu-id="f865c-119">Nome della definizione dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="f865c-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f865c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f865c-120">-ResourceId</span></span>
<span data-ttu-id="f865c-121">ID della definizione dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="f865c-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f865c-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f865c-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f865c-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f865c-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f865c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f865c-124">-Confirm</span></span>
<span data-ttu-id="f865c-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f865c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f865c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f865c-126">-WhatIf</span></span>
<span data-ttu-id="f865c-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f865c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f865c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f865c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f865c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f865c-129">CommonParameters</span></span>
<span data-ttu-id="f865c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f865c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f865c-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f865c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f865c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f865c-132">INPUTS</span></span>

### <span data-ttu-id="f865c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f865c-133">System.String</span></span>

### <span data-ttu-id="f865c-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f865c-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="f865c-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f865c-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f865c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f865c-136">OUTPUTS</span></span>

### <span data-ttu-id="f865c-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f865c-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f865c-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="f865c-138">NOTES</span></span>

## <span data-ttu-id="f865c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f865c-139">RELATED LINKS</span></span>

[<span data-ttu-id="f865c-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f865c-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f865c-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f865c-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f865c-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f865c-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f865c-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f865c-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
