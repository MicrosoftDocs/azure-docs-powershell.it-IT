---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030215"
---
# <span data-ttu-id="33b23-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="33b23-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="33b23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33b23-102">SYNOPSIS</span></span>
<span data-ttu-id="33b23-103">Delega offerta.</span><span class="sxs-lookup"><span data-stu-id="33b23-103">Offer delegation.</span></span>

## <span data-ttu-id="33b23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33b23-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="33b23-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33b23-105">DESCRIPTION</span></span>
<span data-ttu-id="33b23-106">Delega offerta.</span><span class="sxs-lookup"><span data-stu-id="33b23-106">Offer delegation.</span></span>

## <span data-ttu-id="33b23-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33b23-107">EXAMPLES</span></span>

### <span data-ttu-id="33b23-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33b23-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="33b23-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="33b23-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="33b23-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33b23-110">PARAMETERS</span></span>

### <span data-ttu-id="33b23-111">-ID</span><span class="sxs-lookup"><span data-stu-id="33b23-111">-Id</span></span>
<span data-ttu-id="33b23-112">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="33b23-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b23-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="33b23-113">-Location</span></span>
<span data-ttu-id="33b23-114">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="33b23-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b23-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="33b23-115">-Name</span></span>
<span data-ttu-id="33b23-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="33b23-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b23-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33b23-117">-SubscriptionId</span></span>
<span data-ttu-id="33b23-118">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="33b23-118">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b23-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="33b23-119">-Tags</span></span>
<span data-ttu-id="33b23-120">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="33b23-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b23-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="33b23-121">-Type</span></span>
<span data-ttu-id="33b23-122">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="33b23-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b23-123">CommonParameters</span></span>
<span data-ttu-id="33b23-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b23-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b23-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b23-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33b23-126">INPUTS</span></span>

## <span data-ttu-id="33b23-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33b23-127">OUTPUTS</span></span>

## <span data-ttu-id="33b23-128">Note</span><span class="sxs-lookup"><span data-stu-id="33b23-128">NOTES</span></span>

## <span data-ttu-id="33b23-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33b23-129">RELATED LINKS</span></span>

