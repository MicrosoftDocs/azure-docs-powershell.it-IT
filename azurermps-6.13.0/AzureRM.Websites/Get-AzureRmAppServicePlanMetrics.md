---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: a8bb330315cfdd43e30ab790afcdeba0b09cef08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516343"
---
# <span data-ttu-id="a557a-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="a557a-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="a557a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a557a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a557a-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a557a-103">SYNTAX</span></span>

### <span data-ttu-id="a557a-104">S1</span><span class="sxs-lookup"><span data-stu-id="a557a-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a557a-105">S2</span><span class="sxs-lookup"><span data-stu-id="a557a-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a557a-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a557a-106">DESCRIPTION</span></span>
<span data-ttu-id="a557a-107">Il **Get-AzureRmAppServicePlanMetrics** ottiene le metriche del piano di servizio app.</span><span class="sxs-lookup"><span data-stu-id="a557a-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="a557a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a557a-108">EXAMPLES</span></span>

### <span data-ttu-id="a557a-109">1:</span><span class="sxs-lookup"><span data-stu-id="a557a-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "CPU Percentage"
```

<span data-ttu-id="a557a-110">Questo comando consente di ottenere la percentuale di CPU del piano di servizio app al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="a557a-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="a557a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a557a-111">PARAMETERS</span></span>

### <span data-ttu-id="a557a-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a557a-112">-AppServicePlan</span></span>
<span data-ttu-id="a557a-113">Oggetto piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="a557a-113">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a557a-114">-DefaultProfile</span></span>
<span data-ttu-id="a557a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a557a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a557a-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a557a-116">-EndTime</span></span>
<span data-ttu-id="a557a-117">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="a557a-117">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-118">-Granularità</span><span class="sxs-lookup"><span data-stu-id="a557a-118">-Granularity</span></span>
<span data-ttu-id="a557a-119">Granularità</span><span class="sxs-lookup"><span data-stu-id="a557a-119">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="a557a-120">-InstanceDetails</span></span>
<span data-ttu-id="a557a-121">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="a557a-121">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-122">-Metriche</span><span class="sxs-lookup"><span data-stu-id="a557a-122">-Metrics</span></span>
<span data-ttu-id="a557a-123">Metriche</span><span class="sxs-lookup"><span data-stu-id="a557a-123">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a557a-124">-Name</span></span>
<span data-ttu-id="a557a-125">Nome piano servizio app</span><span class="sxs-lookup"><span data-stu-id="a557a-125">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a557a-126">-ResourceGroupName</span></span>
<span data-ttu-id="a557a-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a557a-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a557a-128">-StartTime</span></span>
<span data-ttu-id="a557a-129">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="a557a-129">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a557a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a557a-130">CommonParameters</span></span>
<span data-ttu-id="a557a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a557a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a557a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a557a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a557a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a557a-133">INPUTS</span></span>

### <span data-ttu-id="a557a-134">Microsoft. Azure. Management. website. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a557a-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="a557a-135">Parametri: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a557a-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="a557a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a557a-136">OUTPUTS</span></span>

### <span data-ttu-id="a557a-137">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="a557a-137">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="a557a-138">Note</span><span class="sxs-lookup"><span data-stu-id="a557a-138">NOTES</span></span>

## <span data-ttu-id="a557a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a557a-139">RELATED LINKS</span></span>
