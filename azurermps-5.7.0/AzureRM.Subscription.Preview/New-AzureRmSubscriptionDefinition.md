---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519819"
---
# <span data-ttu-id="1f98a-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="1f98a-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="1f98a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f98a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f98a-103">Crea una definizione di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1f98a-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f98a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f98a-104">SYNTAX</span></span>

### <span data-ttu-id="1f98a-105">Creare una definizione di abbonamento</span><span class="sxs-lookup"><span data-stu-id="1f98a-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="1f98a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f98a-106">DESCRIPTION</span></span>
<span data-ttu-id="1f98a-107">Il cmdlet **New-AzureRmSubscriptionDefinition** crea una definizione di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1f98a-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="1f98a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f98a-108">EXAMPLES</span></span>

### <span data-ttu-id="1f98a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f98a-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="1f98a-110">Crea una definizione di abbonamento con un nome visualizzato dell'abbonamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="1f98a-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="1f98a-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1f98a-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="1f98a-112">Crea una definizione di abbonamento con un nome visualizzato dell'abbonamento personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1f98a-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="1f98a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f98a-113">PARAMETERS</span></span>

### <span data-ttu-id="1f98a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f98a-114">-Name</span></span>
<span data-ttu-id="1f98a-115">Nome della definizione della sottoscrizione da creare.</span><span class="sxs-lookup"><span data-stu-id="1f98a-115">The name of the subscription definition to create.</span></span>

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

### <span data-ttu-id="1f98a-116">-OfferType</span><span class="sxs-lookup"><span data-stu-id="1f98a-116">-OfferType</span></span>
<span data-ttu-id="1f98a-117">Tipo di offerta da usare per la creazione dell'abbonamento sottostante.</span><span class="sxs-lookup"><span data-stu-id="1f98a-117">The type of offer to use when creating the underlying subscription.</span></span>

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

### <span data-ttu-id="1f98a-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="1f98a-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="1f98a-119">Nome visualizzato da usare quando si crea l'abbonamento sottostante alla definizione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1f98a-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f98a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f98a-120">CommonParameters</span></span>
<span data-ttu-id="1f98a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f98a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f98a-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f98a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f98a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f98a-123">INPUTS</span></span>

### <span data-ttu-id="1f98a-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f98a-124">None</span></span>

## <span data-ttu-id="1f98a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f98a-125">OUTPUTS</span></span>

### <span data-ttu-id="1f98a-126">Microsoft. Azure. Commands. SubscriptionDefinition. Models. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="1f98a-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="1f98a-127">Note</span><span class="sxs-lookup"><span data-stu-id="1f98a-127">NOTES</span></span>

## <span data-ttu-id="1f98a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f98a-128">RELATED LINKS</span></span>

