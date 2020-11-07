---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859517"
---
# <span data-ttu-id="dd0fb-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="dd0fb-101">New-PlanObject</span></span>

## <span data-ttu-id="dd0fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd0fb-102">SYNOPSIS</span></span>
<span data-ttu-id="dd0fb-103">Un piano rappresenta un pacchetto di quote e funzionalità offerte dai tenant.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="dd0fb-104">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="dd0fb-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd0fb-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="dd0fb-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd0fb-106">DESCRIPTION</span></span>
<span data-ttu-id="dd0fb-107">Un piano rappresenta un pacchetto di quote e funzionalità offerte dai tenant.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="dd0fb-108">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="dd0fb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd0fb-109">EXAMPLES</span></span>

### <span data-ttu-id="dd0fb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dd0fb-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="dd0fb-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="dd0fb-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="dd0fb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd0fb-112">PARAMETERS</span></span>

### <span data-ttu-id="dd0fb-113">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd0fb-113">-Description</span></span>
<span data-ttu-id="dd0fb-114">Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-114">Description of the plan.</span></span>

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

### <span data-ttu-id="dd0fb-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd0fb-115">-DisplayName</span></span>
<span data-ttu-id="dd0fb-116">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-116">Display name.</span></span>

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

### <span data-ttu-id="dd0fb-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="dd0fb-117">-ExternalReferenceId</span></span>
<span data-ttu-id="dd0fb-118">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-118">External reference identifier.</span></span>

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

### <span data-ttu-id="dd0fb-119">-ID</span><span class="sxs-lookup"><span data-stu-id="dd0fb-119">-Id</span></span>
<span data-ttu-id="dd0fb-120">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-120">URI of the resource.</span></span>

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

### <span data-ttu-id="dd0fb-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dd0fb-121">-Location</span></span>
<span data-ttu-id="dd0fb-122">Posizione in cui la risorsa è posizione.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="dd0fb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd0fb-123">-Name</span></span>
<span data-ttu-id="dd0fb-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-124">Name of the resource.</span></span>

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

### <span data-ttu-id="dd0fb-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="dd0fb-125">-QuotaIds</span></span>
<span data-ttu-id="dd0fb-126">Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-126">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="dd0fb-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="dd0fb-127">-SkuIds</span></span>
<span data-ttu-id="dd0fb-128">Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-128">SKU identifiers.</span></span>

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

### <span data-ttu-id="dd0fb-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="dd0fb-129">-SubscriptionCount</span></span>
<span data-ttu-id="dd0fb-130">Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-130">Subscription count.</span></span>

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

### <span data-ttu-id="dd0fb-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="dd0fb-131">-Tags</span></span>
<span data-ttu-id="dd0fb-132">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-132">List of key-value pairs.</span></span>

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

### <span data-ttu-id="dd0fb-133">-Digitare</span><span class="sxs-lookup"><span data-stu-id="dd0fb-133">-Type</span></span>
<span data-ttu-id="dd0fb-134">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-134">Type of resource.</span></span>

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

### <span data-ttu-id="dd0fb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd0fb-135">CommonParameters</span></span>
<span data-ttu-id="dd0fb-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd0fb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd0fb-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd0fb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd0fb-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd0fb-138">INPUTS</span></span>

## <span data-ttu-id="dd0fb-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd0fb-139">OUTPUTS</span></span>

## <span data-ttu-id="dd0fb-140">Note</span><span class="sxs-lookup"><span data-stu-id="dd0fb-140">NOTES</span></span>

## <span data-ttu-id="dd0fb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd0fb-141">RELATED LINKS</span></span>

