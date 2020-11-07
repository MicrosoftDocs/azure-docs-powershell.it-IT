---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: e52c096d1c5cf2c012952a89a922b7d3719c3f20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684906"
---
# <span data-ttu-id="523c6-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="523c6-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="523c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="523c6-102">SYNOPSIS</span></span>
<span data-ttu-id="523c6-103">Ottenere i fogli di prezzo dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="523c6-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="523c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="523c6-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="523c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="523c6-105">DESCRIPTION</span></span>
<span data-ttu-id="523c6-106">Il cmdlet **Get-AzConsumptionPriceSheet** ottiene i fogli di prezzo dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="523c6-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="523c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="523c6-107">EXAMPLES</span></span>

### <span data-ttu-id="523c6-108">Esempio 1: ottenere i fogli di prezzo</span><span class="sxs-lookup"><span data-stu-id="523c6-108">Example 1: Get price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="523c6-109">Esempio 2: ottenere i fogli di prezzo con l'espansione di MeterDetails</span><span class="sxs-lookup"><span data-stu-id="523c6-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### <span data-ttu-id="523c6-110">Esempio 3: ottenere fogli di prezzo di BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="523c6-110">Example 3: Get price sheets of BillingPeriodName</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### <span data-ttu-id="523c6-111">Esempio 4: ottenere i primi 5 record dei fogli di prezzo</span><span class="sxs-lookup"><span data-stu-id="523c6-111">Example 4: Get top 5 records of price sheets</span></span>
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## <span data-ttu-id="523c6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="523c6-112">PARAMETERS</span></span>

### <span data-ttu-id="523c6-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="523c6-113">-BillingPeriodName</span></span>
<span data-ttu-id="523c6-114">Nome di un periodo di fatturazione specifico per ottenere i fogli di prezzo con cui si associa.</span><span class="sxs-lookup"><span data-stu-id="523c6-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="523c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523c6-115">-DefaultProfile</span></span>
<span data-ttu-id="523c6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="523c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523c6-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="523c6-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="523c6-118">Espandere i fogli di prezzo in base a MeterDetails.</span><span class="sxs-lookup"><span data-stu-id="523c6-118">Expand the price sheets based on MeterDetails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523c6-119">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="523c6-119">-Top</span></span>
<span data-ttu-id="523c6-120">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="523c6-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523c6-121">CommonParameters</span></span>
<span data-ttu-id="523c6-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523c6-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523c6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523c6-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="523c6-124">INPUTS</span></span>

### <span data-ttu-id="523c6-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="523c6-125">None</span></span>

## <span data-ttu-id="523c6-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="523c6-126">OUTPUTS</span></span>

### <span data-ttu-id="523c6-127">Microsoft. Azure. Commands. consume. Models. PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="523c6-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="523c6-128">Note</span><span class="sxs-lookup"><span data-stu-id="523c6-128">NOTES</span></span>

## <span data-ttu-id="523c6-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="523c6-129">RELATED LINKS</span></span>
