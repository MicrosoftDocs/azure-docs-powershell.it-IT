---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotMetrics.md
ms.openlocfilehash: 474f5a450adba9f01ef56fe99875d062ece1689d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861913"
---
# <span data-ttu-id="eeb28-101">Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="eeb28-101">Get-AzWebAppSlotMetrics</span></span>

## <span data-ttu-id="eeb28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eeb28-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb28-103">Ottiene le metriche per uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="eeb28-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="eeb28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eeb28-104">SYNTAX</span></span>

### <span data-ttu-id="eeb28-105">S1</span><span class="sxs-lookup"><span data-stu-id="eeb28-105">S1</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeb28-106">S2</span><span class="sxs-lookup"><span data-stu-id="eeb28-106">S2</span></span>
```
Get-AzWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eeb28-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eeb28-107">DESCRIPTION</span></span>
<span data-ttu-id="eeb28-108">**Get-AzWebAppSlotMetrics** ottiene le metriche delle app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="eeb28-108">The **Get-AzWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="eeb28-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eeb28-109">EXAMPLES</span></span>

### <span data-ttu-id="eeb28-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eeb28-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="eeb28-111">Questo comando ottiene la richiesta dell'app Web specificata al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="eeb28-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="eeb28-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eeb28-112">PARAMETERS</span></span>

### <span data-ttu-id="eeb28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb28-113">-DefaultProfile</span></span>
<span data-ttu-id="eeb28-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb28-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeb28-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="eeb28-115">-EndTime</span></span>
<span data-ttu-id="eeb28-116">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="eeb28-116">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb28-117">-Granularità</span><span class="sxs-lookup"><span data-stu-id="eeb28-117">-Granularity</span></span>
<span data-ttu-id="eeb28-118">Granularità</span><span class="sxs-lookup"><span data-stu-id="eeb28-118">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb28-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="eeb28-119">-InstanceDetails</span></span>
<span data-ttu-id="eeb28-120">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="eeb28-120">Instance Details</span></span>

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

### <span data-ttu-id="eeb28-121">-Metriche</span><span class="sxs-lookup"><span data-stu-id="eeb28-121">-Metrics</span></span>
<span data-ttu-id="eeb28-122">Metriche</span><span class="sxs-lookup"><span data-stu-id="eeb28-122">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb28-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="eeb28-123">-Name</span></span>
<span data-ttu-id="eeb28-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="eeb28-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb28-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb28-125">-ResourceGroupName</span></span>
<span data-ttu-id="eeb28-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="eeb28-126">Resource Group Name</span></span>

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

### <span data-ttu-id="eeb28-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="eeb28-127">-Slot</span></span>
<span data-ttu-id="eeb28-128">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="eeb28-128">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb28-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="eeb28-129">-StartTime</span></span>
<span data-ttu-id="eeb28-130">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="eeb28-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb28-131">-Web App</span><span class="sxs-lookup"><span data-stu-id="eeb28-131">-WebApp</span></span>
<span data-ttu-id="eeb28-132">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="eeb28-132">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb28-133">CommonParameters</span></span>
<span data-ttu-id="eeb28-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb28-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb28-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb28-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eeb28-136">INPUTS</span></span>

### <span data-ttu-id="eeb28-137">Sito</span><span class="sxs-lookup"><span data-stu-id="eeb28-137">Site</span></span>
<span data-ttu-id="eeb28-138">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="eeb28-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eeb28-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eeb28-139">OUTPUTS</span></span>

## <span data-ttu-id="eeb28-140">Note</span><span class="sxs-lookup"><span data-stu-id="eeb28-140">NOTES</span></span>

## <span data-ttu-id="eeb28-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eeb28-141">RELATED LINKS</span></span>

[<span data-ttu-id="eeb28-142">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="eeb28-142">Get-AzAppServicePlanMetrics</span></span>](./Get-AzAppServicePlanMetrics.md)

[<span data-ttu-id="eeb28-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eeb28-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="eeb28-144">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eeb28-144">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
