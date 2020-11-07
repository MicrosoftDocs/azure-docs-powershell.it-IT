---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3677b580629360a9f38d808af8df9ec0694bcc61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853357"
---
# <span data-ttu-id="82910-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82910-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="82910-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82910-102">SYNOPSIS</span></span>
<span data-ttu-id="82910-103">Aggiunge una definizione di criteri endpoint servizio a un criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="82910-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="82910-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82910-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82910-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82910-105">DESCRIPTION</span></span>
<span data-ttu-id="82910-106">Il cmdlet **Add-AzServiceEndpointPolicyDefinition** aggiunge una definizione di criteri endpoint del servizio al criterio.</span><span class="sxs-lookup"><span data-stu-id="82910-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="82910-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82910-107">EXAMPLES</span></span>

### <span data-ttu-id="82910-108">Esempio 1: aggiorna una definizione dei criteri endpoint del servizio in un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="82910-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="82910-109">Questo comando ha aggiornato la definizione dei criteri endpoint del servizio con Name ServiceEndpointPolicyDefinition1, Service Microsoft. storage, Service Resources subscriptions/Sub1 e Description "New Definition" che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="82910-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="82910-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82910-110">PARAMETERS</span></span>

### <span data-ttu-id="82910-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82910-111">-DefaultProfile</span></span>
<span data-ttu-id="82910-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82910-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82910-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="82910-113">-Description</span></span>
<span data-ttu-id="82910-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="82910-114">The description of the definition</span></span>

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

### <span data-ttu-id="82910-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="82910-115">-Name</span></span>
<span data-ttu-id="82910-116">Nome della definizione dei criteri di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="82910-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="82910-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="82910-117">-Service</span></span>
<span data-ttu-id="82910-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="82910-118">Name of the service</span></span>

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

### <span data-ttu-id="82910-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="82910-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="82910-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="82910-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="82910-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="82910-121">-ServiceResource</span></span>
<span data-ttu-id="82910-122">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="82910-122">List of service resources</span></span>

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

### <span data-ttu-id="82910-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82910-123">-Confirm</span></span>
<span data-ttu-id="82910-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82910-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82910-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82910-125">-WhatIf</span></span>
<span data-ttu-id="82910-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82910-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82910-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82910-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82910-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82910-128">CommonParameters</span></span>
<span data-ttu-id="82910-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82910-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82910-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82910-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82910-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82910-131">INPUTS</span></span>

### <span data-ttu-id="82910-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="82910-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="82910-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82910-133">OUTPUTS</span></span>

### <span data-ttu-id="82910-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="82910-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="82910-135">Note</span><span class="sxs-lookup"><span data-stu-id="82910-135">NOTES</span></span>

## <span data-ttu-id="82910-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82910-136">RELATED LINKS</span></span>

[<span data-ttu-id="82910-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82910-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="82910-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82910-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="82910-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82910-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="82910-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82910-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
