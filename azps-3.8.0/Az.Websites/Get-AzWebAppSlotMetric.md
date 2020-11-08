---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 27800007756f8de91f23feab2f3cc1bd5206aa76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019805"
---
# <span data-ttu-id="cc6f5-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="cc6f5-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="cc6f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="cc6f5-103">Ottiene le metriche per uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="cc6f5-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="cc6f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc6f5-104">SYNTAX</span></span>

### <span data-ttu-id="cc6f5-105">S1</span><span class="sxs-lookup"><span data-stu-id="cc6f5-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc6f5-106">S2</span><span class="sxs-lookup"><span data-stu-id="cc6f5-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc6f5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc6f5-107">DESCRIPTION</span></span>
<span data-ttu-id="cc6f5-108">**Get-AzWebAppSlotMetric** ottiene le metriche delle app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="cc6f5-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="cc6f5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc6f5-109">EXAMPLES</span></span>

### <span data-ttu-id="cc6f5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cc6f5-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="cc6f5-111">Questo comando ottiene la richiesta dell'app Web specificata al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="cc6f5-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="cc6f5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc6f5-112">PARAMETERS</span></span>

### <span data-ttu-id="cc6f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc6f5-113">-DefaultProfile</span></span>
<span data-ttu-id="cc6f5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc6f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc6f5-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="cc6f5-115">-EndTime</span></span>
<span data-ttu-id="cc6f5-116">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="cc6f5-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6f5-117">-Granularità</span><span class="sxs-lookup"><span data-stu-id="cc6f5-117">-Granularity</span></span>
<span data-ttu-id="cc6f5-118">Granularità</span><span class="sxs-lookup"><span data-stu-id="cc6f5-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6f5-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="cc6f5-119">-InstanceDetails</span></span>
<span data-ttu-id="cc6f5-120">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="cc6f5-120">Instance Details</span></span>

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

### <span data-ttu-id="cc6f5-121">-Metriche</span><span class="sxs-lookup"><span data-stu-id="cc6f5-121">-Metrics</span></span>
<span data-ttu-id="cc6f5-122">Metriche</span><span class="sxs-lookup"><span data-stu-id="cc6f5-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6f5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc6f5-123">-Name</span></span>
<span data-ttu-id="cc6f5-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="cc6f5-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc6f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc6f5-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cc6f5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cc6f5-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="cc6f5-127">-Slot</span></span>
<span data-ttu-id="cc6f5-128">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="cc6f5-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6f5-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cc6f5-129">-StartTime</span></span>
<span data-ttu-id="cc6f5-130">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="cc6f5-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc6f5-131">-Web App</span><span class="sxs-lookup"><span data-stu-id="cc6f5-131">-WebApp</span></span>
<span data-ttu-id="cc6f5-132">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="cc6f5-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc6f5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc6f5-133">CommonParameters</span></span>
<span data-ttu-id="cc6f5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc6f5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc6f5-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc6f5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc6f5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc6f5-136">INPUTS</span></span>

### <span data-ttu-id="cc6f5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cc6f5-137">System.String</span></span>

### <span data-ttu-id="cc6f5-138">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cc6f5-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cc6f5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc6f5-139">OUTPUTS</span></span>

### <span data-ttu-id="cc6f5-140">Microsoft. Azure. Management. website. Models. ResourceMetric</span><span class="sxs-lookup"><span data-stu-id="cc6f5-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="cc6f5-141">Note</span><span class="sxs-lookup"><span data-stu-id="cc6f5-141">NOTES</span></span>

## <span data-ttu-id="cc6f5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc6f5-142">RELATED LINKS</span></span>

[<span data-ttu-id="cc6f5-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="cc6f5-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="cc6f5-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cc6f5-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="cc6f5-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc6f5-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
