---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotMetrics.md
ms.openlocfilehash: 9c4399146d99da6317c70fc08f7b01dc9679525a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512116"
---
# <span data-ttu-id="bb5fb-101">Get-AzureRmWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="bb5fb-101">Get-AzureRmWebAppSlotMetrics</span></span>

## <span data-ttu-id="bb5fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5fb-103">Ottiene le metriche per uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bb5fb-103">Gets metrics for an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb5fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb5fb-104">SYNTAX</span></span>

### <span data-ttu-id="bb5fb-105">S1</span><span class="sxs-lookup"><span data-stu-id="bb5fb-105">S1</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb5fb-106">S2</span><span class="sxs-lookup"><span data-stu-id="bb5fb-106">S2</span></span>
```
Get-AzureRmWebAppSlotMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb5fb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb5fb-107">DESCRIPTION</span></span>
<span data-ttu-id="bb5fb-108">**Get-AzureRmWebAppSlotMetrics** ottiene le metriche delle app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="bb5fb-108">The **Get-AzureRmWebAppSlotMetrics** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="bb5fb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb5fb-109">EXAMPLES</span></span>

### <span data-ttu-id="bb5fb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb5fb-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="bb5fb-111">Questo comando ottiene la richiesta dell'app Web specificata al minuto (PT1M-poll Time 1 minute) tra StartTime e EndTime</span><span class="sxs-lookup"><span data-stu-id="bb5fb-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="bb5fb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb5fb-112">PARAMETERS</span></span>

### <span data-ttu-id="bb5fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5fb-113">-DefaultProfile</span></span>
<span data-ttu-id="bb5fb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb5fb-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bb5fb-115">-EndTime</span></span>
<span data-ttu-id="bb5fb-116">Ora di fine in UTC</span><span class="sxs-lookup"><span data-stu-id="bb5fb-116">End Time in UTC</span></span>

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

### <span data-ttu-id="bb5fb-117">-Granularità</span><span class="sxs-lookup"><span data-stu-id="bb5fb-117">-Granularity</span></span>
<span data-ttu-id="bb5fb-118">Granularità</span><span class="sxs-lookup"><span data-stu-id="bb5fb-118">Granularity</span></span>

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

### <span data-ttu-id="bb5fb-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="bb5fb-119">-InstanceDetails</span></span>
<span data-ttu-id="bb5fb-120">Dettagli istanza</span><span class="sxs-lookup"><span data-stu-id="bb5fb-120">Instance Details</span></span>

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

### <span data-ttu-id="bb5fb-121">-Metriche</span><span class="sxs-lookup"><span data-stu-id="bb5fb-121">-Metrics</span></span>
<span data-ttu-id="bb5fb-122">Metriche</span><span class="sxs-lookup"><span data-stu-id="bb5fb-122">Metrics</span></span>

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

### <span data-ttu-id="bb5fb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb5fb-123">-Name</span></span>
<span data-ttu-id="bb5fb-124">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="bb5fb-124">WebApp Name</span></span>

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

### <span data-ttu-id="bb5fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb5fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb5fb-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bb5fb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="bb5fb-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="bb5fb-127">-Slot</span></span>
<span data-ttu-id="bb5fb-128">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="bb5fb-128">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bb5fb-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bb5fb-129">-StartTime</span></span>
<span data-ttu-id="bb5fb-130">Ora di inizio in UTC</span><span class="sxs-lookup"><span data-stu-id="bb5fb-130">Start Time in UTC</span></span>

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

### <span data-ttu-id="bb5fb-131">-Web App</span><span class="sxs-lookup"><span data-stu-id="bb5fb-131">-WebApp</span></span>
<span data-ttu-id="bb5fb-132">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="bb5fb-132">WebApp Object</span></span>

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

### <span data-ttu-id="bb5fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5fb-133">CommonParameters</span></span>
<span data-ttu-id="bb5fb-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb5fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5fb-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5fb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5fb-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb5fb-136">INPUTS</span></span>

### <span data-ttu-id="bb5fb-137">Sito</span><span class="sxs-lookup"><span data-stu-id="bb5fb-137">Site</span></span>
<span data-ttu-id="bb5fb-138">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bb5fb-138">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bb5fb-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb5fb-139">OUTPUTS</span></span>

## <span data-ttu-id="bb5fb-140">Note</span><span class="sxs-lookup"><span data-stu-id="bb5fb-140">NOTES</span></span>

## <span data-ttu-id="bb5fb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb5fb-141">RELATED LINKS</span></span>

[<span data-ttu-id="bb5fb-142">Get-AzureRMAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="bb5fb-142">Get-AzureRMAppServicePlanMetrics</span></span>](./Get-AzureRmAppServicePlanMetrics.md)

[<span data-ttu-id="bb5fb-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="bb5fb-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="bb5fb-144">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bb5fb-144">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)