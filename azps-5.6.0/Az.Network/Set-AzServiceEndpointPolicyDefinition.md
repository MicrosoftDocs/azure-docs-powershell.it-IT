---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: bc68a57437bae2af10b5ee39221459aebf82a2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010301"
---
# <span data-ttu-id="7769a-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7769a-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="7769a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7769a-102">SYNOPSIS</span></span>
<span data-ttu-id="7769a-103">Aggiorna la definizione di un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="7769a-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="7769a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7769a-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7769a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7769a-105">DESCRIPTION</span></span>
<span data-ttu-id="7769a-106">Il cmdlet **Set-AzServiceEndpointPolicyDefinition crea** una definizione di criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="7769a-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="7769a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7769a-107">EXAMPLES</span></span>

### <span data-ttu-id="7769a-108">Esempio 1: Aggiorna la definizione di un criterio endpoint del servizio nei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="7769a-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="7769a-109">Questo comando aggiorna la definizione di un criterio endpoint del servizio denominato Policydef1 nel criterio dell'endpoint di servizio definito dall'oggetto $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="7769a-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="7769a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7769a-110">PARAMETERS</span></span>

### <span data-ttu-id="7769a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7769a-111">-DefaultProfile</span></span>
<span data-ttu-id="7769a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7769a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7769a-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7769a-113">-Description</span></span>
<span data-ttu-id="7769a-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="7769a-114">The description of the definition</span></span>

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

### <span data-ttu-id="7769a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7769a-115">-Name</span></span>
<span data-ttu-id="7769a-116">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="7769a-116">The name of the rule</span></span>

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

### <span data-ttu-id="7769a-117">-Service</span><span class="sxs-lookup"><span data-stu-id="7769a-117">-Service</span></span>
<span data-ttu-id="7769a-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="7769a-118">Name of the service</span></span>

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

### <span data-ttu-id="7769a-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7769a-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="7769a-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7769a-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="7769a-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="7769a-121">-ServiceResource</span></span>
<span data-ttu-id="7769a-122">Elenco delle risorse per i servizi</span><span class="sxs-lookup"><span data-stu-id="7769a-122">List of service resources</span></span>

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

### <span data-ttu-id="7769a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7769a-123">-Confirm</span></span>
<span data-ttu-id="7769a-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7769a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7769a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7769a-125">-WhatIf</span></span>
<span data-ttu-id="7769a-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7769a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7769a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7769a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7769a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7769a-128">CommonParameters</span></span>
<span data-ttu-id="7769a-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7769a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7769a-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7769a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7769a-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="7769a-131">INPUTS</span></span>

### <span data-ttu-id="7769a-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7769a-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="7769a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7769a-133">OUTPUTS</span></span>

### <span data-ttu-id="7769a-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7769a-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="7769a-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="7769a-135">NOTES</span></span>

## <span data-ttu-id="7769a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7769a-136">RELATED LINKS</span></span>

[<span data-ttu-id="7769a-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7769a-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7769a-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7769a-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7769a-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7769a-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7769a-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7769a-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
