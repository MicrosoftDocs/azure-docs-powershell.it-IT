---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 554d3285c80370559bbedfb91430d2b6801a6f51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959501"
---
# <span data-ttu-id="71fc9-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71fc9-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="71fc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="71fc9-103">Ottiene la definizione di un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="71fc9-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="71fc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71fc9-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71fc9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="71fc9-106">Il cmdlet **Get-AzServiceEndpointPolicyDefinition ottiene** la definizione di un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="71fc9-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="71fc9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71fc9-107">EXAMPLES</span></span>

### <span data-ttu-id="71fc9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71fc9-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="71fc9-109">Questo comando recupera la definizione del criterio dell'endpoint del servizio denominata ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy la archivia nella variabile $policydef servizio.</span><span class="sxs-lookup"><span data-stu-id="71fc9-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="71fc9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71fc9-110">PARAMETERS</span></span>

### <span data-ttu-id="71fc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fc9-111">-DefaultProfile</span></span>
<span data-ttu-id="71fc9-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71fc9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71fc9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="71fc9-113">-Name</span></span>
<span data-ttu-id="71fc9-114">Nome della definizione dei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="71fc9-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="71fc9-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="71fc9-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="71fc9-116">Criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="71fc9-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="71fc9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71fc9-117">-Confirm</span></span>
<span data-ttu-id="71fc9-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71fc9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71fc9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71fc9-119">-WhatIf</span></span>
<span data-ttu-id="71fc9-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71fc9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71fc9-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71fc9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71fc9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fc9-122">CommonParameters</span></span>
<span data-ttu-id="71fc9-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71fc9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fc9-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71fc9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fc9-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="71fc9-125">INPUTS</span></span>

### <span data-ttu-id="71fc9-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="71fc9-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="71fc9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71fc9-127">OUTPUTS</span></span>

### <span data-ttu-id="71fc9-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71fc9-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="71fc9-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="71fc9-129">NOTES</span></span>

## <span data-ttu-id="71fc9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71fc9-130">RELATED LINKS</span></span>

[<span data-ttu-id="71fc9-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71fc9-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="71fc9-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71fc9-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="71fc9-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71fc9-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="71fc9-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71fc9-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
