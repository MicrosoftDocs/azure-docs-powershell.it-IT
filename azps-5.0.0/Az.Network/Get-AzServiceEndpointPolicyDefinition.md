---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302076"
---
# <span data-ttu-id="b0afd-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b0afd-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b0afd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0afd-102">SYNOPSIS</span></span>
<span data-ttu-id="b0afd-103">Ottiene una definizione di criteri endpoint servizio.</span><span class="sxs-lookup"><span data-stu-id="b0afd-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="b0afd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0afd-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0afd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0afd-105">DESCRIPTION</span></span>
<span data-ttu-id="b0afd-106">Il cmdlet **Get-AzServiceEndpointPolicyDefinition** ottiene una definizione dei criteri di endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="b0afd-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="b0afd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0afd-107">EXAMPLES</span></span>

### <span data-ttu-id="b0afd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0afd-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="b0afd-109">Questo comando ottiene la definizione dei criteri endpoint del servizio denominata ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="b0afd-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="b0afd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0afd-110">PARAMETERS</span></span>

### <span data-ttu-id="b0afd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0afd-111">-DefaultProfile</span></span>
<span data-ttu-id="b0afd-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0afd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0afd-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0afd-113">-Name</span></span>
<span data-ttu-id="b0afd-114">Nome della definizione dei criteri di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="b0afd-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="b0afd-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b0afd-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b0afd-116">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="b0afd-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="b0afd-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0afd-117">-Confirm</span></span>
<span data-ttu-id="b0afd-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0afd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0afd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0afd-119">-WhatIf</span></span>
<span data-ttu-id="b0afd-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0afd-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0afd-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0afd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0afd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0afd-122">CommonParameters</span></span>
<span data-ttu-id="b0afd-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0afd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0afd-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0afd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0afd-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0afd-125">INPUTS</span></span>

### <span data-ttu-id="b0afd-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b0afd-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="b0afd-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0afd-127">OUTPUTS</span></span>

### <span data-ttu-id="b0afd-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b0afd-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="b0afd-129">Note</span><span class="sxs-lookup"><span data-stu-id="b0afd-129">NOTES</span></span>

## <span data-ttu-id="b0afd-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0afd-130">RELATED LINKS</span></span>

[<span data-ttu-id="b0afd-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b0afd-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b0afd-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b0afd-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b0afd-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b0afd-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="b0afd-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b0afd-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
