---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplanmetric
schema: 2.0.0
ms.openlocfilehash: 9a8ef074cf6e59d30217b55b956a4d5101708bcc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023159"
---
# <span data-ttu-id="365a4-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="365a4-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="365a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="365a4-102">SYNOPSIS</span></span>
<span data-ttu-id="365a4-103">Ottenere le metriche del piano specificato.</span><span class="sxs-lookup"><span data-stu-id="365a4-103">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="365a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="365a4-104">SYNTAX</span></span>

```
Get-AzsPlanMetric -PlanName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="365a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="365a4-105">DESCRIPTION</span></span>
<span data-ttu-id="365a4-106">Ottenere le metriche del piano specificato.</span><span class="sxs-lookup"><span data-stu-id="365a4-106">Get the metrics of the specified plan.</span></span>

## <span data-ttu-id="365a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="365a4-107">EXAMPLES</span></span>

### <span data-ttu-id="365a4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="365a4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlanMetric -PlanName "testplan" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:06:16 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="365a4-109">Ottenere le metriche di un piano.</span><span class="sxs-lookup"><span data-stu-id="365a4-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="365a4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="365a4-110">PARAMETERS</span></span>

### <span data-ttu-id="365a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365a4-111">-DefaultProfile</span></span>
<span data-ttu-id="365a4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="365a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="365a4-113">-PlanName</span><span class="sxs-lookup"><span data-stu-id="365a4-113">-PlanName</span></span>
<span data-ttu-id="365a4-114">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="365a4-114">Name of the plan.</span></span>

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

### <span data-ttu-id="365a4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365a4-115">-ResourceGroupName</span></span>
<span data-ttu-id="365a4-116">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="365a4-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="365a4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="365a4-117">-SubscriptionId</span></span>
<span data-ttu-id="365a4-118">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="365a4-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="365a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365a4-119">CommonParameters</span></span>
<span data-ttu-id="365a4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365a4-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="365a4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365a4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="365a4-122">INPUTS</span></span>

## <span data-ttu-id="365a4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="365a4-123">OUTPUTS</span></span>

### <span data-ttu-id="365a4-124">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IMetricList</span><span class="sxs-lookup"><span data-stu-id="365a4-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="365a4-125">ALIAS</span><span class="sxs-lookup"><span data-stu-id="365a4-125">ALIASES</span></span>

## <span data-ttu-id="365a4-126">Note</span><span class="sxs-lookup"><span data-stu-id="365a4-126">NOTES</span></span>

## <span data-ttu-id="365a4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="365a4-127">RELATED LINKS</span></span>

