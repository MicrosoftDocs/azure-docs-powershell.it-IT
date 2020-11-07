---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861958"
---
# <span data-ttu-id="5c950-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="5c950-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="5c950-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c950-102">SYNOPSIS</span></span>
<span data-ttu-id="5c950-103">Ottiene le metriche del piano di servizio Web Azure.</span><span class="sxs-lookup"><span data-stu-id="5c950-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="5c950-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c950-104">SYNTAX</span></span>

### <span data-ttu-id="5c950-105">S1</span><span class="sxs-lookup"><span data-stu-id="5c950-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c950-106">S2</span><span class="sxs-lookup"><span data-stu-id="5c950-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c950-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c950-107">DESCRIPTION</span></span>
<span data-ttu-id="5c950-108">Il **Get-AzAppServicePlanMetrics** ottiene le metriche del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="5c950-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="5c950-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c950-109">EXAMPLES</span></span>

### <span data-ttu-id="5c950-110">1:</span><span class="sxs-lookup"><span data-stu-id="5c950-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="5c950-111">Questo comando consente di ottenere la percentuale di CPU del piano di servizio app al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="5c950-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="5c950-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c950-112">PARAMETERS</span></span>

### <span data-ttu-id="5c950-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5c950-113">-AppServicePlan</span></span>
<span data-ttu-id="5c950-114">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="5c950-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c950-115">-DefaultProfile</span></span>
<span data-ttu-id="5c950-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c950-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5c950-117">-EndTime</span></span>
<span data-ttu-id="5c950-118">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="5c950-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-119">-Granularità</span><span class="sxs-lookup"><span data-stu-id="5c950-119">-Granularity</span></span>
<span data-ttu-id="5c950-120">Granularità</span><span class="sxs-lookup"><span data-stu-id="5c950-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="5c950-121">-InstanceDetails</span></span>
<span data-ttu-id="5c950-122">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="5c950-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-123">-Metriche</span><span class="sxs-lookup"><span data-stu-id="5c950-123">-Metrics</span></span>
<span data-ttu-id="5c950-124">Metriche</span><span class="sxs-lookup"><span data-stu-id="5c950-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c950-125">-Name</span></span>
<span data-ttu-id="5c950-126">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="5c950-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c950-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c950-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5c950-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5c950-129">-StartTime</span></span>
<span data-ttu-id="5c950-130">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="5c950-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c950-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c950-131">CommonParameters</span></span>
<span data-ttu-id="5c950-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c950-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c950-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c950-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c950-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c950-134">INPUTS</span></span>

### <span data-ttu-id="5c950-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="5c950-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="5c950-136">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5c950-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="5c950-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c950-137">OUTPUTS</span></span>

## <span data-ttu-id="5c950-138">Note</span><span class="sxs-lookup"><span data-stu-id="5c950-138">NOTES</span></span>

## <span data-ttu-id="5c950-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c950-139">RELATED LINKS</span></span>

