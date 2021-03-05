---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: ebc51005bcffdde2ad5f64764e90440e8d1e7583
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961725"
---
# <span data-ttu-id="6f67a-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6f67a-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="6f67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f67a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f67a-103">Aggiunge una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="6f67a-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="6f67a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f67a-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f67a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f67a-105">DESCRIPTION</span></span>
<span data-ttu-id="6f67a-106">Il cmdlet **New-AzRedisCachePatchSchedule aggiunge** una pianificazione delle patch a una cache in Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="6f67a-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="6f67a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f67a-107">EXAMPLES</span></span>

### <span data-ttu-id="6f67a-108">Esempio 1: Creare e aggiungere una pianificazione delle patch in una cache</span><span class="sxs-lookup"><span data-stu-id="6f67a-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="6f67a-109">Questo comando aggiunge una pianificazione delle patch alla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="6f67a-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="6f67a-110">Il parametro Entries accetta come valore un comando che usa **New-AzRedisCacheScheduleEntry** per creare una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="6f67a-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="6f67a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f67a-111">PARAMETERS</span></span>

### <span data-ttu-id="6f67a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f67a-112">-DefaultProfile</span></span>
<span data-ttu-id="6f67a-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f67a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f67a-114">-Voci</span><span class="sxs-lookup"><span data-stu-id="6f67a-114">-Entries</span></span>
<span data-ttu-id="6f67a-115">Specifica una matrice di pianificazioni che questo cmdlet imposta in una cache.</span><span class="sxs-lookup"><span data-stu-id="6f67a-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="6f67a-116">Per ottenere un **oggetto PSScheduleEntry,** usare il cmdlet New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="6f67a-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="6f67a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6f67a-117">-Name</span></span>
<span data-ttu-id="6f67a-118">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="6f67a-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="6f67a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f67a-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f67a-120">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="6f67a-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="6f67a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f67a-121">-Confirm</span></span>
<span data-ttu-id="6f67a-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f67a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f67a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f67a-123">-WhatIf</span></span>
<span data-ttu-id="6f67a-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f67a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f67a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f67a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f67a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f67a-126">CommonParameters</span></span>
<span data-ttu-id="6f67a-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f67a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f67a-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f67a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f67a-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f67a-129">INPUTS</span></span>

### <span data-ttu-id="6f67a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6f67a-130">System.String</span></span>

### <span data-ttu-id="6f67a-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="6f67a-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="6f67a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f67a-132">OUTPUTS</span></span>

### <span data-ttu-id="6f67a-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6f67a-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="6f67a-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f67a-134">NOTES</span></span>
* <span data-ttu-id="6f67a-135">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridis, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="6f67a-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6f67a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f67a-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f67a-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6f67a-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="6f67a-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6f67a-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="6f67a-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6f67a-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


