---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859494"
---
# <span data-ttu-id="c3aa1-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="c3aa1-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="c3aa1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="c3aa1-103">Elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-103">List of supported operations.</span></span>

## <span data-ttu-id="c3aa1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3aa1-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="c3aa1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="c3aa1-106">Elenco delle operazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-106">List of supported operations.</span></span>

## <span data-ttu-id="c3aa1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3aa1-107">EXAMPLES</span></span>

### <span data-ttu-id="c3aa1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3aa1-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c3aa1-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="c3aa1-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c3aa1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3aa1-110">PARAMETERS</span></span>

### <span data-ttu-id="c3aa1-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3aa1-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="c3aa1-112">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="c3aa1-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c3aa1-113">-DisplayName</span></span>
<span data-ttu-id="c3aa1-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-114">Subscription name.</span></span>

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

### <span data-ttu-id="c3aa1-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c3aa1-115">-ExternalReferenceId</span></span>
<span data-ttu-id="c3aa1-116">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-116">External reference identifier.</span></span>

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

### <span data-ttu-id="c3aa1-117">-ID</span><span class="sxs-lookup"><span data-stu-id="c3aa1-117">-Id</span></span>
<span data-ttu-id="c3aa1-118">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-118">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="c3aa1-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3aa1-119">-Name</span></span>
<span data-ttu-id="c3aa1-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-120">Name of the resource.</span></span>

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

### <span data-ttu-id="c3aa1-121">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="c3aa1-121">-OfferId</span></span>
<span data-ttu-id="c3aa1-122">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-122">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="c3aa1-123">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="c3aa1-123">-Owner</span></span>
<span data-ttu-id="c3aa1-124">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-124">Subscription owner.</span></span>

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

### <span data-ttu-id="c3aa1-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="c3aa1-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="c3aa1-126">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-126">Routing resource manager type.</span></span>

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

### <span data-ttu-id="c3aa1-127">-Stato</span><span class="sxs-lookup"><span data-stu-id="c3aa1-127">-State</span></span>
<span data-ttu-id="c3aa1-128">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-128">Subscription state.</span></span>

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

### <span data-ttu-id="c3aa1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3aa1-129">-SubscriptionId</span></span>
<span data-ttu-id="c3aa1-130">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="c3aa1-131">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="c3aa1-131">-TenantId</span></span>
<span data-ttu-id="c3aa1-132">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="c3aa1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3aa1-133">CommonParameters</span></span>
<span data-ttu-id="c3aa1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3aa1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3aa1-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3aa1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3aa1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3aa1-136">INPUTS</span></span>

## <span data-ttu-id="c3aa1-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3aa1-137">OUTPUTS</span></span>

## <span data-ttu-id="c3aa1-138">Note</span><span class="sxs-lookup"><span data-stu-id="c3aa1-138">NOTES</span></span>

## <span data-ttu-id="c3aa1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3aa1-139">RELATED LINKS</span></span>

