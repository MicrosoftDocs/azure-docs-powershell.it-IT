---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519723"
---
# <span data-ttu-id="fef8f-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fef8f-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="fef8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fef8f-102">SYNOPSIS</span></span>
<span data-ttu-id="fef8f-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="fef8f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fef8f-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef8f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fef8f-105">DESCRIPTION</span></span>
<span data-ttu-id="fef8f-106">Il cmdlet **Get-AzureRmServiceEndpointPolicyDefinition** ottiene una definizione dei criteri di endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="fef8f-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="fef8f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fef8f-107">EXAMPLES</span></span>

### <span data-ttu-id="fef8f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fef8f-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="fef8f-109">Questo comando ottiene la definizione dei criteri endpoint del servizio denominata ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="fef8f-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="fef8f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fef8f-110">PARAMETERS</span></span>

### <span data-ttu-id="fef8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef8f-111">-DefaultProfile</span></span>
<span data-ttu-id="fef8f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fef8f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef8f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fef8f-113">-Name</span></span>
<span data-ttu-id="fef8f-114">Nome della definizione dei criteri di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="fef8f-114">The name of the service endpoint policy definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef8f-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fef8f-115">-ResourceId</span></span>
<span data-ttu-id="fef8f-116">{{Fill ResourceId Description}}</span><span class="sxs-lookup"><span data-stu-id="fef8f-116">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef8f-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fef8f-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="fef8f-118">Criteri endpoint servizio</span><span class="sxs-lookup"><span data-stu-id="fef8f-118">The Service endpoint policy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fef8f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fef8f-119">-Confirm</span></span>
<span data-ttu-id="fef8f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fef8f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef8f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef8f-121">-WhatIf</span></span>
<span data-ttu-id="fef8f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fef8f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fef8f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fef8f-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef8f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef8f-124">CommonParameters</span></span>
<span data-ttu-id="fef8f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef8f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef8f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef8f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef8f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fef8f-127">INPUTS</span></span>

### <span data-ttu-id="fef8f-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fef8f-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="fef8f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fef8f-129">OUTPUTS</span></span>

### <span data-ttu-id="fef8f-130">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fef8f-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="fef8f-131">Note</span><span class="sxs-lookup"><span data-stu-id="fef8f-131">NOTES</span></span>

## <span data-ttu-id="fef8f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fef8f-132">RELATED LINKS</span></span>
