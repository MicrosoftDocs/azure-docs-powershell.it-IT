---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: b966f15cc42ffc61f7d88cd5a1855f31564742ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980205"
---
# <span data-ttu-id="3e1d8-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="3e1d8-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="3e1d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1d8-103">Recuperare gli eventi del log attività.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="3e1d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e1d8-104">SYNTAX</span></span>

### <span data-ttu-id="3e1d8-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="3e1d8-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e1d8-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e1d8-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e1d8-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3e1d8-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e1d8-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3e1d8-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e1d8-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="3e1d8-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e1d8-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e1d8-110">DESCRIPTION</span></span>
<span data-ttu-id="3e1d8-111">Il cmdlet Get-AzActivityLog recuperare gli eventi del log attività.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="3e1d8-112">Gli eventi possono essere associati all'ID della sottoscrizione corrente, all'ID di correlazione, al gruppo di risorse, all'ID risorsa o al provider di risorse corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="3e1d8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e1d8-113">EXAMPLES</span></span>

### <span data-ttu-id="3e1d8-114">Esempio 1: Ottenere un log eventi in base all'ID sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="3e1d8-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzActivityLog
```

<span data-ttu-id="3e1d8-115">Questo comando elenca al massimo 1000 eventi associati all'ID sottoscrizione dell'utente, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-116">Esempio 2: Ottenere un log eventi in base all'ID sottoscrizione con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="3e1d8-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="3e1d8-117">Questo comando elenca al massimo 100 eventi associati all'ID sottoscrizione dell'utente, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-118">Esempio 3: Ottenere un log eventi in base all'ID abbonamento con un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="3e1d8-119">Questo comando elenca al massimo 1000 eventi associati all'ID abbonamento dell'utente che hanno avuto luogo il 06-06-01T10:30 ora locale se tale data/ora non è a partire da 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-120">Esempio 4: Ottenere un log eventi in base all'ID abbonamento con un'ora di inizio e un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="3e1d8-121">Questo comando elenca al massimo 1000 degli eventi associati all'ID abbonamento dell'utente che hanno avuto luogo il 04-04-04-01T10:30 ora locale e prima dell'ora locale 2017-04-14T11:30 se l'intero intervallo di data/ora non è a partire da 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="3e1d8-122">Esempio 5: Ottenere un log eventi in base all'ID di correlazione</span><span class="sxs-lookup"><span data-stu-id="3e1d8-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="3e1d8-123">Questo comando elenca al massimo 1000 eventi associati all'ID di correlazione specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="3e1d8-124">**NOTA:** in genere si tratta di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-124">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="3e1d8-125">Esempio 6: Ottenere un log eventi per ID di correlazione con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="3e1d8-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="3e1d8-126">Questo comando elenca al massimo 100 eventi associati all'ID di correlazione specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="3e1d8-127">**NOTA:** in genere si tratta di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-127">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="3e1d8-128">Esempio 7: Ottenere un log eventi in base all'ID di correlazione e all'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="3e1d8-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="3e1d8-129">Questo comando elenca al massimo 1000 eventi associati all'ID di correlazione specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è a partire da 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="3e1d8-130">**NOTA:** in genere si tratta di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-130">**NOTE**: this is usually only one event.</span></span>

### <span data-ttu-id="3e1d8-131">Esempio 8: Ottenere un log eventi per ID di correlazione con ora di inizio e ora di fine</span><span class="sxs-lookup"><span data-stu-id="3e1d8-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="3e1d8-132">Questo comando elenca al massimo 1000 eventi associati all'ID di correlazione specificato che hanno avuto luogo il 04-04-15T04:30 ora locale prima dell'ora locale 2017-04-25T12:30 se l'intero intervallo di data/ora non è a partire dalla data/ora corrente, ad esempio il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="3e1d8-133">Esempio 9: Ottenere un log eventi per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3e1d8-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="3e1d8-134">Questo comando elenca al massimo 1000 gli eventi associati al gruppo di risorse specificato che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-135">Esempio 10: Ottenere un log eventi per un gruppo di risorse con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="3e1d8-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="3e1d8-136">Questo comando elenca al massimo 100 eventi associati al gruppo di risorse specificato che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-137">Esempio 11: Ottenere un log eventi per un gruppo di risorse in base all'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="3e1d8-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="3e1d8-138">Questo comando elenca al massimo 1000 eventi associati al gruppo di risorse specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è precedente a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-139">Esempio 12: Ottenere un log eventi per un gruppo di risorse con un'ora di inizio e un'ora di fine</span><span class="sxs-lookup"><span data-stu-id="3e1d8-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="3e1d8-140">Questo comando elenca al massimo 1000 eventi associati al gruppo di risorse specificato che hanno avuto luogo il 04-04-15T04:30 ora locale 2017-04-25T12:30 se l'intero intervallo di data/ora non è a partire da 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="3e1d8-141">Esempio 13: Ottenere un log eventi in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="3e1d8-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="3e1d8-142">Questo comando elenca al massimo 1000 eventi associati all'ID risorsa specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-143">Esempio 14: Ottenere un log eventi in base all'ID risorsa con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="3e1d8-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="3e1d8-144">Questo comando elenca al massimo 100 eventi associati all'ID risorsa specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-145">Esempio 15: Ottenere un log eventi in base all'ID risorsa con un'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="3e1d8-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="3e1d8-146">Questo comando elenca al massimo 1000 eventi associati all'ID risorsa specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è a partire da 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-147">Esempio 16: Ottenere un log eventi in base all'ID risorsa con un'ora di inizio e un'ora di fine</span><span class="sxs-lookup"><span data-stu-id="3e1d8-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="3e1d8-148">Questo comando elenca al massimo 1000 eventi associati all'ID risorsa specificato che hanno avuto luogo il 04-04-15T04:30 ora locale prima dell'ora locale 2017-04-25T12:30 se l'intero intervallo di data/ora non è precedente a 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="3e1d8-149">Esempio 17: Ottenere un log eventi in base al provider di risorse</span><span class="sxs-lookup"><span data-stu-id="3e1d8-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="3e1d8-150">Questo comando elenca al massimo 1000 eventi associati al provider di risorse specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-151">Esempio 18: Ottenere un log eventi per provider di risorse con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="3e1d8-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="3e1d8-152">Questo comando elenca al massimo 100 eventi associati al provider di risorse specificato, che hanno avuto luogo 7 giorni a partire dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-153">Esempio 19: Ottenere un log eventi per provider di risorse con un'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="3e1d8-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="3e1d8-154">Questo comando elenca al massimo 1000 eventi associati al provider di risorse specificato che hanno avuto luogo il 05-05-22T04:30:00 ora locale se l'ora di inizio non è precedente a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="3e1d8-155">Esempio 20: Ottenere un log eventi per provider di risorse con un'ora di inizio e un'ora di fine</span><span class="sxs-lookup"><span data-stu-id="3e1d8-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="3e1d8-156">Questo comando elenca al massimo 1000 eventi associati al provider di risorse specificato che hanno avuto luogo il 04-04-15T04:30 ora locale prima del 04-04-25T12:30 locale 2017-15T04:30, se l'intero intervallo di data/ora non è precedente a 90 giorni dalla data/ora corrente, ad esempio il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="3e1d8-157">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e1d8-157">PARAMETERS</span></span>

### <span data-ttu-id="3e1d8-158">-Caller</span><span class="sxs-lookup"><span data-stu-id="3e1d8-158">-Caller</span></span>
<span data-ttu-id="3e1d8-159">Il chiamante degli eventi da recuperare</span><span class="sxs-lookup"><span data-stu-id="3e1d8-159">The caller of the events to fetch</span></span>

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

### <span data-ttu-id="3e1d8-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="3e1d8-160">-CorrelationId</span></span>
<span data-ttu-id="3e1d8-161">Id correlazione</span><span class="sxs-lookup"><span data-stu-id="3e1d8-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1d8-162">-DefaultProfile</span></span>
<span data-ttu-id="3e1d8-163">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e1d8-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="3e1d8-164">-DetailedOutput</span></span>
<span data-ttu-id="3e1d8-165">Restituire l'oggetto con tutti i dettagli degli eventi (per impostazione predefinita vengono restituiti solo alcuni attributi, ad esempio nessun dettaglio)</span><span class="sxs-lookup"><span data-stu-id="3e1d8-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-166">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3e1d8-166">-EndTime</span></span>
<span data-ttu-id="3e1d8-167">EndTime della query</span><span class="sxs-lookup"><span data-stu-id="3e1d8-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="3e1d8-168">-MaxRecord</span></span>
<span data-ttu-id="3e1d8-169">Numero massimo di record da recuperare.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="3e1d8-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="3e1d8-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1d8-171">-ResourceGroupName</span></span>
<span data-ttu-id="3e1d8-172">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3e1d8-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e1d8-173">-ResourceId</span></span>
<span data-ttu-id="3e1d8-174">L'ID Risorsa</span><span class="sxs-lookup"><span data-stu-id="3e1d8-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3e1d8-175">-ResourceProvider</span></span>
<span data-ttu-id="3e1d8-176">Nome ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="3e1d8-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3e1d8-177">-StartTime</span></span>
<span data-ttu-id="3e1d8-178">Id di correlazione della query</span><span class="sxs-lookup"><span data-stu-id="3e1d8-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1d8-179">-Stato</span><span class="sxs-lookup"><span data-stu-id="3e1d8-179">-Status</span></span>
<span data-ttu-id="3e1d8-180">Stato degli eventi da recuperare</span><span class="sxs-lookup"><span data-stu-id="3e1d8-180">The status of the events to fetch</span></span>

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

### <span data-ttu-id="3e1d8-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1d8-181">CommonParameters</span></span>
<span data-ttu-id="3e1d8-182">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1d8-183">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e1d8-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1d8-184">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e1d8-184">INPUTS</span></span>

### <span data-ttu-id="3e1d8-185">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3e1d8-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3e1d8-186">System.String</span><span class="sxs-lookup"><span data-stu-id="3e1d8-186">System.String</span></span>

### <span data-ttu-id="3e1d8-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e1d8-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3e1d8-188">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3e1d8-188">System.Int32</span></span>

## <span data-ttu-id="3e1d8-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e1d8-189">OUTPUTS</span></span>

### <span data-ttu-id="3e1d8-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="3e1d8-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="3e1d8-191">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e1d8-191">NOTES</span></span>

## <span data-ttu-id="3e1d8-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e1d8-192">RELATED LINKS</span></span>
