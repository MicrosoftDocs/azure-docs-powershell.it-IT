---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 297966fe0ad59948fd321ec52cf066ad5caa3d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008654"
---
# <span data-ttu-id="3dbdc-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="3dbdc-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="3dbdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="3dbdc-103">Ottiene una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="3dbdc-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="3dbdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dbdc-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dbdc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3dbdc-105">DESCRIPTION</span></span>
<span data-ttu-id="3dbdc-106">Il cmdlet **Get-AzRedisCachePatchSchedule** ottiene una pianificazione delle patch per una cache in Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="3dbdc-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="3dbdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dbdc-107">EXAMPLES</span></span>

### <span data-ttu-id="3dbdc-108">Esempio 1: Ottenere la pianificazione delle patch</span><span class="sxs-lookup"><span data-stu-id="3dbdc-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="3dbdc-109">Questo comando recupera la pianificazione delle patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="3dbdc-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="3dbdc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dbdc-110">PARAMETERS</span></span>

### <span data-ttu-id="3dbdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dbdc-111">-DefaultProfile</span></span>
<span data-ttu-id="3dbdc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dbdc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dbdc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3dbdc-113">-Name</span></span>
<span data-ttu-id="3dbdc-114">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="3dbdc-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="3dbdc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dbdc-115">-ResourceGroupName</span></span>
<span data-ttu-id="3dbdc-116">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="3dbdc-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="3dbdc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dbdc-117">CommonParameters</span></span>
<span data-ttu-id="3dbdc-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dbdc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dbdc-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dbdc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dbdc-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="3dbdc-120">INPUTS</span></span>

### <span data-ttu-id="3dbdc-121">System.String</span><span class="sxs-lookup"><span data-stu-id="3dbdc-121">System.String</span></span>

## <span data-ttu-id="3dbdc-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dbdc-122">OUTPUTS</span></span>

### <span data-ttu-id="3dbdc-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="3dbdc-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="3dbdc-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="3dbdc-124">NOTES</span></span>
* <span data-ttu-id="3dbdc-125">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridisposizione, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="3dbdc-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="3dbdc-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dbdc-126">RELATED LINKS</span></span>

[<span data-ttu-id="3dbdc-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="3dbdc-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="3dbdc-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="3dbdc-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="3dbdc-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="3dbdc-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


