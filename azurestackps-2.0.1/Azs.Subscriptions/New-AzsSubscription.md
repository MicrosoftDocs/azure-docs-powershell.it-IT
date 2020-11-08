---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023133"
---
# <span data-ttu-id="7b085-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="7b085-101">New-AzsSubscription</span></span>

## <span data-ttu-id="7b085-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b085-102">SYNOPSIS</span></span>
<span data-ttu-id="7b085-103">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b085-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="7b085-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b085-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7b085-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b085-105">DESCRIPTION</span></span>
<span data-ttu-id="7b085-106">Creare o aggiornare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b085-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="7b085-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b085-107">EXAMPLES</span></span>

### <span data-ttu-id="7b085-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7b085-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="7b085-109">Creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b085-109">Create a subscription.</span></span>

## <span data-ttu-id="7b085-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b085-110">PARAMETERS</span></span>

### <span data-ttu-id="7b085-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b085-111">-DefaultProfile</span></span>
<span data-ttu-id="7b085-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b085-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b085-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7b085-113">-DisplayName</span></span>
<span data-ttu-id="7b085-114">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b085-114">Subscription name.</span></span>

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

### <span data-ttu-id="7b085-115">-ID</span><span class="sxs-lookup"><span data-stu-id="7b085-115">-Id</span></span>
<span data-ttu-id="7b085-116">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="7b085-116">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="7b085-117">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="7b085-117">-OfferId</span></span>
<span data-ttu-id="7b085-118">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="7b085-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="7b085-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="7b085-119">-State</span></span>
<span data-ttu-id="7b085-120">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7b085-120">Subscription state.</span></span>

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

### <span data-ttu-id="7b085-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b085-121">-SubscriptionId</span></span>
<span data-ttu-id="7b085-122">ID dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7b085-122">Id of the subscription.</span></span>

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

### <span data-ttu-id="7b085-123">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="7b085-123">-TenantId</span></span>
<span data-ttu-id="7b085-124">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="7b085-124">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="7b085-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b085-125">-Confirm</span></span>
<span data-ttu-id="7b085-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b085-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b085-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b085-127">-WhatIf</span></span>
<span data-ttu-id="7b085-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b085-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b085-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b085-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b085-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b085-130">CommonParameters</span></span>
<span data-ttu-id="7b085-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b085-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b085-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b085-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b085-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b085-133">INPUTS</span></span>

## <span data-ttu-id="7b085-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b085-134">OUTPUTS</span></span>

### <span data-ttu-id="7b085-135">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="7b085-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="7b085-136">Note</span><span class="sxs-lookup"><span data-stu-id="7b085-136">NOTES</span></span>

## <span data-ttu-id="7b085-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b085-137">RELATED LINKS</span></span>

