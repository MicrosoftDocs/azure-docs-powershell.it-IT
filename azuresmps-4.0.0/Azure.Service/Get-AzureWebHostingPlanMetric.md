---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029972"
---
# <span data-ttu-id="b4e7a-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="b4e7a-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="b4e7a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e7a-103">Ottiene le metriche per i piani di hosting di siti Web Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="b4e7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4e7a-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4e7a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e7a-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b4e7a-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b4e7a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b4e7a-108">Il cmdlet **Get-AzureWebHostingPlanMetric** ottiene le metriche per i piani di hosting di Azure Web in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="b4e7a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="b4e7a-110">Esempio 1: ottenere le metriche per le ultime tre ore a un livello per istanza</span><span class="sxs-lookup"><span data-stu-id="b4e7a-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

<span data-ttu-id="b4e7a-111">Questo comando ottiene le metriche del piano di hosting Web per le ultime tre ore sul livello per istanza.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="b4e7a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4e7a-112">PARAMETERS</span></span>

### <span data-ttu-id="b4e7a-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b4e7a-113">-EndDate</span></span>
<span data-ttu-id="b4e7a-114">Specifica l'ora di fine, come oggetto **DateTime** , da cui restituire le metriche.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="b4e7a-115">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="b4e7a-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="b4e7a-116">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b4e7a-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="b4e7a-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="b4e7a-117">-InstanceDetails</span></span>
<span data-ttu-id="b4e7a-118">Indica che questo cmdlet include dettagli su un livello per istanza.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="b4e7a-119">Se il piano di hosting del sito Web viene eseguito su due o più computer, questo cmdlet restituisce le metriche dettagliate per ogni computer.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

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

### <span data-ttu-id="b4e7a-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="b4e7a-120">-MetricNames</span></span>
<span data-ttu-id="b4e7a-121">Specie una matrice di metriche da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="b4e7a-122">Se non specifichi un valore per questo parametro, questo cmdlet otterrà tutte le metriche.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="b4e7a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4e7a-123">-Name</span></span>
<span data-ttu-id="b4e7a-124">Specifica il nome di un piano nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="b4e7a-125">Per impostazione predefinita, **Get-AzureWebHostingPlanMetric** ottiene tutti i siti Web nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="b4e7a-126">Questo parametro non supporta i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-126">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="b4e7a-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="b4e7a-127">-Profile</span></span>
<span data-ttu-id="b4e7a-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4e7a-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4e7a-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b4e7a-130">-StartDate</span></span>
<span data-ttu-id="b4e7a-131">Specifica l'ora di inizio, come oggetto **DateTime** , per cui ottenere le metriche.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

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

### <span data-ttu-id="b4e7a-132">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="b4e7a-132">-TimeGrain</span></span>
<span data-ttu-id="b4e7a-133">Specifica l'unità di tempo per cui ottenere le metriche.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="b4e7a-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b4e7a-134">Valid values are:</span></span> 

- <span data-ttu-id="b4e7a-135">PT1M (minuto)</span><span class="sxs-lookup"><span data-stu-id="b4e7a-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="b4e7a-136">PT1H (ora)</span><span class="sxs-lookup"><span data-stu-id="b4e7a-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="b4e7a-137">P1D (giorno)</span><span class="sxs-lookup"><span data-stu-id="b4e7a-137">P1D (Day)</span></span>

<span data-ttu-id="b4e7a-138">Il valore predefinito è PT1H.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-138">The default value is PT1H.</span></span>

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

### <span data-ttu-id="b4e7a-139">-Webspacename</span><span class="sxs-lookup"><span data-stu-id="b4e7a-139">-WebSpaceName</span></span>
<span data-ttu-id="b4e7a-140">Specifica il nome di uno spazio Web nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="b4e7a-141">Per impostazione predefinita, **Get-AzureWebHostingPlanMetric** ottiene tutti i piani della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="b4e7a-142">Questo parametro non supporta i caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-142">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e7a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e7a-143">CommonParameters</span></span>
<span data-ttu-id="b4e7a-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e7a-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e7a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e7a-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4e7a-146">INPUTS</span></span>

###  
<span data-ttu-id="b4e7a-147">Puoi passare l'input al cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="b4e7a-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b4e7a-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4e7a-148">OUTPUTS</span></span>

###  
<span data-ttu-id="b4e7a-149">Microsoft. WindowsAzure. Commands. Utilities. Web. Services. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="b4e7a-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="b4e7a-150">Per impostazione predefinita, **Get-AzureWebHostingPlanMetric** restituisce una matrice di oggetti **MetricResponse** .</span><span class="sxs-lookup"><span data-stu-id="b4e7a-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="b4e7a-151">Note</span><span class="sxs-lookup"><span data-stu-id="b4e7a-151">NOTES</span></span>

## <span data-ttu-id="b4e7a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4e7a-152">RELATED LINKS</span></span>

[<span data-ttu-id="b4e7a-153">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="b4e7a-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


