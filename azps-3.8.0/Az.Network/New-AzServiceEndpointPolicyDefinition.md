---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 27124aa859fc9c97a74a3ed401c67de328d93884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021205"
---
# <span data-ttu-id="8fdd9-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8fdd9-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8fdd9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdd9-103">Crea una definizione di criteri endpoint servizio.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="8fdd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fdd9-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fdd9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fdd9-105">DESCRIPTION</span></span>
<span data-ttu-id="8fdd9-106">Il cmdlet **New-AzServiceEndpointPolicyDefinition** crea una definizione di criteri per endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="8fdd9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fdd9-107">EXAMPLES</span></span>

### <span data-ttu-id="8fdd9-108">Esempio 1: crea un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="8fdd9-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="8fdd9-109">Questo comando crea la definizione dei criteri endpoint del servizio con nome ServiceEndpointPolicyDefinition1, servizio Microsoft. storage, Service Resources subscriptions/Sub1 e Description "nuova definizione" che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="8fdd9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fdd9-110">PARAMETERS</span></span>

### <span data-ttu-id="8fdd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdd9-111">-DefaultProfile</span></span>
<span data-ttu-id="8fdd9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fdd9-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fdd9-113">-Description</span></span>
<span data-ttu-id="8fdd9-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="8fdd9-114">The description of the definition</span></span>

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

### <span data-ttu-id="8fdd9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fdd9-115">-Name</span></span>
<span data-ttu-id="8fdd9-116">Nome del criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="8fdd9-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="8fdd9-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="8fdd9-117">-Service</span></span>
<span data-ttu-id="8fdd9-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="8fdd9-118">Name of the service</span></span>

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

### <span data-ttu-id="8fdd9-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="8fdd9-119">-ServiceResource</span></span>
<span data-ttu-id="8fdd9-120">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="8fdd9-120">List of service resources</span></span>

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

### <span data-ttu-id="8fdd9-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8fdd9-121">-Confirm</span></span>
<span data-ttu-id="8fdd9-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fdd9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fdd9-123">-WhatIf</span></span>
<span data-ttu-id="8fdd9-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fdd9-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fdd9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdd9-126">CommonParameters</span></span>
<span data-ttu-id="8fdd9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdd9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdd9-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fdd9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdd9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fdd9-129">INPUTS</span></span>

### <span data-ttu-id="8fdd9-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8fdd9-130">None</span></span>

## <span data-ttu-id="8fdd9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fdd9-131">OUTPUTS</span></span>

### <span data-ttu-id="8fdd9-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8fdd9-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8fdd9-133">Note</span><span class="sxs-lookup"><span data-stu-id="8fdd9-133">NOTES</span></span>

## <span data-ttu-id="8fdd9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fdd9-134">RELATED LINKS</span></span>

[<span data-ttu-id="8fdd9-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8fdd9-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8fdd9-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8fdd9-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8fdd9-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8fdd9-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8fdd9-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8fdd9-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
