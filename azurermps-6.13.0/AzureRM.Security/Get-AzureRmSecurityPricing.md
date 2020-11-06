---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509079"
---
# <span data-ttu-id="3f00d-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="3f00d-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="3f00d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f00d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f00d-103">Ottiene i dati di livello dei prezzi per Azure Security Center per un ambito.</span><span class="sxs-lookup"><span data-stu-id="3f00d-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f00d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f00d-104">SYNTAX</span></span>

### <span data-ttu-id="3f00d-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f00d-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f00d-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="3f00d-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f00d-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="3f00d-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f00d-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3f00d-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f00d-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f00d-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f00d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f00d-110">DESCRIPTION</span></span>
<span data-ttu-id="3f00d-111">Il livello di prezzo del centro di sicurezza di Azure viene deciso per ogni ambito, con questo cmdlet è possibile ottenere i livelli di prezzo configurati.</span><span class="sxs-lookup"><span data-stu-id="3f00d-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="3f00d-112">Il livello prezzi abbonamento include tutti i gruppi di risorse sotto di esso.</span><span class="sxs-lookup"><span data-stu-id="3f00d-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="3f00d-113">Il livello di prezzo dei gruppi di risorse sovrascriverà il livello prezzi abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3f00d-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="3f00d-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f00d-114">EXAMPLES</span></span>

### <span data-ttu-id="3f00d-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f00d-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="3f00d-116">Ottiene tutti i livelli di prezzo configurati per l'abbonamento e i gruppi di risorse sotto di esso.</span><span class="sxs-lookup"><span data-stu-id="3f00d-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="3f00d-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3f00d-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="3f00d-118">Ottiene il livello di prezzo configurato per il Gorup di risorse "myService1".</span><span class="sxs-lookup"><span data-stu-id="3f00d-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="3f00d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f00d-119">PARAMETERS</span></span>

### <span data-ttu-id="3f00d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f00d-120">-DefaultProfile</span></span>
<span data-ttu-id="3f00d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f00d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f00d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f00d-122">-Name</span></span>
<span data-ttu-id="3f00d-123">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f00d-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f00d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f00d-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f00d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3f00d-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f00d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f00d-126">-ResourceId</span></span>
<span data-ttu-id="3f00d-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3f00d-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f00d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f00d-128">CommonParameters</span></span>
<span data-ttu-id="3f00d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f00d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f00d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f00d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f00d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f00d-131">INPUTS</span></span>

### <span data-ttu-id="3f00d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3f00d-132">System.String</span></span>

## <span data-ttu-id="3f00d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f00d-133">OUTPUTS</span></span>

### <span data-ttu-id="3f00d-134">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="3f00d-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="3f00d-135">Note</span><span class="sxs-lookup"><span data-stu-id="3f00d-135">NOTES</span></span>

## <span data-ttu-id="3f00d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f00d-136">RELATED LINKS</span></span>
