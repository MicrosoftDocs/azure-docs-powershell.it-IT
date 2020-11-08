---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023283"
---
# <span data-ttu-id="7bdb5-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="7bdb5-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="7bdb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bdb5-102">SYNOPSIS</span></span>
<span data-ttu-id="7bdb5-103">Ottenere le metriche per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-103">Get the offer metrics.</span></span>

## <span data-ttu-id="7bdb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bdb5-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7bdb5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bdb5-105">DESCRIPTION</span></span>
<span data-ttu-id="7bdb5-106">Ottenere le metriche per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-106">Get the offer metrics.</span></span>

## <span data-ttu-id="7bdb5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bdb5-107">EXAMPLES</span></span>

### <span data-ttu-id="7bdb5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7bdb5-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="7bdb5-109">Ottenere le metriche per l'offerta.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-109">Get the offer metrics.</span></span>

## <span data-ttu-id="7bdb5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bdb5-110">PARAMETERS</span></span>

### <span data-ttu-id="7bdb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bdb5-111">-DefaultProfile</span></span>
<span data-ttu-id="7bdb5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bdb5-113">-Offername</span><span class="sxs-lookup"><span data-stu-id="7bdb5-113">-OfferName</span></span>
<span data-ttu-id="7bdb5-114">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-114">Name of an offer.</span></span>

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

### <span data-ttu-id="7bdb5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bdb5-115">-ResourceGroupName</span></span>
<span data-ttu-id="7bdb5-116">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7bdb5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bdb5-117">-SubscriptionId</span></span>
<span data-ttu-id="7bdb5-118">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7bdb5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bdb5-119">CommonParameters</span></span>
<span data-ttu-id="7bdb5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bdb5-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bdb5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bdb5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bdb5-122">INPUTS</span></span>

## <span data-ttu-id="7bdb5-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bdb5-123">OUTPUTS</span></span>

### <span data-ttu-id="7bdb5-124">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="7bdb5-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="7bdb5-125">ALIAS</span><span class="sxs-lookup"><span data-stu-id="7bdb5-125">ALIASES</span></span>

## <span data-ttu-id="7bdb5-126">Note</span><span class="sxs-lookup"><span data-stu-id="7bdb5-126">NOTES</span></span>

## <span data-ttu-id="7bdb5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bdb5-127">RELATED LINKS</span></span>

