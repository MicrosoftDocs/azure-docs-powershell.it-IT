---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203353"
---
# <span data-ttu-id="61337-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61337-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="61337-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61337-102">SYNOPSIS</span></span>
<span data-ttu-id="61337-103">Aggiunge una definizione di criteri endpoint servizio a un criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="61337-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="61337-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61337-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61337-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61337-105">DESCRIPTION</span></span>
<span data-ttu-id="61337-106">Il cmdlet **Add-AzServiceEndpointPolicyDefinition** aggiunge una definizione di criteri endpoint del servizio al criterio.</span><span class="sxs-lookup"><span data-stu-id="61337-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="61337-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61337-107">EXAMPLES</span></span>

### <span data-ttu-id="61337-108">Esempio 1: aggiorna una definizione dei criteri endpoint del servizio in un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="61337-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="61337-109">Questo comando ha aggiornato la definizione dei criteri endpoint del servizio con Name ServiceEndpointPolicyDefinition1, Service Microsoft. storage, Service Resources subscriptions/Sub1 e Description "New Definition" che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="61337-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="61337-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61337-110">PARAMETERS</span></span>

### <span data-ttu-id="61337-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61337-111">-DefaultProfile</span></span>
<span data-ttu-id="61337-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61337-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61337-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="61337-113">-Description</span></span>
<span data-ttu-id="61337-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="61337-114">The description of the definition</span></span>

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

### <span data-ttu-id="61337-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="61337-115">-Name</span></span>
<span data-ttu-id="61337-116">Nome della definizione dei criteri di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="61337-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="61337-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="61337-117">-Service</span></span>
<span data-ttu-id="61337-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="61337-118">Name of the service</span></span>

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

### <span data-ttu-id="61337-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="61337-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="61337-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="61337-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="61337-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="61337-121">-ServiceResource</span></span>
<span data-ttu-id="61337-122">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="61337-122">List of service resources</span></span>

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

### <span data-ttu-id="61337-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="61337-123">-Confirm</span></span>
<span data-ttu-id="61337-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61337-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61337-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61337-125">-WhatIf</span></span>
<span data-ttu-id="61337-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61337-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61337-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="61337-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61337-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61337-128">CommonParameters</span></span>
<span data-ttu-id="61337-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61337-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61337-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61337-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61337-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61337-131">INPUTS</span></span>

### <span data-ttu-id="61337-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="61337-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="61337-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61337-133">OUTPUTS</span></span>

### <span data-ttu-id="61337-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="61337-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="61337-135">Note</span><span class="sxs-lookup"><span data-stu-id="61337-135">NOTES</span></span>

## <span data-ttu-id="61337-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61337-136">RELATED LINKS</span></span>

[<span data-ttu-id="61337-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61337-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="61337-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61337-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="61337-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61337-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="61337-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="61337-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
