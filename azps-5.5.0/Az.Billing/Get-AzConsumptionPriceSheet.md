---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: 999466a754fdeeb98a3d8aaefd91f0b65a2810f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205162"
---
# <span data-ttu-id="a1a92-101">Get-AzConsumptionPriceSheet</span><span class="sxs-lookup"><span data-stu-id="a1a92-101">Get-AzConsumptionPriceSheet</span></span>

## <span data-ttu-id="a1a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1a92-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a92-103">Ottieni i listini prezzi dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1a92-103">Get price sheets of the subscription.</span></span>

## <span data-ttu-id="a1a92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1a92-104">SYNTAX</span></span>

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a92-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1a92-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a92-106">Il **cmdlet Get-AzConsumptionPriceSheet** ottiene i listini prezzi dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1a92-106">The **Get-AzConsumptionPriceSheet** cmdlet gets price sheets of the subscription.</span></span>

## <span data-ttu-id="a1a92-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1a92-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a92-108">Esempio 1: Ottenere fogli prezzi</span><span class="sxs-lookup"><span data-stu-id="a1a92-108">Example 1: Get price sheets</span></span>
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

### <span data-ttu-id="a1a92-109">Esempio 2: Ottenere fogli prezzi con l'espansione di MeterDetails</span><span class="sxs-lookup"><span data-stu-id="a1a92-109">Example 2: Get price sheets with expand of MeterDetails</span></span>
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

### <span data-ttu-id="a1a92-110">Esempio 3: Ottenere fogli prezzi di BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="a1a92-110">Example 3: Get price sheets of BillingPeriodName</span></span>
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

### <span data-ttu-id="a1a92-111">Esempio 4: Ottenere i primi 5 record di listini prezzi</span><span class="sxs-lookup"><span data-stu-id="a1a92-111">Example 4: Get top 5 records of price sheets</span></span>
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

## <span data-ttu-id="a1a92-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1a92-112">PARAMETERS</span></span>

### <span data-ttu-id="a1a92-113">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="a1a92-113">-BillingPeriodName</span></span>
<span data-ttu-id="a1a92-114">Nome di un periodo di fatturazione specifico a cui ottenere gli fogli prezzi associati.</span><span class="sxs-lookup"><span data-stu-id="a1a92-114">Name of a specific billing period to get the price sheets that associate with.</span></span>

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

### <span data-ttu-id="a1a92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a92-115">-DefaultProfile</span></span>
<span data-ttu-id="a1a92-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1a92-117">-ExpandMeterDetail</span><span class="sxs-lookup"><span data-stu-id="a1a92-117">-ExpandMeterDetail</span></span>
<span data-ttu-id="a1a92-118">Espandere i listini prezzi in base a MeterDetails.</span><span class="sxs-lookup"><span data-stu-id="a1a92-118">Expand the price sheets based on MeterDetails.</span></span>

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

### <span data-ttu-id="a1a92-119">-In alto</span><span class="sxs-lookup"><span data-stu-id="a1a92-119">-Top</span></span>
<span data-ttu-id="a1a92-120">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="a1a92-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="a1a92-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a92-121">CommonParameters</span></span>
<span data-ttu-id="a1a92-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a92-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a92-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a92-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a92-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1a92-124">INPUTS</span></span>

### <span data-ttu-id="a1a92-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a1a92-125">None</span></span>

## <span data-ttu-id="a1a92-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1a92-126">OUTPUTS</span></span>

### <span data-ttu-id="a1a92-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span><span class="sxs-lookup"><span data-stu-id="a1a92-127">Microsoft.Azure.Commands.Consumption.Models.PSPriceSheet</span></span>

## <span data-ttu-id="a1a92-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1a92-128">NOTES</span></span>

## <span data-ttu-id="a1a92-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1a92-129">RELATED LINKS</span></span>
