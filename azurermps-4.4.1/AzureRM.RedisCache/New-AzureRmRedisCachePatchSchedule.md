---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685880"
---
# <span data-ttu-id="d774c-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d774c-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="d774c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d774c-102">SYNOPSIS</span></span>
<span data-ttu-id="d774c-103">Aggiunge una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="d774c-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d774c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d774c-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d774c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d774c-105">DESCRIPTION</span></span>
<span data-ttu-id="d774c-106">Il cmdlet **New-AzureRmRedisCachePatchSchedule** aggiunge una pianificazione delle patch a una cache in Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="d774c-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="d774c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d774c-107">EXAMPLES</span></span>

### <span data-ttu-id="d774c-108">Esempio 1: creare e aggiungere una pianificazione delle patch in una cache</span><span class="sxs-lookup"><span data-stu-id="d774c-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="d774c-109">Questo comando aggiunge una pianificazione della patch alla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="d774c-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="d774c-110">Il parametro Entries accetta come valore un comando che usa **New-AzureRmRedisCacheScheduleEntry** per creare una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d774c-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="d774c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d774c-111">PARAMETERS</span></span>

### <span data-ttu-id="d774c-112">-Voci</span><span class="sxs-lookup"><span data-stu-id="d774c-112">-Entries</span></span>
<span data-ttu-id="d774c-113">Specifica una matrice di pianificazioni che questo cmdlet imposta su una cache.</span><span class="sxs-lookup"><span data-stu-id="d774c-113">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="d774c-114">Per ottenere un oggetto **PSScheduleEntry** , usa il cmdlet New-AzureRmRedisCacheScheduleEntry.</span><span class="sxs-lookup"><span data-stu-id="d774c-114">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="d774c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d774c-115">-Name</span></span>
<span data-ttu-id="d774c-116">Specifica il nome della cache.</span><span class="sxs-lookup"><span data-stu-id="d774c-116">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="d774c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d774c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d774c-118">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="d774c-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="d774c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d774c-119">-DefaultProfile</span></span>
<span data-ttu-id="d774c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d774c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d774c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d774c-121">CommonParameters</span></span>
<span data-ttu-id="d774c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d774c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d774c-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d774c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d774c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d774c-124">INPUTS</span></span>

### <span data-ttu-id="d774c-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d774c-125">None</span></span>
<span data-ttu-id="d774c-126">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="d774c-126">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d774c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d774c-127">OUTPUTS</span></span>

### <span data-ttu-id="d774c-128">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d774c-128">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="d774c-129">Questo cmdlet restituisce le voci della pianificazione delle patch impostate nella cache.</span><span class="sxs-lookup"><span data-stu-id="d774c-129">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="d774c-130">Note</span><span class="sxs-lookup"><span data-stu-id="d774c-130">NOTES</span></span>
* <span data-ttu-id="d774c-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="d774c-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d774c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d774c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d774c-133">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d774c-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="d774c-134">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="d774c-134">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="d774c-135">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="d774c-135">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


