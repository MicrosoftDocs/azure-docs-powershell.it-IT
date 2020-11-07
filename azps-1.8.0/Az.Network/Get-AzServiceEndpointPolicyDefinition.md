---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: a0e4f0c877d43ffa49737e3c3a180783a385c795
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678456"
---
# <span data-ttu-id="cac27-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cac27-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="cac27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cac27-102">SYNOPSIS</span></span>
<span data-ttu-id="cac27-103">Ottiene una definizione di criteri endpoint servizio.</span><span class="sxs-lookup"><span data-stu-id="cac27-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="cac27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cac27-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cac27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cac27-105">DESCRIPTION</span></span>
<span data-ttu-id="cac27-106">Il cmdlet **Get-AzServiceEndpointPolicyDefinition** ottiene una definizione dei criteri di endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="cac27-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="cac27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cac27-107">EXAMPLES</span></span>

### <span data-ttu-id="cac27-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cac27-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="cac27-109">Questo comando ottiene la definizione dei criteri endpoint del servizio denominata ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="cac27-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="cac27-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cac27-110">PARAMETERS</span></span>

### <span data-ttu-id="cac27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac27-111">-DefaultProfile</span></span>
<span data-ttu-id="cac27-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cac27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac27-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cac27-113">-Name</span></span>
<span data-ttu-id="cac27-114">Nome della definizione dei criteri di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="cac27-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="cac27-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cac27-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="cac27-116">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="cac27-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="cac27-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cac27-117">-Confirm</span></span>
<span data-ttu-id="cac27-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cac27-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cac27-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cac27-119">-WhatIf</span></span>
<span data-ttu-id="cac27-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cac27-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cac27-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cac27-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cac27-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac27-122">CommonParameters</span></span>
<span data-ttu-id="cac27-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac27-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac27-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cac27-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac27-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cac27-125">INPUTS</span></span>

### <span data-ttu-id="cac27-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cac27-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="cac27-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cac27-127">OUTPUTS</span></span>

### <span data-ttu-id="cac27-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cac27-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="cac27-129">Note</span><span class="sxs-lookup"><span data-stu-id="cac27-129">NOTES</span></span>

## <span data-ttu-id="cac27-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cac27-130">RELATED LINKS</span></span>

[<span data-ttu-id="cac27-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cac27-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="cac27-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cac27-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="cac27-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cac27-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="cac27-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cac27-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)