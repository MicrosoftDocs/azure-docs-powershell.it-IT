---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858869"
---
# <span data-ttu-id="f0c0c-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="f0c0c-101">New-OfferObject</span></span>

## <span data-ttu-id="f0c0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c0c-103">Rappresenta un'offerta di servizi per cui è possibile creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="f0c0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0c0c-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="f0c0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0c0c-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c0c-106">Rappresenta un'offerta di servizi per cui è possibile creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="f0c0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0c0c-107">EXAMPLES</span></span>

### <span data-ttu-id="f0c0c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0c0c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f0c0c-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="f0c0c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f0c0c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0c0c-110">PARAMETERS</span></span>

### <span data-ttu-id="f0c0c-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="f0c0c-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="f0c0c-112">Riferimenti a piani per i componenti aggiuntivi che un tenant può acquistare facoltativamente come parte dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c0c-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="f0c0c-113">-BasePlanIds</span></span>
<span data-ttu-id="f0c0c-114">Identificatori dei piani di base che diventano disponibili per il tenant immediatamente quando un tenant sottoscrive l'offerta.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c0c-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0c0c-115">-Description</span></span>
<span data-ttu-id="f0c0c-116">Descrizione dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-116">Description of offer.</span></span>

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

### <span data-ttu-id="f0c0c-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f0c0c-117">-DisplayName</span></span>
<span data-ttu-id="f0c0c-118">Nome visualizzato dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-118">Display name of offer.</span></span>

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

### <span data-ttu-id="f0c0c-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f0c0c-119">-ExternalReferenceId</span></span>
<span data-ttu-id="f0c0c-120">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-120">External reference identifier.</span></span>

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

### <span data-ttu-id="f0c0c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f0c0c-121">-Id</span></span>
<span data-ttu-id="f0c0c-122">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-122">URI of the resource.</span></span>

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

### <span data-ttu-id="f0c0c-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f0c0c-123">-Location</span></span>
<span data-ttu-id="f0c0c-124">Posizione in cui la risorsa è posizione.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-124">Location where resource is location.</span></span>

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

### <span data-ttu-id="f0c0c-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="f0c0c-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="f0c0c-126">Numero massimo di abbonamenti per account.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c0c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0c0c-127">-Name</span></span>
<span data-ttu-id="f0c0c-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-128">Name of the resource.</span></span>

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

### <span data-ttu-id="f0c0c-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="f0c0c-129">-State</span></span>
<span data-ttu-id="f0c0c-130">Offrire lo stato di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="f0c0c-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="f0c0c-131">-SubscriptionCount</span></span>
<span data-ttu-id="f0c0c-132">Conteggio corrente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c0c-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0c0c-133">-Tags</span></span>
<span data-ttu-id="f0c0c-134">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c0c-135">-Digitare</span><span class="sxs-lookup"><span data-stu-id="f0c0c-135">-Type</span></span>
<span data-ttu-id="f0c0c-136">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-136">Type of resource.</span></span>

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

### <span data-ttu-id="f0c0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c0c-137">CommonParameters</span></span>
<span data-ttu-id="f0c0c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c0c-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c0c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c0c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0c0c-140">INPUTS</span></span>

## <span data-ttu-id="f0c0c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0c0c-141">OUTPUTS</span></span>

## <span data-ttu-id="f0c0c-142">Note</span><span class="sxs-lookup"><span data-stu-id="f0c0c-142">NOTES</span></span>

## <span data-ttu-id="f0c0c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0c0c-143">RELATED LINKS</span></span>

