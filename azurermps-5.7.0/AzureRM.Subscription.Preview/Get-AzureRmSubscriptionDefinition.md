---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509532"
---
# <span data-ttu-id="3ec8b-101">Get-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="3ec8b-101">Get-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="3ec8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ec8b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec8b-103">Ottenere una definizione di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-103">Get a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ec8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ec8b-104">SYNTAX</span></span>

### <span data-ttu-id="3ec8b-105">Ottenere le definizioni di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-105">Get subscription definitions.</span></span>
```
Get-AzureRmSubscriptionDefinition
```

## <span data-ttu-id="3ec8b-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ec8b-106">EXAMPLES</span></span>

### <span data-ttu-id="3ec8b-107">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ec8b-107">Example 1</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="3ec8b-108">Ottiene tutte le definizioni di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-108">Gets all subscription definitions.</span></span>

### <span data-ttu-id="3ec8b-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3ec8b-109">Example 2</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="3ec8b-110">Ottiene una definizione di abbonamento con il nome MyProdSubscription2.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-110">Gets a subscription definition with the name MyProdSubscription2.</span></span>

## <span data-ttu-id="3ec8b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ec8b-111">PARAMETERS</span></span>

### <span data-ttu-id="3ec8b-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ec8b-112">-Name</span></span>
<span data-ttu-id="3ec8b-113">Nome della definizione della sottoscrizione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-113">The name of the subscription definition to retrieve.</span></span>

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

### <span data-ttu-id="3ec8b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec8b-114">CommonParameters</span></span>
<span data-ttu-id="3ec8b-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec8b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec8b-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec8b-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec8b-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ec8b-117">INPUTS</span></span>

### <span data-ttu-id="3ec8b-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ec8b-118">None</span></span>

## <span data-ttu-id="3ec8b-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ec8b-119">OUTPUTS</span></span>

### <span data-ttu-id="3ec8b-120">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SubscriptionDefinition. Models. PSSubscriptionDefinition, Microsoft. Azure. Commands. SubscriptionDefinition, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3ec8b-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition, Microsoft.Azure.Commands.SubscriptionDefinition, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3ec8b-121">Note</span><span class="sxs-lookup"><span data-stu-id="3ec8b-121">NOTES</span></span>

## <span data-ttu-id="3ec8b-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ec8b-122">RELATED LINKS</span></span>

