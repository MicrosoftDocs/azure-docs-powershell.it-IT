---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 9921cc32530c712f3a1ca69d81b07fa8117ba80a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519709"
---
# <span data-ttu-id="203d3-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="203d3-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="203d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="203d3-102">SYNOPSIS</span></span>
<span data-ttu-id="203d3-103">Aggiunge una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="203d3-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="203d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="203d3-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="203d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="203d3-105">DESCRIPTION</span></span>
<span data-ttu-id="203d3-106">Il cmdlet **New-AzureRmRedisCachePatchSchedule** aggiunge una pianificazione delle patch a una cache in Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="203d3-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="203d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="203d3-107">EXAMPLES</span></span>

### <span data-ttu-id="203d3-108">Esempio 1: creare e aggiungere una pianificazione delle patch in una cache</span><span class="sxs-lookup"><span data-stu-id="203d3-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="203d3-109">Questo comando aggiunge una pianificazione della patch alla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="203d3-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="203d3-110">Il parametro Entries accetta come valore un comando che usa **New-AzureRmRedisCacheScheduleEntry** per creare una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="203d3-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="203d3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="203d3-111">PARAMETERS</span></span>

### <span data-ttu-id="203d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203d3-112">-DefaultProfile</span></span>
<span data-ttu-id="203d3-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="203d3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="203d3-114">-Voci</span><span class="sxs-lookup"><span data-stu-id="203d3-114">-Entries</span></span>
<span data-ttu-id="203d3-115">Specifica una matrice di pianificazioni che questo cmdlet imposta su una cache.</span><span class="sxs-lookup"><span data-stu-id="203d3-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="203d3-116">Per ottenere un oggetto **PSScheduleEntry** , usa il cmdlet New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="203d3-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="203d3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="203d3-117">-Name</span></span>
<span data-ttu-id="203d3-118">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="203d3-118">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="203d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="203d3-120">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="203d3-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="203d3-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="203d3-121">-Confirm</span></span>
<span data-ttu-id="203d3-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="203d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="203d3-123">-WhatIf</span></span>
<span data-ttu-id="203d3-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="203d3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="203d3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="203d3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203d3-126">CommonParameters</span></span>
<span data-ttu-id="203d3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203d3-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203d3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203d3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="203d3-129">INPUTS</span></span>

### <span data-ttu-id="203d3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="203d3-130">System.String</span></span>

### <span data-ttu-id="203d3-131">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry []</span><span class="sxs-lookup"><span data-stu-id="203d3-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="203d3-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="203d3-132">OUTPUTS</span></span>

### <span data-ttu-id="203d3-133">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="203d3-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="203d3-134">Note</span><span class="sxs-lookup"><span data-stu-id="203d3-134">NOTES</span></span>
* <span data-ttu-id="203d3-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="203d3-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="203d3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="203d3-136">RELATED LINKS</span></span>

[<span data-ttu-id="203d3-137">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="203d3-137">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="203d3-138">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="203d3-138">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="203d3-139">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="203d3-139">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


