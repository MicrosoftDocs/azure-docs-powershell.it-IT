---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029733"
---
# <span data-ttu-id="ca89f-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="ca89f-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="ca89f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca89f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca89f-103">Ottiene le metriche per il sito Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ca89f-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="ca89f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca89f-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ca89f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca89f-105">DESCRIPTION</span></span>
<span data-ttu-id="ca89f-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ca89f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ca89f-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ca89f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ca89f-108">Il cmdlet **Get-AzureWebsiteMetric** ottiene le metriche per il sito Web di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ca89f-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="ca89f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca89f-109">EXAMPLES</span></span>

### <span data-ttu-id="ca89f-110">Esempio 1: ottenere le metriche per le ultime tre ore su un livello per istanza per un sito Web</span><span class="sxs-lookup"><span data-stu-id="ca89f-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="ca89f-111">Questo comando ottiene le metriche per le ultime tre ore in un livello per istanza per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="ca89f-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="ca89f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca89f-112">PARAMETERS</span></span>

### <span data-ttu-id="ca89f-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ca89f-113">-EndDate</span></span>
<span data-ttu-id="ca89f-114">Specifica l'ora, come oggetto **DateTime** , per interrompere l'ottenimento delle metriche.</span><span class="sxs-lookup"><span data-stu-id="ca89f-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="ca89f-115">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="ca89f-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ca89f-116">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ca89f-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="ca89f-117">-InstanceDetails</span></span>
<span data-ttu-id="ca89f-118">Indica che questo cmdlet include dettagli su un livello per istanza.</span><span class="sxs-lookup"><span data-stu-id="ca89f-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="ca89f-119">Se il piano di hosting Web viene eseguito in due o più computer, questo cmdlet restituisce le metriche per ogni computer.</span><span class="sxs-lookup"><span data-stu-id="ca89f-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="ca89f-120">-MetricNames</span></span>
<span data-ttu-id="ca89f-121">Specifica una matrice di metriche da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ca89f-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="ca89f-122">Se non specifichi questo parametro, il cmdlet otterrà tutte le metriche.</span><span class="sxs-lookup"><span data-stu-id="ca89f-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca89f-123">-Name</span></span>
<span data-ttu-id="ca89f-124">Specifica il nome di un sito Web nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ca89f-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="ca89f-125">Questo parametro non supporta i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ca89f-125">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="ca89f-126">-Profile</span></span>
<span data-ttu-id="ca89f-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca89f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca89f-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ca89f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="ca89f-129">-Slot</span></span>
<span data-ttu-id="ca89f-130">Specifica l'ambiente di una distribuzione del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="ca89f-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="ca89f-131">I valori validi sono: produzione e staging.</span><span class="sxs-lookup"><span data-stu-id="ca89f-131">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="ca89f-132">-SlotView</span></span>
<span data-ttu-id="ca89f-133">Indica che questo cmdlet ottiene le metriche per i nomi host che ricevono il traffico nello slot corrente.</span><span class="sxs-lookup"><span data-stu-id="ca89f-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="ca89f-134">Se si verifica uno scambio durante il periodo di tempo, le metriche vengono unite.</span><span class="sxs-lookup"><span data-stu-id="ca89f-134">If a swap occurs during the time period, the metrics are merged.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ca89f-135">-StartDate</span></span>
<span data-ttu-id="ca89f-136">Specifica l'ora, come oggetto **DateTime** , per iniziare a ottenere le metriche.</span><span class="sxs-lookup"><span data-stu-id="ca89f-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-137">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="ca89f-137">-TimeGrain</span></span>
<span data-ttu-id="ca89f-138">Specifica l'unità di tempo per le metriche.</span><span class="sxs-lookup"><span data-stu-id="ca89f-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="ca89f-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ca89f-139">Valid values are:</span></span> 

- <span data-ttu-id="ca89f-140">PT1M (minuto)</span><span class="sxs-lookup"><span data-stu-id="ca89f-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="ca89f-141">PT1H (ora)</span><span class="sxs-lookup"><span data-stu-id="ca89f-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="ca89f-142">P1D (giorno)</span><span class="sxs-lookup"><span data-stu-id="ca89f-142">P1D (Day)</span></span>

<span data-ttu-id="ca89f-143">Il valore predefinito è PT1H.</span><span class="sxs-lookup"><span data-stu-id="ca89f-143">The default value is PT1H.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca89f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca89f-144">CommonParameters</span></span>
<span data-ttu-id="ca89f-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca89f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca89f-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca89f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca89f-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca89f-147">INPUTS</span></span>

###  
<span data-ttu-id="ca89f-148">Puoi passare l'input al cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="ca89f-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ca89f-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca89f-149">OUTPUTS</span></span>

### <span data-ttu-id="ca89f-150">Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="ca89f-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="ca89f-151">Per impostazione predefinita, **Get-AzureWebsiteMetric** restituisce una matrice di oggetti **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="ca89f-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="ca89f-152">Note</span><span class="sxs-lookup"><span data-stu-id="ca89f-152">NOTES</span></span>

## <span data-ttu-id="ca89f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca89f-153">RELATED LINKS</span></span>

[<span data-ttu-id="ca89f-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ca89f-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


