---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 69a9fd259350238175016b3245d22022845a9f51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677924"
---
# <span data-ttu-id="5edc8-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5edc8-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="5edc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5edc8-102">SYNOPSIS</span></span>
<span data-ttu-id="5edc8-103">Aggiorna la definizione di un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="5edc8-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="5edc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5edc8-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5edc8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5edc8-105">DESCRIPTION</span></span>
<span data-ttu-id="5edc8-106">Il cmdlet **set-AzServiceEndpointPolicyDefinition** crea una definizione di criteri per endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="5edc8-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="5edc8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5edc8-107">EXAMPLES</span></span>

### <span data-ttu-id="5edc8-108">Esempio 1: aggiorna una definizione dei criteri endpoint del servizio in un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="5edc8-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="5edc8-109">Questo comando aggiorna una definizione dei criteri di endpoint del servizio denominata Policydef1 nel criterio endpoint del servizio definito dall'oggetto $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="5edc8-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="5edc8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5edc8-110">PARAMETERS</span></span>

### <span data-ttu-id="5edc8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edc8-111">-DefaultProfile</span></span>
<span data-ttu-id="5edc8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5edc8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5edc8-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5edc8-113">-Description</span></span>
<span data-ttu-id="5edc8-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="5edc8-114">The description of the definition</span></span>

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

### <span data-ttu-id="5edc8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5edc8-115">-Name</span></span>
<span data-ttu-id="5edc8-116">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="5edc8-116">The name of the rule</span></span>

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

### <span data-ttu-id="5edc8-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="5edc8-117">-Service</span></span>
<span data-ttu-id="5edc8-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="5edc8-118">Name of the service</span></span>

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

### <span data-ttu-id="5edc8-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5edc8-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5edc8-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5edc8-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="5edc8-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="5edc8-121">-ServiceResource</span></span>
<span data-ttu-id="5edc8-122">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="5edc8-122">List of service resources</span></span>

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

### <span data-ttu-id="5edc8-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5edc8-123">-Confirm</span></span>
<span data-ttu-id="5edc8-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5edc8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5edc8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5edc8-125">-WhatIf</span></span>
<span data-ttu-id="5edc8-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5edc8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5edc8-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5edc8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5edc8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edc8-128">CommonParameters</span></span>
<span data-ttu-id="5edc8-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edc8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edc8-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edc8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edc8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5edc8-131">INPUTS</span></span>

### <span data-ttu-id="5edc8-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5edc8-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5edc8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5edc8-133">OUTPUTS</span></span>

### <span data-ttu-id="5edc8-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5edc8-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5edc8-135">Note</span><span class="sxs-lookup"><span data-stu-id="5edc8-135">NOTES</span></span>

## <span data-ttu-id="5edc8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5edc8-136">RELATED LINKS</span></span>

[<span data-ttu-id="5edc8-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5edc8-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="5edc8-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5edc8-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="5edc8-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5edc8-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="5edc8-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5edc8-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
