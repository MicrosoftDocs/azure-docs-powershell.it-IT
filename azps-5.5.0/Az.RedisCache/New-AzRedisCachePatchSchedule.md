---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 4215cf8450922a03f061abcc04022ee4e20950b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206131"
---
# <span data-ttu-id="f4eb1-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f4eb1-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="f4eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="f4eb1-103">Aggiunge una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="f4eb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4eb1-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4eb1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="f4eb1-106">Il cmdlet **New-AzRedisCachePatchSchedule aggiunge** una pianificazione delle patch a una cache in Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="f4eb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="f4eb1-108">Esempio 1: Creare e aggiungere una pianificazione delle patch in una cache</span><span class="sxs-lookup"><span data-stu-id="f4eb1-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="f4eb1-109">Questo comando aggiunge una pianificazione delle patch alla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="f4eb1-110">Il parametro Entries accetta come valore un comando che usa **New-AzRedisCacheScheduleEntry** per creare una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="f4eb1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4eb1-111">PARAMETERS</span></span>

### <span data-ttu-id="f4eb1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4eb1-112">-DefaultProfile</span></span>
<span data-ttu-id="f4eb1-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4eb1-114">-Voci</span><span class="sxs-lookup"><span data-stu-id="f4eb1-114">-Entries</span></span>
<span data-ttu-id="f4eb1-115">Specifica una matrice di pianificazioni che questo cmdlet imposta in una cache.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="f4eb1-116">Per ottenere un **oggetto PSScheduleEntry,** usare il cmdlet New-AzRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="f4eb1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f4eb1-117">-Name</span></span>
<span data-ttu-id="f4eb1-118">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="f4eb1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4eb1-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4eb1-120">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="f4eb1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4eb1-121">-Confirm</span></span>
<span data-ttu-id="f4eb1-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4eb1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4eb1-123">-WhatIf</span></span>
<span data-ttu-id="f4eb1-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4eb1-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4eb1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4eb1-126">CommonParameters</span></span>
<span data-ttu-id="f4eb1-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4eb1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4eb1-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4eb1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4eb1-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4eb1-129">INPUTS</span></span>

### <span data-ttu-id="f4eb1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f4eb1-130">System.String</span></span>

### <span data-ttu-id="f4eb1-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="f4eb1-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="f4eb1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4eb1-132">OUTPUTS</span></span>

### <span data-ttu-id="f4eb1-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f4eb1-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="f4eb1-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4eb1-134">NOTES</span></span>
* <span data-ttu-id="f4eb1-135">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridis, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="f4eb1-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f4eb1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4eb1-136">RELATED LINKS</span></span>

[<span data-ttu-id="f4eb1-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f4eb1-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="f4eb1-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f4eb1-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="f4eb1-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f4eb1-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


