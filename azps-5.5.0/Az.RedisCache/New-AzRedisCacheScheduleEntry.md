---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachescheduleentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheScheduleEntry.md
ms.openlocfilehash: e3976c1008388c85a04715541d0d88e164a422e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206130"
---
# <span data-ttu-id="c23ed-101">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="c23ed-101">New-AzRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="c23ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c23ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c23ed-103">Crea una voce di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c23ed-103">Creates a schedule entry.</span></span>

## <span data-ttu-id="c23ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c23ed-104">SYNTAX</span></span>

```
New-AzRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c23ed-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c23ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c23ed-106">Il cmdlet **New-AzRedisCacheScheduleEntry** crea un **oggetto PSScheduleEntry.**</span><span class="sxs-lookup"><span data-stu-id="c23ed-106">The **New-AzRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="c23ed-107">I cmdlet di pianificazione delle patch della cache di Azure Redis, come il cmdlet New-AzRedisCachePatchSchedule, richiedono oggetti di voci di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="c23ed-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="c23ed-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c23ed-108">EXAMPLES</span></span>

### <span data-ttu-id="c23ed-109">Esempio 1: Creare una voce di programmazione per i fine settimana</span><span class="sxs-lookup"><span data-stu-id="c23ed-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="c23ed-110">Questo comando crea un **oggetto PSScheduleEntry che** rappresenta una pianificazione festivi con l'ora di inizio e la finestra specificate.</span><span class="sxs-lookup"><span data-stu-id="c23ed-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="c23ed-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c23ed-111">PARAMETERS</span></span>

### <span data-ttu-id="c23ed-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="c23ed-112">-DayOfWeek</span></span>
<span data-ttu-id="c23ed-113">Specifica il giorno della settimana per la voce di programmazione.</span><span class="sxs-lookup"><span data-stu-id="c23ed-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="c23ed-114">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="c23ed-114">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c23ed-115">Ogni giorno</span><span class="sxs-lookup"><span data-stu-id="c23ed-115">Everyday</span></span> 
- <span data-ttu-id="c23ed-116">Fine settimana</span><span class="sxs-lookup"><span data-stu-id="c23ed-116">Weekend</span></span> 
- <span data-ttu-id="c23ed-117">Lunedì</span><span class="sxs-lookup"><span data-stu-id="c23ed-117">Monday</span></span> 
- <span data-ttu-id="c23ed-118">Martedì</span><span class="sxs-lookup"><span data-stu-id="c23ed-118">Tuesday</span></span> 
- <span data-ttu-id="c23ed-119">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="c23ed-119">Wednesday</span></span> 
- <span data-ttu-id="c23ed-120">Giovedì</span><span class="sxs-lookup"><span data-stu-id="c23ed-120">Thursday</span></span> 
- <span data-ttu-id="c23ed-121">Venerdì</span><span class="sxs-lookup"><span data-stu-id="c23ed-121">Friday</span></span> 
- <span data-ttu-id="c23ed-122">Sabato</span><span class="sxs-lookup"><span data-stu-id="c23ed-122">Saturday</span></span> 
- <span data-ttu-id="c23ed-123">Domenica</span><span class="sxs-lookup"><span data-stu-id="c23ed-123">Sunday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Everyday, Weekend, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23ed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23ed-124">-DefaultProfile</span></span>
<span data-ttu-id="c23ed-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c23ed-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c23ed-126">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="c23ed-126">-MaintenanceWindow</span></span>
<span data-ttu-id="c23ed-127">Specifica la quantità di tempo consentita per gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="c23ed-127">Specifies the amount of time window allowed for updates.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23ed-128">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="c23ed-128">-StartHourUtc</span></span>
<span data-ttu-id="c23ed-129">Specifica un'ora del giorno in cui inizia la programmazione.</span><span class="sxs-lookup"><span data-stu-id="c23ed-129">Specifies an hour of the day when the schedule starts.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23ed-130">CommonParameters</span></span>
<span data-ttu-id="c23ed-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23ed-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c23ed-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23ed-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c23ed-133">INPUTS</span></span>

### <span data-ttu-id="c23ed-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c23ed-134">System.String</span></span>

### <span data-ttu-id="c23ed-135">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c23ed-135">System.Int32</span></span>

### <span data-ttu-id="c23ed-136">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c23ed-136">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c23ed-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c23ed-137">OUTPUTS</span></span>

### <span data-ttu-id="c23ed-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="c23ed-138">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="c23ed-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="c23ed-139">NOTES</span></span>
* <span data-ttu-id="c23ed-140">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridis, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="c23ed-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="c23ed-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c23ed-141">RELATED LINKS</span></span>

[<span data-ttu-id="c23ed-142">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c23ed-142">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="c23ed-143">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c23ed-143">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="c23ed-144">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="c23ed-144">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


