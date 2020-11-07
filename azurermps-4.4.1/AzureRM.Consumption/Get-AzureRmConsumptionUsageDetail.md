---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionUsageDetail.md
ms.openlocfilehash: f8347fca355080f11e69bae9793cc0367325ce98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688351"
---
# <span data-ttu-id="4fc79-101">Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="4fc79-101">Get-AzureRmConsumptionUsageDetail</span></span>

## <span data-ttu-id="4fc79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fc79-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc79-103">Ottenere i dettagli sull'utilizzo dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4fc79-103">Get usage details of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fc79-104">SYNTAX</span></span>

### <span data-ttu-id="4fc79-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4fc79-105">Subscription (Default)</span></span>
```
Get-AzureRmConsumptionUsageDetail [-MaxCount <Int32>] [-IncludeMeterDetails] [-IncludeAdditionalProperties]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc79-106">Fattura</span><span class="sxs-lookup"><span data-stu-id="4fc79-106">Invoice</span></span>
```
Get-AzureRmConsumptionUsageDetail -InvoiceName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc79-107">BillingPeriod</span><span class="sxs-lookup"><span data-stu-id="4fc79-107">BillingPeriod</span></span>
```
Get-AzureRmConsumptionUsageDetail -BillingPeriodName <String> [-MaxCount <Int32>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc79-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fc79-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc79-109">Il cmdlet **Get-AzureRmConsumptionUsageDetail** ottiene i dettagli sull'utilizzo dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4fc79-109">The **Get-AzureRmConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="4fc79-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fc79-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc79-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4fc79-111">Example 1</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeMeterDetails -InvoiceName 201704-117283130069214
```

<span data-ttu-id="4fc79-112">Ottenere i dettagli sull'utilizzo della fattura con il nome specificato e includere la proprietà MeterDetails nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4fc79-112">Get usage details of the invoice with specified name, and include MeterDetails property in the result.</span></span>

### <span data-ttu-id="4fc79-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4fc79-113">Example 2</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -IncludeAdditionalProperties -BillingPeriodName 201704-1
```

<span data-ttu-id="4fc79-114">Ottenere i dettagli sull'utilizzo del periodo di fatturazione con il nome specificato e includere la proprietà AdditionalProperties nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4fc79-114">Get usage details of the billing period with specified name, and include AdditionalProperties property in the result.</span></span>

### <span data-ttu-id="4fc79-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4fc79-115">Example 3</span></span>
```
PS C:\> Get-AzureRmConsumptionUsageDetail -StartDate 2017-01-17 -EndDate 2017-01-19
```

<span data-ttu-id="4fc79-116">Ottenere i dettagli sull'utilizzo dell'abbonamento compreso tra 2017-01-17 e 2017-01-19.</span><span class="sxs-lookup"><span data-stu-id="4fc79-116">Get usage details of the subscription that is between 2017-01-17 to 2017-01-19.</span></span>

## <span data-ttu-id="4fc79-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fc79-117">PARAMETERS</span></span>

### <span data-ttu-id="4fc79-118">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="4fc79-118">-BillingPeriodName</span></span>
<span data-ttu-id="4fc79-119">Nome di un periodo di fatturazione specifico per ottenere i dettagli sull'utilizzo associati.</span><span class="sxs-lookup"><span data-stu-id="4fc79-119">Name of a specific billing period to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: BillingPeriod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc79-120">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4fc79-120">-EndDate</span></span>
<span data-ttu-id="4fc79-121">Data di fine (in formato UTC) degli usi.</span><span class="sxs-lookup"><span data-stu-id="4fc79-121">The end date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc79-122">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="4fc79-122">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="4fc79-123">Includi proprietà aggiuntive negli usi.</span><span class="sxs-lookup"><span data-stu-id="4fc79-123">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="4fc79-124">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="4fc79-124">-IncludeMeterDetails</span></span>
<span data-ttu-id="4fc79-125">Includere i dettagli dei contatori negli usi.</span><span class="sxs-lookup"><span data-stu-id="4fc79-125">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="4fc79-126">-Invoicename</span><span class="sxs-lookup"><span data-stu-id="4fc79-126">-InvoiceName</span></span>
<span data-ttu-id="4fc79-127">Nome di una fattura specifica per ottenere i dettagli sull'utilizzo associati.</span><span class="sxs-lookup"><span data-stu-id="4fc79-127">Name of a specific invoice to get the usage details that associate with.</span></span>

```yaml
Type: System.String
Parameter Sets: Invoice
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc79-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4fc79-128">-MaxCount</span></span>
<span data-ttu-id="4fc79-129">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="4fc79-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="4fc79-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4fc79-130">-StartDate</span></span>
<span data-ttu-id="4fc79-131">Data di inizio (in formato UTC) degli usi.</span><span class="sxs-lookup"><span data-stu-id="4fc79-131">The start date (in UTC) of the usages.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc79-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc79-132">-DefaultProfile</span></span>
<span data-ttu-id="4fc79-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc79-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc79-134">CommonParameters</span></span>
<span data-ttu-id="4fc79-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc79-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc79-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc79-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fc79-137">INPUTS</span></span>

### <span data-ttu-id="4fc79-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4fc79-138">None</span></span>

## <span data-ttu-id="4fc79-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fc79-139">OUTPUTS</span></span>

### <span data-ttu-id="4fc79-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. consume. Models. PSUsageDetail, Microsoft. Azure. Commands. consumer, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4fc79-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail, Microsoft.Azure.Commands.Consumption, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4fc79-141">Note</span><span class="sxs-lookup"><span data-stu-id="4fc79-141">NOTES</span></span>

## <span data-ttu-id="4fc79-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fc79-142">RELATED LINKS</span></span>

