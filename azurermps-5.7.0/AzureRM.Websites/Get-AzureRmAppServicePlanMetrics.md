---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: f3376f40246640b8de52ffa138912c768486a3dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686991"
---
# <span data-ttu-id="224ed-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="224ed-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="224ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="224ed-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="224ed-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="224ed-103">SYNTAX</span></span>

### <span data-ttu-id="224ed-104">S1</span><span class="sxs-lookup"><span data-stu-id="224ed-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="224ed-105">S2</span><span class="sxs-lookup"><span data-stu-id="224ed-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="224ed-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="224ed-106">DESCRIPTION</span></span>
<span data-ttu-id="224ed-107">Il **Get-AzureRmAppServicePlanMetrics** ottiene le metriche del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="224ed-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="224ed-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="224ed-108">EXAMPLES</span></span>

### <span data-ttu-id="224ed-109">1:</span><span class="sxs-lookup"><span data-stu-id="224ed-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="224ed-110">Questo comando consente di ottenere la percentuale di CPU del piano di servizio app al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="224ed-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="224ed-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="224ed-111">PARAMETERS</span></span>

### <span data-ttu-id="224ed-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="224ed-112">-AppServicePlan</span></span>
<span data-ttu-id="224ed-113">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="224ed-113">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="224ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224ed-114">-DefaultProfile</span></span>
<span data-ttu-id="224ed-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="224ed-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="224ed-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="224ed-116">-EndTime</span></span>
<span data-ttu-id="224ed-117">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="224ed-117">End Time in UTC</span></span>

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

### <span data-ttu-id="224ed-118">-Granularità</span><span class="sxs-lookup"><span data-stu-id="224ed-118">-Granularity</span></span>
<span data-ttu-id="224ed-119">Granularità</span><span class="sxs-lookup"><span data-stu-id="224ed-119">Granularity</span></span>

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

### <span data-ttu-id="224ed-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="224ed-120">-InstanceDetails</span></span>
<span data-ttu-id="224ed-121">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="224ed-121">Instance Details</span></span>

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

### <span data-ttu-id="224ed-122">-Metriche</span><span class="sxs-lookup"><span data-stu-id="224ed-122">-Metrics</span></span>
<span data-ttu-id="224ed-123">Metriche</span><span class="sxs-lookup"><span data-stu-id="224ed-123">Metrics</span></span>

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

### <span data-ttu-id="224ed-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="224ed-124">-Name</span></span>
<span data-ttu-id="224ed-125">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="224ed-125">App Service Plan Name</span></span>

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

### <span data-ttu-id="224ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="224ed-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="224ed-127">Resource Group Name</span></span>

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

### <span data-ttu-id="224ed-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="224ed-128">-StartTime</span></span>
<span data-ttu-id="224ed-129">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="224ed-129">Start Time in UTC</span></span>

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

### <span data-ttu-id="224ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224ed-130">CommonParameters</span></span>
<span data-ttu-id="224ed-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="224ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224ed-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="224ed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224ed-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="224ed-133">INPUTS</span></span>

### <span data-ttu-id="224ed-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="224ed-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="224ed-135">Il parametro ' AppServicePlan ' accetta il valore di tipo ' ServerFarmWithRichSku ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="224ed-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="224ed-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="224ed-136">OUTPUTS</span></span>

## <span data-ttu-id="224ed-137">Note</span><span class="sxs-lookup"><span data-stu-id="224ed-137">NOTES</span></span>

## <span data-ttu-id="224ed-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="224ed-138">RELATED LINKS</span></span>

