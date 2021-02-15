---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionusagedetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionUsageDetail.md
ms.openlocfilehash: 8eeee753fda32f40dfabf156b352724b0bd87b92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182014"
---
# <span data-ttu-id="e857a-101">Get-AzConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="e857a-101">Get-AzConsumptionUsageDetail</span></span>

## <span data-ttu-id="e857a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e857a-102">SYNOPSIS</span></span>
<span data-ttu-id="e857a-103">Ottenere i dettagli di utilizzo dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e857a-103">Get usage details of the subscription.</span></span>

## <span data-ttu-id="e857a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e857a-104">SYNTAX</span></span>

```
Get-AzConsumptionUsageDetail [-BillingPeriodName <String>] [-Expand <String>] [-IncludeMeterDetails]
 [-IncludeAdditionalProperties] [-StartDate <DateTime>] [-EndDate <DateTime>] [-ResourceGroup <String>]
 [-InstanceName <String>] [-InstanceId <String>] [-Tag <String>] [-MaxCount <Int32>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e857a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e857a-105">DESCRIPTION</span></span>
<span data-ttu-id="e857a-106">Il cmdlet **Get-AzConsumptionUsageDetail** ottiene i dettagli di utilizzo dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e857a-106">The **Get-AzConsumptionUsageDetail** cmdlet gets usage details of the subscription.</span></span> 

## <span data-ttu-id="e857a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e857a-107">EXAMPLES</span></span>

### <span data-ttu-id="e857a-108">Esempio 1: Ottenere i dettagli di utilizzo con l'espansione di MeterDetails</span><span class="sxs-lookup"><span data-stu-id="e857a-108">Example 1: Get usage details with expand of MeterDetails</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -Expand MeterDetails -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
ConsumedService:  Microsoft.Compute
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/usageDetails/24b9dff0-f022-55a1-886b-17b330000db3
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/MAR-CCM/providers/Microsoft.Compute/disks/mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
InstanceLocation:  usnorthcentral
InstanceName:  mar-ccm-vm01_OsDisk_1_d0beead4b6ff4b4088a687701d355d61
IsEstimated:  true
MeterDetails:  MeterCategory:  Data Management
               MeterLocation:  usnorthcentral
               MeterName:  Standard Managed Disk Operations (in 10,000s)
               MeterSubCategory:  Data Management
               Unit:  Operations
MeterId:  82cd70ab-1aee-4b30-bc04-8b71e1204dbc
Name:  24b9dff0-f022-55a1-886b-17b330000db3
PretaxCost:  0
Product:  Data Management Standard Managed Disk Operations
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  6/1/2018 11:59:59 PM
UsageQuantity:  3.8218
UsageStart:  6/1/2018 12:00:00 AM
```

### <span data-ttu-id="e857a-109">Esempio 2: Ottenere i dettagli sull'utilizzo con l'intervallo di date</span><span class="sxs-lookup"><span data-stu-id="e857a-109">Example 2: Get usage details with date range</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -StartDate 2017-10-02 -EndDate 2017-10-05 -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/732582e5-40ad-bb23-7a69-ca1ff7c8b004
InstanceId:  storsimplezc9q6r2t7f
InstanceLocation:  US West Central
InstanceName:  storsimplezc9q6r2t7f
IsEstimated:  false
MeterId:  ad22fac8-9da5-4577-8683-56ae94d39e42
Name:  732582e5-40ad-bb23-7a69-ca1ff7c8b004
PretaxCost:  0
Product:  Data Management Geo Redundant Standard IO - Table Write
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/2/2017 11:59:59 PM
UsageQuantity:  0.0006
UsageStart:  10/2/2017 12:00:00 AM
```

### <span data-ttu-id="e857a-110">Esempio 3: Ottenere i dettagli di utilizzo di BillingPeriodName con il filtro InstanceName</span><span class="sxs-lookup"><span data-stu-id="e857a-110">Example 3: Get usage details of BillingPeriodName with InstanceName filter</span></span>
```powershell
PS C:\> Get-AzConsumptionUsageDetail -BillingPeriodName 201710 -InstanceName 1c2052westus -Top 10
AccountName:  AAAA
BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001
ConsumedService:  Microsoft.Storage
CostCenter:  XYZ987
Currency:  USD
DepartmentName:  Ama
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20171001/providers/Microsoft.Consumption/usageDetails/8abc8b65-e8f1-31e1-f02b-058a7572363f
InstanceId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/securitydata/providers/Microsoft.Storage/storageAccounts/1c2052westus
InstanceLocation:  uswest
InstanceName:  1c2052westus
IsEstimated:  false
MeterId:  9995d93a-7d35-4d3f-9c69-7a7fea447ef4
Name:  8abc8b65-e8f1-31e1-f02b-058a7572363f
PretaxCost:  0.000000693016692
Product:  Data Transfer Out - Zone 1
SubscriptionGuid:  1caaa5a3-2b66-438e-8ab4-bce37d518c5d
SubscriptionName:  CCM - Microsoft Azure Enterprise - 1
Type:  Microsoft.Consumption/usageDetails
UsageEnd:  10/1/2017 11:59:59 PM
UsageQuantity:  0.000009
UsageStart:  10/1/2017 12:00:00 AM
```

## <span data-ttu-id="e857a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e857a-111">PARAMETERS</span></span>

### <span data-ttu-id="e857a-112">-BillingPeriodName</span><span class="sxs-lookup"><span data-stu-id="e857a-112">-BillingPeriodName</span></span>
<span data-ttu-id="e857a-113">Nome di un periodo di fatturazione specifico a cui ottenere i dettagli di utilizzo associati.</span><span class="sxs-lookup"><span data-stu-id="e857a-113">Name of a specific billing period to get the usage details that associate with.</span></span>

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

### <span data-ttu-id="e857a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e857a-114">-DefaultProfile</span></span>
<span data-ttu-id="e857a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e857a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e857a-116">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e857a-116">-EndDate</span></span>
<span data-ttu-id="e857a-117">Data di fine (in UTC) degli utilizzi da filtrare.</span><span class="sxs-lookup"><span data-stu-id="e857a-117">The end date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="e857a-118">-Expand</span><span class="sxs-lookup"><span data-stu-id="e857a-118">-Expand</span></span>
<span data-ttu-id="e857a-119">Espandere gli utilizzi in base a MeterDetails o AdditionalInfo.</span><span class="sxs-lookup"><span data-stu-id="e857a-119">Expand the usages based on MeterDetails, or AdditionalInfo.</span></span>

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

### <span data-ttu-id="e857a-120">-IncludeAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="e857a-120">-IncludeAdditionalProperties</span></span>
<span data-ttu-id="e857a-121">Includere proprietà aggiuntive nelle modalità di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e857a-121">Include additional properties in the usages.</span></span>

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

### <span data-ttu-id="e857a-122">-IncludeMeterDetails</span><span class="sxs-lookup"><span data-stu-id="e857a-122">-IncludeMeterDetails</span></span>
<span data-ttu-id="e857a-123">Includere i dettagli del contatore nelle modalità di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e857a-123">Include meter details in the usages.</span></span>

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

### <span data-ttu-id="e857a-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e857a-124">-InstanceId</span></span>
<span data-ttu-id="e857a-125">ID istanza degli utilizzi da filtrare.</span><span class="sxs-lookup"><span data-stu-id="e857a-125">The instance id of the usages to filter.</span></span>

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

### <span data-ttu-id="e857a-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e857a-126">-InstanceName</span></span>
<span data-ttu-id="e857a-127">Nome dell'istanza degli utilizzi da filtrare.</span><span class="sxs-lookup"><span data-stu-id="e857a-127">The instance name of the usages to filter.</span></span>

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

### <span data-ttu-id="e857a-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e857a-128">-MaxCount</span></span>
<span data-ttu-id="e857a-129">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="e857a-129">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="e857a-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e857a-130">-ResourceGroup</span></span>
<span data-ttu-id="e857a-131">Gruppo di risorse degli utilizzi da filtrare.</span><span class="sxs-lookup"><span data-stu-id="e857a-131">The resource group of the usages to filter.</span></span>

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

### <span data-ttu-id="e857a-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e857a-132">-StartDate</span></span>
<span data-ttu-id="e857a-133">Data di inizio (in UTC) degli utilizzi da filtrare.</span><span class="sxs-lookup"><span data-stu-id="e857a-133">The start date (in UTC) of the usages to filter.</span></span>

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

### <span data-ttu-id="e857a-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="e857a-134">-Tag</span></span>
<span data-ttu-id="e857a-135">Tag degli utilizzi da filtrare.</span><span class="sxs-lookup"><span data-stu-id="e857a-135">The tag of the usages to filter.</span></span>

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

### <span data-ttu-id="e857a-136">-In alto</span><span class="sxs-lookup"><span data-stu-id="e857a-136">-Top</span></span>
<span data-ttu-id="e857a-137">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="e857a-137">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="e857a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e857a-138">CommonParameters</span></span>
<span data-ttu-id="e857a-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e857a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e857a-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e857a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e857a-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="e857a-141">INPUTS</span></span>

### <span data-ttu-id="e857a-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e857a-142">None</span></span>

## <span data-ttu-id="e857a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e857a-143">OUTPUTS</span></span>

### <span data-ttu-id="e857a-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span><span class="sxs-lookup"><span data-stu-id="e857a-144">Microsoft.Azure.Commands.Consumption.Models.PSUsageDetail</span></span>

## <span data-ttu-id="e857a-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e857a-145">NOTES</span></span>

## <span data-ttu-id="e857a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e857a-146">RELATED LINKS</span></span>
