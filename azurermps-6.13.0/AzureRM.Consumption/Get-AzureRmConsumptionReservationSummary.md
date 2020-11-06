---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationSummary.md
ms.openlocfilehash: 18f12e6ccf7f43aa832c00864192142457f45520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518803"
---
# <span data-ttu-id="559e5-101">Get-AzureRmConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="559e5-101">Get-AzureRmConsumptionReservationSummary</span></span>

## <span data-ttu-id="559e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="559e5-102">SYNOPSIS</span></span>
<span data-ttu-id="559e5-103">Ottenere riassunti di prenotazione per cereali giornalieri o mensili.</span><span class="sxs-lookup"><span data-stu-id="559e5-103">Get reservation summaries for daily or monthly grain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="559e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="559e5-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="559e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="559e5-105">DESCRIPTION</span></span>
<span data-ttu-id="559e5-106">Il cmdlet **Get-AzureRmConsumptionReservationSummay** ottiene i riassunti di prenotazione per i cereali giornalieri o mensili.</span><span class="sxs-lookup"><span data-stu-id="559e5-106">The **Get-AzureRmConsumptionReservationSummay** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="559e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="559e5-107">EXAMPLES</span></span>

### <span data-ttu-id="559e5-108">Esempio 1: ottenere riassunti di prenotazione con ID ordine di prenotazione per grain mensile</span><span class="sxs-lookup"><span data-stu-id="559e5-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="559e5-109">Esempio 2: ottenere riassunti di prenotazione con ID ordine di prenotazione e ID prenotazione per grain mensile</span><span class="sxs-lookup"><span data-stu-id="559e5-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="559e5-110">Esempio 3: ottenere riassunti di prenotazione con l'ID ordine di prenotazione per l'intervallo di date specificato in grana giornaliera</span><span class="sxs-lookup"><span data-stu-id="559e5-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="559e5-111">Esempio 4: ottenere riassunti di prenotazione con ID ordine di prenotazione e ID prenotazione per l'intervallo di date specificato in grana giornaliera</span><span class="sxs-lookup"><span data-stu-id="559e5-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="559e5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="559e5-112">PARAMETERS</span></span>

### <span data-ttu-id="559e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559e5-113">-DefaultProfile</span></span>
<span data-ttu-id="559e5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="559e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="559e5-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="559e5-115">-EndDate</span></span>
<span data-ttu-id="559e5-116">I dati finali (AAAA-MM-DD in UTC) del riepilogo della prenotazione, necessari solo per la granulosità giornaliera.</span><span class="sxs-lookup"><span data-stu-id="559e5-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="559e5-117">-Grana</span><span class="sxs-lookup"><span data-stu-id="559e5-117">-Grain</span></span>
<span data-ttu-id="559e5-118">Il periodo di tempo del riepilogo della prenotazione può essere giornaliero o mensile.</span><span class="sxs-lookup"><span data-stu-id="559e5-118">The time grain of the reservation summaryy, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559e5-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="559e5-119">-ReservationId</span></span>
<span data-ttu-id="559e5-120">Identificatore di una prenotazione in un ordine di prenotazione.</span><span class="sxs-lookup"><span data-stu-id="559e5-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="559e5-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="559e5-121">-ReservationOrderId</span></span>
<span data-ttu-id="559e5-122">Identificatore di un acquisto di prenotazione.</span><span class="sxs-lookup"><span data-stu-id="559e5-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="559e5-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="559e5-123">-StartDate</span></span>
<span data-ttu-id="559e5-124">I dati di inizio (AAAA-MM-DD in UTC) del riepilogo della prenotazione, necessari solo per la granulosità giornaliera.</span><span class="sxs-lookup"><span data-stu-id="559e5-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="559e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559e5-125">CommonParameters</span></span>
<span data-ttu-id="559e5-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="559e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559e5-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="559e5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559e5-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="559e5-128">INPUTS</span></span>

### <span data-ttu-id="559e5-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="559e5-129">None</span></span>

## <span data-ttu-id="559e5-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="559e5-130">OUTPUTS</span></span>

### <span data-ttu-id="559e5-131">Microsoft. Azure. Commands. consume. Models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="559e5-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="559e5-132">Note</span><span class="sxs-lookup"><span data-stu-id="559e5-132">NOTES</span></span>

## <span data-ttu-id="559e5-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="559e5-133">RELATED LINKS</span></span>
