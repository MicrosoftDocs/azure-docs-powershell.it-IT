---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859521"
---
# <span data-ttu-id="28eb9-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="28eb9-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="28eb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="28eb9-103">Delega offerta.</span><span class="sxs-lookup"><span data-stu-id="28eb9-103">Offer delegation.</span></span>

## <span data-ttu-id="28eb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28eb9-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="28eb9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="28eb9-106">Delega offerta.</span><span class="sxs-lookup"><span data-stu-id="28eb9-106">Offer delegation.</span></span>

## <span data-ttu-id="28eb9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="28eb9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28eb9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="28eb9-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="28eb9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="28eb9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28eb9-110">PARAMETERS</span></span>

### <span data-ttu-id="28eb9-111">-ID</span><span class="sxs-lookup"><span data-stu-id="28eb9-111">-Id</span></span>
<span data-ttu-id="28eb9-112">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="28eb9-112">URI of the resource.</span></span>

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

### <span data-ttu-id="28eb9-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="28eb9-113">-Location</span></span>
<span data-ttu-id="28eb9-114">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="28eb9-114">Location of the resource.</span></span>

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

### <span data-ttu-id="28eb9-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="28eb9-115">-Name</span></span>
<span data-ttu-id="28eb9-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="28eb9-116">Name of the resource.</span></span>

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

### <span data-ttu-id="28eb9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28eb9-117">-SubscriptionId</span></span>
<span data-ttu-id="28eb9-118">Identificatore dell'abbonamento che riceve l'offerta delegata.</span><span class="sxs-lookup"><span data-stu-id="28eb9-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="28eb9-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="28eb9-119">-Tags</span></span>
<span data-ttu-id="28eb9-120">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="28eb9-120">List of key-value pairs.</span></span>

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

### <span data-ttu-id="28eb9-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="28eb9-121">-Type</span></span>
<span data-ttu-id="28eb9-122">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="28eb9-122">Type of resource.</span></span>

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

### <span data-ttu-id="28eb9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28eb9-123">CommonParameters</span></span>
<span data-ttu-id="28eb9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28eb9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28eb9-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28eb9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28eb9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28eb9-126">INPUTS</span></span>

## <span data-ttu-id="28eb9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28eb9-127">OUTPUTS</span></span>

## <span data-ttu-id="28eb9-128">Note</span><span class="sxs-lookup"><span data-stu-id="28eb9-128">NOTES</span></span>

## <span data-ttu-id="28eb9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28eb9-129">RELATED LINKS</span></span>

