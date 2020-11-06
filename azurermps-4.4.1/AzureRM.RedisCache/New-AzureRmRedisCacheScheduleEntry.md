---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: ACB53C23-99E0-4A0A-A44E-0D3FDB12450B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheScheduleEntry.md
ms.openlocfilehash: 07bfc520cfabc33ed4f72f1d0d4c46c9104a5253
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510379"
---
# <span data-ttu-id="1e48b-101">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1e48b-101">New-AzureRmRedisCacheScheduleEntry</span></span>

## <span data-ttu-id="1e48b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e48b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e48b-103">Crea una voce di programmazione.</span><span class="sxs-lookup"><span data-stu-id="1e48b-103">Creates a schedule entry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e48b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e48b-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheScheduleEntry -DayOfWeek <String> -StartHourUtc <Int32> [-MaintenanceWindow <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e48b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e48b-105">DESCRIPTION</span></span>
<span data-ttu-id="1e48b-106">Il cmdlet **New-AzureRmRedisCacheScheduleEntry** crea un oggetto **PSScheduleEntry** .</span><span class="sxs-lookup"><span data-stu-id="1e48b-106">The **New-AzureRmRedisCacheScheduleEntry** cmdlet creates a **PSScheduleEntry** object.</span></span>
<span data-ttu-id="1e48b-107">I cmdlet di pianificazione della patch della cache di Azure Redis, ad esempio il cmdlet New-AzureRmRedisCachePatchSchedule, richiedono la pianificazione degli oggetti voce.</span><span class="sxs-lookup"><span data-stu-id="1e48b-107">Azure Redis Cache patch schedule cmdlets, such as the New-AzureRmRedisCachePatchSchedule cmdlet, require schedule entry objects.</span></span>

## <span data-ttu-id="1e48b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e48b-108">EXAMPLES</span></span>

### <span data-ttu-id="1e48b-109">Esempio 1: creare una voce di programmazione per i fine settimana</span><span class="sxs-lookup"><span data-stu-id="1e48b-109">Example 1: Create a schedule entry for weekends</span></span>
```
PS C:\>New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00"
```

<span data-ttu-id="1e48b-110">Questo comando crea un oggetto **PSScheduleEntry** che rappresenta una pianificazione di fine settimana con l'ora di inizio e la finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="1e48b-110">This command creates a **PSScheduleEntry** object that represents a weekend schedule that has the specified start time and window.</span></span>

## <span data-ttu-id="1e48b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e48b-111">PARAMETERS</span></span>

### <span data-ttu-id="1e48b-112">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="1e48b-112">-DayOfWeek</span></span>
<span data-ttu-id="1e48b-113">Specifica il giorno della settimana per la voce di programmazione.</span><span class="sxs-lookup"><span data-stu-id="1e48b-113">Specifies the day of the week for the schedule entry.</span></span>
<span data-ttu-id="1e48b-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e48b-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1e48b-115">Quotidiani</span><span class="sxs-lookup"><span data-stu-id="1e48b-115">Everyday</span></span> 
- <span data-ttu-id="1e48b-116">Weekend</span><span class="sxs-lookup"><span data-stu-id="1e48b-116">Weekend</span></span> 
- <span data-ttu-id="1e48b-117">Lunedì</span><span class="sxs-lookup"><span data-stu-id="1e48b-117">Monday</span></span> 
- <span data-ttu-id="1e48b-118">Martedì</span><span class="sxs-lookup"><span data-stu-id="1e48b-118">Tuesday</span></span> 
- <span data-ttu-id="1e48b-119">Mercoledì</span><span class="sxs-lookup"><span data-stu-id="1e48b-119">Wednesday</span></span> 
- <span data-ttu-id="1e48b-120">Giovedì</span><span class="sxs-lookup"><span data-stu-id="1e48b-120">Thursday</span></span> 
- <span data-ttu-id="1e48b-121">Venerdì</span><span class="sxs-lookup"><span data-stu-id="1e48b-121">Friday</span></span> 
- <span data-ttu-id="1e48b-122">Sabato</span><span class="sxs-lookup"><span data-stu-id="1e48b-122">Saturday</span></span> 
- <span data-ttu-id="1e48b-123">Domenica</span><span class="sxs-lookup"><span data-stu-id="1e48b-123">Sunday</span></span>

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

### <span data-ttu-id="1e48b-124">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="1e48b-124">-MaintenanceWindow</span></span>
<span data-ttu-id="1e48b-125">Specifica l'intervallo di tempo consentito per gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="1e48b-125">Specifies the amount of time window allowed for updates.</span></span>

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

### <span data-ttu-id="1e48b-126">-StartHourUtc</span><span class="sxs-lookup"><span data-stu-id="1e48b-126">-StartHourUtc</span></span>
<span data-ttu-id="1e48b-127">Specifica un'ora del giorno in cui viene avviata la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1e48b-127">Specifies an hour of the day when the schedule starts.</span></span>

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

### <span data-ttu-id="1e48b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e48b-128">-DefaultProfile</span></span>
<span data-ttu-id="1e48b-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e48b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e48b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e48b-130">CommonParameters</span></span>
<span data-ttu-id="1e48b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e48b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e48b-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e48b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e48b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e48b-133">INPUTS</span></span>

### <span data-ttu-id="1e48b-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1e48b-134">None</span></span>
<span data-ttu-id="1e48b-135">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="1e48b-135">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="1e48b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e48b-136">OUTPUTS</span></span>

### <span data-ttu-id="1e48b-137">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1e48b-137">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="1e48b-138">Questo cmdlet restituisce un oggetto voce pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1e48b-138">This cmdlet returns a schedule entry object.</span></span>

## <span data-ttu-id="1e48b-139">Note</span><span class="sxs-lookup"><span data-stu-id="1e48b-139">NOTES</span></span>
* <span data-ttu-id="1e48b-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="1e48b-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1e48b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e48b-141">RELATED LINKS</span></span>

[<span data-ttu-id="1e48b-142">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1e48b-142">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1e48b-143">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1e48b-143">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1e48b-144">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1e48b-144">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


