---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: 6a217be0122a94aec7b247fbc7e8835155805ffe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835083"
---
# <span data-ttu-id="94be6-101">Get-AzLog</span><span class="sxs-lookup"><span data-stu-id="94be6-101">Get-AzLog</span></span>

## <span data-ttu-id="94be6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94be6-102">SYNOPSIS</span></span>
<span data-ttu-id="94be6-103">Ottiene un log di eventi.</span><span class="sxs-lookup"><span data-stu-id="94be6-103">Gets a log of events.</span></span>

## <span data-ttu-id="94be6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94be6-104">SYNTAX</span></span>

### <span data-ttu-id="94be6-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="94be6-105">GetByCorrelationId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94be6-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="94be6-106">GetByResourceId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94be6-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94be6-107">GetByResourceGroup</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94be6-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="94be6-108">GetByResourceProvider</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="94be6-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="94be6-109">GetBySubscription</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94be6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94be6-110">DESCRIPTION</span></span>
<span data-ttu-id="94be6-111">Il cmdlet **Get-AzLog** ottiene un log di eventi.</span><span class="sxs-lookup"><span data-stu-id="94be6-111">The **Get-AzLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="94be6-112">Gli eventi possono essere associati all'ID corrente dell'abbonamento, all'ID di correlazione, al gruppo di risorse, all'ID risorsa o al provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="94be6-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="94be6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94be6-113">EXAMPLES</span></span>

### <span data-ttu-id="94be6-114">Esempio 1: ottenere un log eventi in base all'ID abbonamento</span><span class="sxs-lookup"><span data-stu-id="94be6-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzLog
```

<span data-ttu-id="94be6-115">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID abbonamento dell'utente che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-116">Esempio 2: ottenere un log eventi in base all'ID abbonamento con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="94be6-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -MaxEvents 100
```

<span data-ttu-id="94be6-117">Questo comando elenca la maggior parte degli eventi di 100 associati all'ID abbonamento dell'utente che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-118">Esempio 3: ottenere un log eventi in base all'ID abbonamento con l'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="94be6-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="94be6-119">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID abbonamento dell'utente che ha avuto luogo dopo il 2017-06-01T10:30 ora locale, se tale data/ora non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-120">Esempio 4: ottenere un log eventi in base all'ID abbonamento con l'ora di inizio e l'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="94be6-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="94be6-121">Questo comando elenca al massimo 1000 degli eventi associati all'ID abbonamento dell'utente che ha avuto luogo dopo il 2017-04-01T10:30 local time e before 2017-04-14T11:30 local time se l'intero intervallo di data/ora non supera i 90 giorni dalla data/ora corrente, ossia: il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="94be6-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="94be6-122">Esempio 5: ottenere un log eventi tramite un ID di correlazione</span><span class="sxs-lookup"><span data-stu-id="94be6-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="94be6-123">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="94be6-124">**Nota** : si tratta in genere di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="94be6-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="94be6-125">Esempio 6: ottenere un log eventi tramite un ID di correlazione con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="94be6-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="94be6-126">Questo comando elenca la maggior parte degli eventi di 100 associati all'ID di correlazione specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="94be6-127">**Nota** : si tratta in genere di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="94be6-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="94be6-128">Esempio 7: ottenere un log eventi dall'ID di correlazione e dall'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="94be6-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="94be6-129">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="94be6-130">**Nota** : si tratta in genere di un solo evento.</span><span class="sxs-lookup"><span data-stu-id="94be6-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="94be6-131">Esempio 8: ottenere un log eventi in base all'ID di correlazione con ora di inizio e ora di fine</span><span class="sxs-lookup"><span data-stu-id="94be6-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="94be6-132">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID di correlazione specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è più vecchio di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="94be6-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="94be6-133">Esempio 9: ottenere un log eventi per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="94be6-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="94be6-134">Questo comando elenca al massimo 1000 gli eventi associati al gruppo di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-135">Esempio 10: ottenere un log eventi per un gruppo di risorse con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="94be6-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="94be6-136">Questo comando elenca la maggior parte degli eventi di 100 associati al gruppo di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-137">Esempio 11: ottenere un log eventi per un gruppo di risorse per ora di inizio</span><span class="sxs-lookup"><span data-stu-id="94be6-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="94be6-138">Questo comando elenca al massimo 1000 Evetns associato al gruppo di risorse specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-139">Esempio 12: ottenere un log eventi per un gruppo di risorse con ora di inizio e ora di fine</span><span class="sxs-lookup"><span data-stu-id="94be6-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="94be6-140">Questo comando elenca la maggior parte degli eventi di 1000 associati al gruppo di risorse specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è superiore a 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="94be6-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="94be6-141">Esempio 13: ottenere un log eventi in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="94be6-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="94be6-142">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-143">Esempio 14: ottenere un log eventi in base all'ID risorsa con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="94be6-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="94be6-144">Questo comando elenca la maggior parte degli eventi di 100 associati all'ID risorsa specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-145">Esempio 15: ottenere un log eventi in base all'ID risorsa con un'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="94be6-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="94be6-146">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-147">Esempio 16: ottenere un log eventi in base all'ID risorsa con l'ora di inizio e di fine</span><span class="sxs-lookup"><span data-stu-id="94be6-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="94be6-148">Questo comando elenca la maggior parte degli eventi di 1000 associati all'ID risorsa specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è maggiore di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="94be6-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="94be6-149">Esempio 17: ottenere un log eventi in base al provider di risorse</span><span class="sxs-lookup"><span data-stu-id="94be6-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="94be6-150">Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-151">Esempio 18: ottenere un log eventi in base al provider di risorse con un numero massimo di eventi</span><span class="sxs-lookup"><span data-stu-id="94be6-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="94be6-152">Questo comando elenca la maggior parte degli eventi di 100 associati al provider di risorse specificato che ha avuto luogo 7 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-153">Esempio 19: ottenere un log eventi in base al provider di risorse con un orario di inizio</span><span class="sxs-lookup"><span data-stu-id="94be6-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="94be6-154">Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo dopo il 2017-05-22T04:30:00 ora locale, se l'ora di inizio non è superiore a 90 giorni dalla data/ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="94be6-155">Esempio 20: ottenere un log eventi in base al provider di risorse con l'ora di inizio e di fine</span><span class="sxs-lookup"><span data-stu-id="94be6-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="94be6-156">Questo comando elenca la maggior parte degli eventi di 1000 associati al provider di risorse specificato che ha avuto luogo dopo il 2017-04-15T04:30 local time, ma prima del 2017-04-25T12:30 local time se l'intero intervallo di data/ora non è maggiore di 90 giorni dalla data/ora corrente, ovvero il periodo di conservazione.</span><span class="sxs-lookup"><span data-stu-id="94be6-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="94be6-157">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94be6-157">PARAMETERS</span></span>

### <span data-ttu-id="94be6-158">-Chiamante</span><span class="sxs-lookup"><span data-stu-id="94be6-158">-Caller</span></span>
<span data-ttu-id="94be6-159">Specifica un chiamante.</span><span class="sxs-lookup"><span data-stu-id="94be6-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="94be6-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="94be6-160">-CorrelationId</span></span>
<span data-ttu-id="94be6-161">Specifica l'ID di correlazione.</span><span class="sxs-lookup"><span data-stu-id="94be6-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="94be6-162">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="94be6-162">This parameter is required.</span></span>

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

### <span data-ttu-id="94be6-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94be6-163">-DefaultProfile</span></span>
<span data-ttu-id="94be6-164">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="94be6-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94be6-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="94be6-165">-DetailedOutput</span></span>
<span data-ttu-id="94be6-166">Indica che questo cmdlet Visualizza l'output dettagliato.</span><span class="sxs-lookup"><span data-stu-id="94be6-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="94be6-167">Per impostazione predefinita, l'output viene riepilogato.</span><span class="sxs-lookup"><span data-stu-id="94be6-167">By default, output is summarized.</span></span>

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

### <span data-ttu-id="94be6-168">-EndTime</span><span class="sxs-lookup"><span data-stu-id="94be6-168">-EndTime</span></span>
<span data-ttu-id="94be6-169">Specifica l'ora di fine della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="94be6-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="94be6-170">Il valore predefinito è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="94be6-170">The default value is the current time.</span></span>
<span data-ttu-id="94be6-171">Il valore deve essere successivo a *StartTime*.</span><span class="sxs-lookup"><span data-stu-id="94be6-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="94be6-172">Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="94be6-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

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

### <span data-ttu-id="94be6-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="94be6-173">-MaxRecord</span></span>
<span data-ttu-id="94be6-174">Specifica il numero totale di record da recuperare per il filtro specificato.</span><span class="sxs-lookup"><span data-stu-id="94be6-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="94be6-175">Il valore predefinito è 1000 e il valore massimo accettato è 100000.</span><span class="sxs-lookup"><span data-stu-id="94be6-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="94be6-176">I valori negativi e 0 vengono ignorati e viene usato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="94be6-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94be6-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94be6-177">-ResourceGroupName</span></span>
<span data-ttu-id="94be6-178">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94be6-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="94be6-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94be6-179">-ResourceId</span></span>
<span data-ttu-id="94be6-180">Specifica l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="94be6-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="94be6-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="94be6-181">-ResourceProvider</span></span>
<span data-ttu-id="94be6-182">Specifica un filtro in base al provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="94be6-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="94be6-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="94be6-183">-StartTime</span></span>
<span data-ttu-id="94be6-184">Specifica l'ora di inizio della query in ora locale.</span><span class="sxs-lookup"><span data-stu-id="94be6-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="94be6-185">Il valore predefinito è *EndTime* meno sette giorni.</span><span class="sxs-lookup"><span data-stu-id="94be6-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="94be6-186">Puoi usare il cmdlet Get-Date per ottenere un oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="94be6-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

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

### <span data-ttu-id="94be6-187">-Stato</span><span class="sxs-lookup"><span data-stu-id="94be6-187">-Status</span></span>
<span data-ttu-id="94be6-188">Specifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="94be6-188">Specifies the status.</span></span>

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

### <span data-ttu-id="94be6-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94be6-189">CommonParameters</span></span>
<span data-ttu-id="94be6-190">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94be6-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94be6-191">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94be6-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94be6-192">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94be6-192">INPUTS</span></span>

### <span data-ttu-id="94be6-193">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="94be6-193">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="94be6-194">System. String</span><span class="sxs-lookup"><span data-stu-id="94be6-194">System.String</span></span>

### <span data-ttu-id="94be6-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94be6-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="94be6-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="94be6-196">System.Int32</span></span>

## <span data-ttu-id="94be6-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94be6-197">OUTPUTS</span></span>

### <span data-ttu-id="94be6-198">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="94be6-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="94be6-199">Note</span><span class="sxs-lookup"><span data-stu-id="94be6-199">NOTES</span></span>

## <span data-ttu-id="94be6-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94be6-200">RELATED LINKS</span></span>
