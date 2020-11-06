---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 93af61d0554435fae4b9d87170b9202026644e49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521122"
---
# <span data-ttu-id="57ea7-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="57ea7-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="57ea7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="57ea7-103">Ottiene le metriche per uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="57ea7-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57ea7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57ea7-104">SYNTAX</span></span>

### <span data-ttu-id="57ea7-105">S1</span><span class="sxs-lookup"><span data-stu-id="57ea7-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57ea7-106">S2</span><span class="sxs-lookup"><span data-stu-id="57ea7-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57ea7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57ea7-107">DESCRIPTION</span></span>
<span data-ttu-id="57ea7-108">**Get-AzureRmWebAppSlotMetrics** ottiene le metriche delle app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="57ea7-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="57ea7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57ea7-109">EXAMPLES</span></span>

### <span data-ttu-id="57ea7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57ea7-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="57ea7-111">Questo comando ottiene la richiesta dell'app Web specificata al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="57ea7-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="57ea7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57ea7-112">PARAMETERS</span></span>

### <span data-ttu-id="57ea7-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="57ea7-113">-EndTime</span></span>
<span data-ttu-id="57ea7-114">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="57ea7-114">End Time in UTC</span></span>

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

### <span data-ttu-id="57ea7-115">-Granularità</span><span class="sxs-lookup"><span data-stu-id="57ea7-115">-Granularity</span></span>
<span data-ttu-id="57ea7-116">Granularità</span><span class="sxs-lookup"><span data-stu-id="57ea7-116">Granularity</span></span>

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

### <span data-ttu-id="57ea7-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="57ea7-117">-InstanceDetails</span></span>
<span data-ttu-id="57ea7-118">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="57ea7-118">Instance Details</span></span>

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

### <span data-ttu-id="57ea7-119">-Metriche</span><span class="sxs-lookup"><span data-stu-id="57ea7-119">-Metrics</span></span>
<span data-ttu-id="57ea7-120">Metriche</span><span class="sxs-lookup"><span data-stu-id="57ea7-120">Metrics</span></span>

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

### <span data-ttu-id="57ea7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="57ea7-121">-Name</span></span>
<span data-ttu-id="57ea7-122">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="57ea7-122">WebApp Name</span></span>

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

### <span data-ttu-id="57ea7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57ea7-123">-ResourceGroupName</span></span>
<span data-ttu-id="57ea7-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="57ea7-124">Resource Group Name</span></span>

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

### <span data-ttu-id="57ea7-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="57ea7-125">-Slot</span></span>
<span data-ttu-id="57ea7-126">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="57ea7-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="57ea7-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="57ea7-127">-StartTime</span></span>
<span data-ttu-id="57ea7-128">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="57ea7-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="57ea7-129">-Web App</span><span class="sxs-lookup"><span data-stu-id="57ea7-129">-WebApp</span></span>
<span data-ttu-id="57ea7-130">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="57ea7-130">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57ea7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ea7-131">-DefaultProfile</span></span>
<span data-ttu-id="57ea7-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57ea7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57ea7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ea7-133">CommonParameters</span></span>
<span data-ttu-id="57ea7-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ea7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ea7-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ea7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ea7-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57ea7-136">INPUTS</span></span>

### <span data-ttu-id="57ea7-137">Sito</span><span class="sxs-lookup"><span data-stu-id="57ea7-137">Site</span></span>
<span data-ttu-id="57ea7-138">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="57ea7-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="57ea7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57ea7-139">OUTPUTS</span></span>

## <span data-ttu-id="57ea7-140">Note</span><span class="sxs-lookup"><span data-stu-id="57ea7-140">NOTES</span></span>

## <span data-ttu-id="57ea7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57ea7-141">RELATED LINKS</span></span>

[<span data-ttu-id="57ea7-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="57ea7-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="57ea7-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="57ea7-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="57ea7-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57ea7-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)
