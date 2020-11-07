---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859210"
---
# <span data-ttu-id="fc234-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="fc234-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="fc234-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc234-102">SYNOPSIS</span></span>
<span data-ttu-id="fc234-103">Elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="fc234-103">List of supported operations.</span></span>

## <span data-ttu-id="fc234-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc234-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="fc234-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc234-105">DESCRIPTION</span></span>
<span data-ttu-id="fc234-106">Elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="fc234-106">List of supported operations.</span></span>

## <span data-ttu-id="fc234-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc234-107">EXAMPLES</span></span>

### <span data-ttu-id="fc234-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc234-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fc234-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="fc234-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="fc234-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc234-110">PARAMETERS</span></span>

### <span data-ttu-id="fc234-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc234-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="fc234-112">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="fc234-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="fc234-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fc234-113">-DisplayName</span></span>
<span data-ttu-id="fc234-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fc234-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc234-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="fc234-115">-ExternalReferenceId</span></span>
<span data-ttu-id="fc234-116">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="fc234-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc234-117">-ID</span><span class="sxs-lookup"><span data-stu-id="fc234-117">-Id</span></span>
<span data-ttu-id="fc234-118">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="fc234-118">Fully qualified identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc234-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc234-119">-Name</span></span>
<span data-ttu-id="fc234-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc234-120">Name of the resource.</span></span>

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

### <span data-ttu-id="fc234-121">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="fc234-121">-OfferId</span></span>
<span data-ttu-id="fc234-122">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="fc234-122">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc234-123">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="fc234-123">-Owner</span></span>
<span data-ttu-id="fc234-124">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fc234-124">Subscription owner.</span></span>

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

### <span data-ttu-id="fc234-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="fc234-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="fc234-126">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="fc234-126">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc234-127">-Stato</span><span class="sxs-lookup"><span data-stu-id="fc234-127">-State</span></span>
<span data-ttu-id="fc234-128">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fc234-128">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc234-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc234-129">-SubscriptionId</span></span>
<span data-ttu-id="fc234-130">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fc234-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="fc234-131">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="fc234-131">-TenantId</span></span>
<span data-ttu-id="fc234-132">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="fc234-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="fc234-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc234-133">CommonParameters</span></span>
<span data-ttu-id="fc234-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc234-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc234-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc234-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc234-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc234-136">INPUTS</span></span>

## <span data-ttu-id="fc234-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc234-137">OUTPUTS</span></span>

## <span data-ttu-id="fc234-138">Note</span><span class="sxs-lookup"><span data-stu-id="fc234-138">NOTES</span></span>

## <span data-ttu-id="fc234-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc234-139">RELATED LINKS</span></span>

