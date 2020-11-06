---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520161"
---
# <span data-ttu-id="14df8-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="14df8-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="14df8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14df8-102">SYNOPSIS</span></span>
<span data-ttu-id="14df8-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="14df8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14df8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14df8-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14df8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14df8-105">DESCRIPTION</span></span>
<span data-ttu-id="14df8-106">Il cmdlet **New-AzureRmServiceEndpointPolicyDefinition** crea una definizione di criteri per endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="14df8-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="14df8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14df8-107">EXAMPLES</span></span>

### <span data-ttu-id="14df8-108">Esempio 1: crea un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="14df8-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="14df8-109">Questo comando crea la definizione dei criteri endpoint del servizio con nome ServiceEndpointPolicyDefinition1, servizio Microsoft. storage, Service Resources subscriptions/Sub1 e Description "nuova definizione" che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policydef.</span><span class="sxs-lookup"><span data-stu-id="14df8-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="14df8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14df8-110">PARAMETERS</span></span>

### <span data-ttu-id="14df8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14df8-111">-DefaultProfile</span></span>
<span data-ttu-id="14df8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14df8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14df8-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="14df8-113">-Description</span></span>
<span data-ttu-id="14df8-114">Descrizione della definizione</span><span class="sxs-lookup"><span data-stu-id="14df8-114">The description of the definition</span></span>

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

### <span data-ttu-id="14df8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="14df8-115">-Name</span></span>
<span data-ttu-id="14df8-116">Nome del criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="14df8-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="14df8-117">-Servizio</span><span class="sxs-lookup"><span data-stu-id="14df8-117">-Service</span></span>
<span data-ttu-id="14df8-118">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="14df8-118">Name of the service</span></span>

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

### <span data-ttu-id="14df8-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="14df8-119">-ServiceResource</span></span>
<span data-ttu-id="14df8-120">Elenco delle risorse di servizio</span><span class="sxs-lookup"><span data-stu-id="14df8-120">List of service resources</span></span>

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

### <span data-ttu-id="14df8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14df8-121">CommonParameters</span></span>
<span data-ttu-id="14df8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14df8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14df8-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14df8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14df8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14df8-124">INPUTS</span></span>

### <span data-ttu-id="14df8-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14df8-125">None</span></span>


## <span data-ttu-id="14df8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14df8-126">OUTPUTS</span></span>

### <span data-ttu-id="14df8-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="14df8-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="14df8-128">Note</span><span class="sxs-lookup"><span data-stu-id="14df8-128">NOTES</span></span>

## <span data-ttu-id="14df8-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14df8-129">RELATED LINKS</span></span>
