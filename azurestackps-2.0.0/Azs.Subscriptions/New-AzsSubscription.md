---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860117"
---
# <span data-ttu-id="ba712-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="ba712-101">New-AzsSubscription</span></span>

## <span data-ttu-id="ba712-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba712-102">SYNOPSIS</span></span>
<span data-ttu-id="ba712-103">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ba712-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="ba712-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba712-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ba712-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba712-105">DESCRIPTION</span></span>
<span data-ttu-id="ba712-106">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ba712-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="ba712-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba712-107">EXAMPLES</span></span>

### <span data-ttu-id="ba712-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba712-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="ba712-109">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ba712-109">Create a subscription.</span></span>

## <span data-ttu-id="ba712-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba712-110">PARAMETERS</span></span>

### <span data-ttu-id="ba712-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba712-111">-DefaultProfile</span></span>
<span data-ttu-id="ba712-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba712-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ba712-113">-DisplayName</span></span>
<span data-ttu-id="ba712-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ba712-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-115">-ID</span><span class="sxs-lookup"><span data-stu-id="ba712-115">-Id</span></span>
<span data-ttu-id="ba712-116">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="ba712-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-117">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="ba712-117">-OfferId</span></span>
<span data-ttu-id="ba712-118">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="ba712-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="ba712-119">-State</span></span>
<span data-ttu-id="ba712-120">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ba712-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba712-121">-SubscriptionId</span></span>
<span data-ttu-id="ba712-122">ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ba712-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-123">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="ba712-123">-TenantId</span></span>
<span data-ttu-id="ba712-124">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="ba712-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba712-125">-Confirm</span></span>
<span data-ttu-id="ba712-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba712-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba712-127">-WhatIf</span></span>
<span data-ttu-id="ba712-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba712-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba712-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba712-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba712-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba712-130">CommonParameters</span></span>
<span data-ttu-id="ba712-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba712-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba712-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba712-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba712-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba712-133">INPUTS</span></span>

## <span data-ttu-id="ba712-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba712-134">OUTPUTS</span></span>

### <span data-ttu-id="ba712-135">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="ba712-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="ba712-136">Note</span><span class="sxs-lookup"><span data-stu-id="ba712-136">NOTES</span></span>

## <span data-ttu-id="ba712-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba712-137">RELATED LINKS</span></span>

