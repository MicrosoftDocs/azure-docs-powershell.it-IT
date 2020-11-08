---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030626"
---
# <span data-ttu-id="8c042-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="8c042-101">New-PlanObject</span></span>

## <span data-ttu-id="8c042-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c042-102">SYNOPSIS</span></span>
<span data-ttu-id="8c042-103">Un piano rappresenta un pacchetto di quote e funzionalità offerte dai tenant.</span><span class="sxs-lookup"><span data-stu-id="8c042-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="8c042-104">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="8c042-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="8c042-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c042-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="8c042-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c042-106">DESCRIPTION</span></span>
<span data-ttu-id="8c042-107">Un piano rappresenta un pacchetto di quote e funzionalità offerte dai tenant.</span><span class="sxs-lookup"><span data-stu-id="8c042-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="8c042-108">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="8c042-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="8c042-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c042-109">EXAMPLES</span></span>

### <span data-ttu-id="8c042-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8c042-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8c042-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="8c042-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="8c042-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c042-112">PARAMETERS</span></span>

### <span data-ttu-id="8c042-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c042-113">-Description</span></span>
<span data-ttu-id="8c042-114">Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="8c042-114">Description of the plan.</span></span>

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

### <span data-ttu-id="8c042-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8c042-115">-DisplayName</span></span>
<span data-ttu-id="8c042-116">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="8c042-116">Display name.</span></span>

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

### <span data-ttu-id="8c042-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8c042-117">-ExternalReferenceId</span></span>
<span data-ttu-id="8c042-118">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="8c042-118">External reference identifier.</span></span>

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

### <span data-ttu-id="8c042-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8c042-119">-Id</span></span>
<span data-ttu-id="8c042-120">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8c042-120">URI of the resource.</span></span>

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

### <span data-ttu-id="8c042-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8c042-121">-Location</span></span>
<span data-ttu-id="8c042-122">Posizione in cui la risorsa è posizione.</span><span class="sxs-lookup"><span data-stu-id="8c042-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="8c042-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c042-123">-Name</span></span>
<span data-ttu-id="8c042-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8c042-124">Name of the resource.</span></span>

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

### <span data-ttu-id="8c042-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="8c042-125">-QuotaIds</span></span>
<span data-ttu-id="8c042-126">Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="8c042-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c042-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="8c042-127">-SkuIds</span></span>
<span data-ttu-id="8c042-128">Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="8c042-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c042-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="8c042-129">-SubscriptionCount</span></span>
<span data-ttu-id="8c042-130">Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="8c042-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c042-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c042-131">-Tags</span></span>
<span data-ttu-id="8c042-132">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="8c042-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c042-133">-Digitare</span><span class="sxs-lookup"><span data-stu-id="8c042-133">-Type</span></span>
<span data-ttu-id="8c042-134">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="8c042-134">Type of resource.</span></span>

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

### <span data-ttu-id="8c042-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c042-135">CommonParameters</span></span>
<span data-ttu-id="8c042-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c042-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c042-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c042-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c042-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c042-138">INPUTS</span></span>

## <span data-ttu-id="8c042-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c042-139">OUTPUTS</span></span>

## <span data-ttu-id="8c042-140">Note</span><span class="sxs-lookup"><span data-stu-id="8c042-140">NOTES</span></span>

## <span data-ttu-id="8c042-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c042-141">RELATED LINKS</span></span>

