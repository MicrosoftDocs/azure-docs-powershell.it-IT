---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: c486e7d33593e779a59efa6c4360fe660eac4015
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520092"
---
# <span data-ttu-id="da1c8-101">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="da1c8-101">Get-AzureRmLog</span></span>

## <span data-ttu-id="da1c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da1c8-102">SYNOPSIS</span></span>
<span data-ttu-id="da1c8-103">Ottiene un log di eventi.</span><span class="sxs-lookup"><span data-stu-id="da1c8-103">Gets a log of events.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da1c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da1c8-104">SYNTAX</span></span>

### <span data-ttu-id="da1c8-105">Query su CorrelationId</span><span class="sxs-lookup"><span data-stu-id="da1c8-105">Query on CorrelationId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da1c8-106">Query in ResourceIdName</span><span class="sxs-lookup"><span data-stu-id="da1c8-106">Query on ResourceIdName</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da1c8-107">Query in ResourceGroupProvider</span><span class="sxs-lookup"><span data-stu-id="da1c8-107">Query on ResourceGroupProvider</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroup] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da1c8-108">Query in ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="da1c8-108">Query on ResourceProvider</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da1c8-109">Query a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="da1c8-109">Query at subscription level</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxEvents <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da1c8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da1c8-110">DESCRIPTION</span></span>
<span data-ttu-id="da1c8-111">Il cmdlet **Get-AzureRmLog** ottiene un log di eventi.</span><span class="sxs-lookup"><span data-stu-id="da1c8-111">The **Get-AzureRmLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="da1c8-112">Gli eventi possono essere associati all'ID corrente dell'abbonamento, all'ID di correlazione, al gruppo di risorse, all'ID risorsa o al provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="da1c8-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="da1c8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da1c8-113">EXAMPLES</span></span>

### <span data-ttu-id="da1c8-114">Esempio 1: ottenere un log eventi in base all'ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="da1c8-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzureRmLog
```

<span data-ttu-id="da1c8-115">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID abbonamento dell'utente che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-116">Esempio 2: ottenere un log eventi in base all'ID abbonamento con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="da1c8-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

<span data-ttu-id="da1c8-117">Questo comando elenca la maggior parte degli eventi di 100 associati all'ID abbonamento dell'utente che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-118">Esempio 3: ottenere un log eventi in base all'ID abbonamento con l'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="da1c8-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="da1c8-119">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID abbonamento dell'utente che ha avuto luogo dopo il 2017-06-01T10:30 ora locale, se tale data/ora non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-120">Esempio 4: ottenere un log eventi in base all'ID abbonamento con l'ora di inizio e l'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="da1c8-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="da1c8-121">Questo comando elenca al massimo 1000 degli eventi associati all'ID abbonamento dell'utente che ha avuto luogo dopo il 2017-04-01T10:30 local time e before 2017-04-14T11:30 local time se l'intero intervallo di data/ora non supera i 90 giorni dalla data/ora corrente, ossia: il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="da1c8-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="da1c8-122">Esempio 5: ottenere un log eventi tramite un ID di correlazione</span><span class="sxs-lookup"><span data-stu-id="da1c8-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="da1c8-123">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="da1c8-124">**Nota** : si tratta in genere di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="da1c8-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="da1c8-125">Esempio 6: ottenere un log eventi tramite un ID di correlazione con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="da1c8-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="da1c8-126">Questo comando elenca la maggior parte degli eventi di 100 associati all'ID di correlazione specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="da1c8-127">**Nota** : si tratta in genere di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="da1c8-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="da1c8-128">Esempio 7: ottenere un log eventi dall'ID di correlazione e dall'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="da1c8-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="da1c8-129">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="da1c8-130">**Nota** : si tratta in genere di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="da1c8-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="da1c8-131">Esempio 8: ottenere un log eventi in base all'ID di correlazione con ora di inizio e ora di fine</span><span class="sxs-lookup"><span data-stu-id="da1c8-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="da1c8-132">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è più vecchio di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="da1c8-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="da1c8-133">Esempio 9: ottenere un log eventi per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="da1c8-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS"
```

<span data-ttu-id="da1c8-134">Questo comando elenca al massimo 1000 gli eventi associati al gruppo di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-135">Esempio 10: ottenere un log eventi per un gruppo di risorse con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="da1c8-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="da1c8-136">Questo comando elenca la maggior parte degli eventi di 100 associati al gruppo di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-137">Esempio 11: ottenere un log eventi per un gruppo di risorse per ora di inizio</span><span class="sxs-lookup"><span data-stu-id="da1c8-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="da1c8-138">Questo comando elenca al massimo 1000 Evetns associato al gruppo di risorse specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-139">Esempio 12: ottenere un log eventi per un gruppo di risorse con ora di inizio e ora di fine</span><span class="sxs-lookup"><span data-stu-id="da1c8-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="da1c8-140">Questo comando elenca la maggior parte degli eventi di 1000 associati al gruppo di risorse specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è superiore a 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="da1c8-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="da1c8-141">Esempio 13: ottenere un log eventi in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="da1c8-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="da1c8-142">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-143">Esempio 14: ottenere un log eventi in base all'ID risorsa con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="da1c8-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="da1c8-144">Questo comando elenca la maggior parte degli eventi di 100 associati all'ID risorsa specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-145">Esempio 15: ottenere un log eventi in base all'ID risorsa con un'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="da1c8-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="da1c8-146">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-147">Esempio 16: ottenere un log eventi in base all'ID risorsa con l'ora di inizio e di fine</span><span class="sxs-lookup"><span data-stu-id="da1c8-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="da1c8-148">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è maggiore di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="da1c8-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="da1c8-149">Esempio 17: ottenere un log eventi in base al provider di risorse</span><span class="sxs-lookup"><span data-stu-id="da1c8-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="da1c8-150">Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-151">Esempio 18: ottenere un log eventi in base al provider di risorse con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="da1c8-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="da1c8-152">Questo comando elenca la maggior parte degli eventi di 100 associati al provider di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-153">Esempio 19: ottenere un log eventi in base al provider di risorse con un orario di inizio</span><span class="sxs-lookup"><span data-stu-id="da1c8-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="da1c8-154">Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="da1c8-155">Esempio 20: ottenere un log eventi in base al provider di risorse con l'ora di inizio e di fine</span><span class="sxs-lookup"><span data-stu-id="da1c8-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="da1c8-156">Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è maggiore di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="da1c8-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="da1c8-157">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da1c8-157">PARAMETERS</span></span>

### <span data-ttu-id="da1c8-158">-Chiamante</span><span class="sxs-lookup"><span data-stu-id="da1c8-158">-Caller</span></span>
<span data-ttu-id="da1c8-159">Specifica un chiamante.</span><span class="sxs-lookup"><span data-stu-id="da1c8-159">Specifies a caller.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="da1c8-160">-CorrelationId</span></span>
<span data-ttu-id="da1c8-161">Specifica l'ID di correlazione.</span><span class="sxs-lookup"><span data-stu-id="da1c8-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="da1c8-162">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="da1c8-162">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: Query on CorrelationId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-163">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="da1c8-163">-DetailedOutput</span></span>
<span data-ttu-id="da1c8-164">Indica che questo cmdlet Visualizza l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="da1c8-164">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="da1c8-165">Per impostazione predefinita, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="da1c8-165">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="da1c8-166">-EndTime</span></span>
<span data-ttu-id="da1c8-167">Specifica l'ora di fine della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="da1c8-167">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="da1c8-168">Il valore predefinito è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="da1c8-168">The default value is the current time.</span></span>
<span data-ttu-id="da1c8-169">Il valore deve essere successivo a *StartTime*.</span><span class="sxs-lookup"><span data-stu-id="da1c8-169">The value must be later than *StartTime*.</span></span>

<span data-ttu-id="da1c8-170">Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="da1c8-170">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-171">-MaxEvents</span><span class="sxs-lookup"><span data-stu-id="da1c8-171">-MaxEvents</span></span>
<span data-ttu-id="da1c8-172">Specifica il numero totale di record da recuperare per il filtro specificato.</span><span class="sxs-lookup"><span data-stu-id="da1c8-172">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="da1c8-173">Il valore predefinito è 1000 e il valore massimo accettato è 100000.</span><span class="sxs-lookup"><span data-stu-id="da1c8-173">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="da1c8-174">I valori negativi e 0 vengono ignorati e viene usato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="da1c8-174">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxRecords

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-175">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="da1c8-175">-ResourceGroup</span></span>
<span data-ttu-id="da1c8-176">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da1c8-176">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Query on ResourceGroupProvider
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-177">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da1c8-177">-ResourceId</span></span>
<span data-ttu-id="da1c8-178">Specifica l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="da1c8-178">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Query on ResourceIdName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-179">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="da1c8-179">-ResourceProvider</span></span>
<span data-ttu-id="da1c8-180">Specifica un filtro in base al provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="da1c8-180">Specifies a filter by resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Query on ResourceProvider
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-181">-StartTime</span><span class="sxs-lookup"><span data-stu-id="da1c8-181">-StartTime</span></span>
<span data-ttu-id="da1c8-182">Specifica l'ora di inizio della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="da1c8-182">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="da1c8-183">Il valore predefinito è *EndTime* meno sette giorni.</span><span class="sxs-lookup"><span data-stu-id="da1c8-183">The default value is *EndTime* minus seven days.</span></span>

<span data-ttu-id="da1c8-184">Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="da1c8-184">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-185">-Stato</span><span class="sxs-lookup"><span data-stu-id="da1c8-185">-Status</span></span>
<span data-ttu-id="da1c8-186">Specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="da1c8-186">Specifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da1c8-187">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1c8-187">-DefaultProfile</span></span>
<span data-ttu-id="da1c8-188">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da1c8-188">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da1c8-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1c8-189">CommonParameters</span></span>
<span data-ttu-id="da1c8-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da1c8-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1c8-191">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da1c8-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1c8-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da1c8-192">INPUTS</span></span>

### <span data-ttu-id="da1c8-193">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da1c8-193">None</span></span>

## <span data-ttu-id="da1c8-194">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da1c8-194">OUTPUTS</span></span>

### <span data-ttu-id="da1c8-195">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da1c8-195">None</span></span>

## <span data-ttu-id="da1c8-196">Note</span><span class="sxs-lookup"><span data-stu-id="da1c8-196">NOTES</span></span>

## <span data-ttu-id="da1c8-197">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da1c8-197">RELATED LINKS</span></span>

