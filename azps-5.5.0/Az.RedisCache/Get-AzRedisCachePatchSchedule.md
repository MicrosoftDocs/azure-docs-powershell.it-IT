---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178935"
---
# <span data-ttu-id="b001f-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b001f-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="b001f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b001f-102">SYNOPSIS</span></span>
<span data-ttu-id="b001f-103">Ottiene una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="b001f-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="b001f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b001f-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b001f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b001f-105">DESCRIPTION</span></span>
<span data-ttu-id="b001f-106">Il cmdlet **Get-AzRedisCachePatchSchedule** ottiene una pianificazione delle patch per una cache in Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="b001f-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="b001f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b001f-107">EXAMPLES</span></span>

### <span data-ttu-id="b001f-108">Esempio 1: Ottenere la pianificazione delle patch</span><span class="sxs-lookup"><span data-stu-id="b001f-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="b001f-109">Questo comando recupera la pianificazione delle patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="b001f-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="b001f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b001f-110">PARAMETERS</span></span>

### <span data-ttu-id="b001f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b001f-111">-DefaultProfile</span></span>
<span data-ttu-id="b001f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b001f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b001f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b001f-113">-Name</span></span>
<span data-ttu-id="b001f-114">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="b001f-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="b001f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b001f-115">-ResourceGroupName</span></span>
<span data-ttu-id="b001f-116">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="b001f-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="b001f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b001f-117">CommonParameters</span></span>
<span data-ttu-id="b001f-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b001f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b001f-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b001f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b001f-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="b001f-120">INPUTS</span></span>

### <span data-ttu-id="b001f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b001f-121">System.String</span></span>

## <span data-ttu-id="b001f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b001f-122">OUTPUTS</span></span>

### <span data-ttu-id="b001f-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b001f-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="b001f-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="b001f-124">NOTES</span></span>
* <span data-ttu-id="b001f-125">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, ridis, cache, Web, webapp, sito Web</span><span class="sxs-lookup"><span data-stu-id="b001f-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b001f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b001f-126">RELATED LINKS</span></span>

[<span data-ttu-id="b001f-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b001f-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="b001f-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="b001f-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="b001f-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="b001f-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


