---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
ms.openlocfilehash: 097b4c5ff6a4a9be32889f104c8e2c8fe0058b13
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865712"
---
# <span data-ttu-id="127d6-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="127d6-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="127d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="127d6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="127d6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="127d6-103">SYNTAX</span></span>

### <span data-ttu-id="127d6-104">S1</span><span class="sxs-lookup"><span data-stu-id="127d6-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="127d6-105">S2</span><span class="sxs-lookup"><span data-stu-id="127d6-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="127d6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="127d6-106">DESCRIPTION</span></span>
<span data-ttu-id="127d6-107">Il **Get-AzureRmAppServicePlanMetrics** ottiene le metriche del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="127d6-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="127d6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="127d6-108">EXAMPLES</span></span>

### <span data-ttu-id="127d6-109">1:</span><span class="sxs-lookup"><span data-stu-id="127d6-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="127d6-110">Questo comando consente di ottenere la percentuale di CPU del piano di servizio app al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="127d6-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="127d6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="127d6-111">PARAMETERS</span></span>

### <span data-ttu-id="127d6-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="127d6-112">-AppServicePlan</span></span>
<span data-ttu-id="127d6-113">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="127d6-113">App Service Plan Object</span></span>

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

### <span data-ttu-id="127d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127d6-114">-DefaultProfile</span></span>
<span data-ttu-id="127d6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="127d6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127d6-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="127d6-116">-EndTime</span></span>
<span data-ttu-id="127d6-117">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="127d6-117">End Time in UTC</span></span>

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

### <span data-ttu-id="127d6-118">-Granularità</span><span class="sxs-lookup"><span data-stu-id="127d6-118">-Granularity</span></span>
<span data-ttu-id="127d6-119">Granularità</span><span class="sxs-lookup"><span data-stu-id="127d6-119">Granularity</span></span>

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

### <span data-ttu-id="127d6-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="127d6-120">-InstanceDetails</span></span>
<span data-ttu-id="127d6-121">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="127d6-121">Instance Details</span></span>

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

### <span data-ttu-id="127d6-122">-Metriche</span><span class="sxs-lookup"><span data-stu-id="127d6-122">-Metrics</span></span>
<span data-ttu-id="127d6-123">Metriche</span><span class="sxs-lookup"><span data-stu-id="127d6-123">Metrics</span></span>

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

### <span data-ttu-id="127d6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="127d6-124">-Name</span></span>
<span data-ttu-id="127d6-125">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="127d6-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="127d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="127d6-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="127d6-127">Resource Group Name</span></span>

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

### <span data-ttu-id="127d6-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="127d6-128">-StartTime</span></span>
<span data-ttu-id="127d6-129">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="127d6-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="127d6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127d6-130">CommonParameters</span></span>
<span data-ttu-id="127d6-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127d6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127d6-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="127d6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127d6-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="127d6-133">INPUTS</span></span>

### <span data-ttu-id="127d6-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="127d6-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="127d6-135">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="127d6-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="127d6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="127d6-136">OUTPUTS</span></span>

## <span data-ttu-id="127d6-137">Note</span><span class="sxs-lookup"><span data-stu-id="127d6-137">NOTES</span></span>

## <span data-ttu-id="127d6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="127d6-138">RELATED LINKS</span></span>

