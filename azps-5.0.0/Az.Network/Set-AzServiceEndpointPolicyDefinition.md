---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301392"
---
# <span data-ttu-id="8199f-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8199f-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="8199f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8199f-102">SYNOPSIS</span></span>
<span data-ttu-id="8199f-103">Aggiorna la definizione di un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="8199f-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="8199f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8199f-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8199f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8199f-105">DESCRIPTION</span></span>
<span data-ttu-id="8199f-106">Il cmdlet **set-AzServiceEndpointPolicyDefinition** crea una definizione di criteri per endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="8199f-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="8199f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8199f-107">EXAMPLES</span></span>

### <span data-ttu-id="8199f-108">Esempio 1: aggiorna una definizione dei criteri endpoint del servizio in un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="8199f-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="8199f-109">Questo comando aggiorna una definizione dei criteri di endpoint del servizio denominata Policydef1 nel criterio endpoint del servizio definito dall'oggetto $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="8199f-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="8199f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8199f-110">PARAMETERS</span></span>

### <span data-ttu-id="8199f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8199f-111">-DefaultProfile</span></span>
<span data-ttu-id="8199f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8199f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8199f-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8199f-113">-Description</span></span>
<span data-ttu-id="8199f-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="8199f-114">The description of the definition</span></span>

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

### <span data-ttu-id="8199f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8199f-115">-Name</span></span>
<span data-ttu-id="8199f-116">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="8199f-116">The name of the rule</span></span>

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

### <span data-ttu-id="8199f-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="8199f-117">-Service</span></span>
<span data-ttu-id="8199f-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="8199f-118">Name of the service</span></span>

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

### <span data-ttu-id="8199f-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8199f-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="8199f-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8199f-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="8199f-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="8199f-121">-ServiceResource</span></span>
<span data-ttu-id="8199f-122">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="8199f-122">List of service resources</span></span>

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

### <span data-ttu-id="8199f-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8199f-123">-Confirm</span></span>
<span data-ttu-id="8199f-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8199f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8199f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8199f-125">-WhatIf</span></span>
<span data-ttu-id="8199f-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8199f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8199f-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8199f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8199f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8199f-128">CommonParameters</span></span>
<span data-ttu-id="8199f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8199f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8199f-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8199f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8199f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8199f-131">INPUTS</span></span>

### <span data-ttu-id="8199f-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8199f-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8199f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8199f-133">OUTPUTS</span></span>

### <span data-ttu-id="8199f-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8199f-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8199f-135">Note</span><span class="sxs-lookup"><span data-stu-id="8199f-135">NOTES</span></span>

## <span data-ttu-id="8199f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8199f-136">RELATED LINKS</span></span>

[<span data-ttu-id="8199f-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8199f-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8199f-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8199f-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8199f-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8199f-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="8199f-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8199f-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
