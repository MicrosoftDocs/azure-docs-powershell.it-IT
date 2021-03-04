---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 9a9795547a1d9699a185ae8957852b41d26ca321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979773"
---
# <span data-ttu-id="f60a2-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f60a2-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f60a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f60a2-103">Aggiunge una definizione di criterio dell'endpoint del servizio a un criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="f60a2-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="f60a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f60a2-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f60a2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f60a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f60a2-106">Il cmdlet **Add-AzServiceEndpointPolicyDefinition** aggiunge una definizione di criterio dell'endpoint del servizio al criterio.</span><span class="sxs-lookup"><span data-stu-id="f60a2-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="f60a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f60a2-107">EXAMPLES</span></span>

### <span data-ttu-id="f60a2-108">Esempio 1: Aggiorna la definizione di un criterio endpoint del servizio nei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="f60a2-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="f60a2-109">Questo comando ha aggiornato la definizione dei criteri dell'endpoint del servizio con il nome ServiceEndpointPolicyDefinition1, il servizio Microsoft.Storage, le sottoscrizioni delle risorse di servizio/sub1 e la descrizione "Nuova definizione" che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="f60a2-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="f60a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f60a2-110">PARAMETERS</span></span>

### <span data-ttu-id="f60a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60a2-111">-DefaultProfile</span></span>
<span data-ttu-id="f60a2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f60a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f60a2-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f60a2-113">-Description</span></span>
<span data-ttu-id="f60a2-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="f60a2-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60a2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f60a2-115">-Name</span></span>
<span data-ttu-id="f60a2-116">Nome della definizione dei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="f60a2-116">The name of the service endpoint policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60a2-117">-Service</span><span class="sxs-lookup"><span data-stu-id="f60a2-117">-Service</span></span>
<span data-ttu-id="f60a2-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="f60a2-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60a2-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f60a2-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f60a2-120">Il ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f60a2-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="f60a2-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="f60a2-121">-ServiceResource</span></span>
<span data-ttu-id="f60a2-122">Elenco delle risorse per i servizi</span><span class="sxs-lookup"><span data-stu-id="f60a2-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60a2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f60a2-123">-Confirm</span></span>
<span data-ttu-id="f60a2-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f60a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f60a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f60a2-125">-WhatIf</span></span>
<span data-ttu-id="f60a2-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60a2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f60a2-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f60a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f60a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60a2-128">CommonParameters</span></span>
<span data-ttu-id="f60a2-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f60a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60a2-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60a2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60a2-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="f60a2-131">INPUTS</span></span>

### <span data-ttu-id="f60a2-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f60a2-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f60a2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f60a2-133">OUTPUTS</span></span>

### <span data-ttu-id="f60a2-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f60a2-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f60a2-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="f60a2-135">NOTES</span></span>

## <span data-ttu-id="f60a2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f60a2-136">RELATED LINKS</span></span>

[<span data-ttu-id="f60a2-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f60a2-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f60a2-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f60a2-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f60a2-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f60a2-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f60a2-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f60a2-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
