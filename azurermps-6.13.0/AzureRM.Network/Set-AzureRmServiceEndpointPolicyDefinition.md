---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686376"
---
# <span data-ttu-id="1a412-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1a412-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1a412-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a412-102">SYNOPSIS</span></span>
<span data-ttu-id="1a412-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="1a412-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a412-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a412-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a412-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a412-105">DESCRIPTION</span></span>
<span data-ttu-id="1a412-106">Il cmdlet **set-AzureRmServiceEndpointPolicyDefinition** crea una definizione di criteri per endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="1a412-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="1a412-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a412-107">EXAMPLES</span></span>

### <span data-ttu-id="1a412-108">Esempio 1: aggiorna una definizione dei criteri endpoint del servizio in un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="1a412-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="1a412-109">Questo comando aggiorna una definizione dei criteri di endpoint del servizio denominata Policydef1 nel criterio endpoint del servizio definito dall'oggetto $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="1a412-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="1a412-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a412-110">PARAMETERS</span></span>

### <span data-ttu-id="1a412-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a412-111">-DefaultProfile</span></span>
<span data-ttu-id="1a412-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a412-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a412-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a412-113">-Description</span></span>
<span data-ttu-id="1a412-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="1a412-114">The description of the definition</span></span>

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

### <span data-ttu-id="1a412-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a412-115">-Name</span></span>
<span data-ttu-id="1a412-116">Nome della regola</span><span class="sxs-lookup"><span data-stu-id="1a412-116">The name of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a412-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="1a412-117">-Service</span></span>
<span data-ttu-id="1a412-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="1a412-118">Name of the service</span></span>

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

### <span data-ttu-id="1a412-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1a412-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="1a412-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1a412-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="1a412-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="1a412-121">-ServiceResource</span></span>
<span data-ttu-id="1a412-122">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="1a412-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a412-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a412-123">CommonParameters</span></span>
<span data-ttu-id="1a412-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a412-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1a412-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a412-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a412-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a412-126">INPUTS</span></span>

### <span data-ttu-id="1a412-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1a412-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="1a412-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a412-128">OUTPUTS</span></span>

### <span data-ttu-id="1a412-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1a412-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="1a412-130">Note</span><span class="sxs-lookup"><span data-stu-id="1a412-130">NOTES</span></span>

## <span data-ttu-id="1a412-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a412-131">RELATED LINKS</span></span>
