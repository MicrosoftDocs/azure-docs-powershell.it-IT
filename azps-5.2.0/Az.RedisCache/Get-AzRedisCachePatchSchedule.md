---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336472"
---
# <span data-ttu-id="60a95-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="60a95-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="60a95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60a95-102">SYNOPSIS</span></span>
<span data-ttu-id="60a95-103">Ottiene una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="60a95-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="60a95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60a95-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a95-105">DESCRIPTION</span></span>
<span data-ttu-id="60a95-106">Il cmdlet **Get-AzRedisCachePatchSchedule** ottiene una pianificazione delle patch per una cache in Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="60a95-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="60a95-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60a95-107">EXAMPLES</span></span>

### <span data-ttu-id="60a95-108">Esempio 1: ottenere la pianificazione della patch</span><span class="sxs-lookup"><span data-stu-id="60a95-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="60a95-109">Questo comando consente di ottenere la pianificazione della patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="60a95-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="60a95-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60a95-110">PARAMETERS</span></span>

### <span data-ttu-id="60a95-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a95-111">-DefaultProfile</span></span>
<span data-ttu-id="60a95-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60a95-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a95-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="60a95-113">-Name</span></span>
<span data-ttu-id="60a95-114">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="60a95-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="60a95-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a95-115">-ResourceGroupName</span></span>
<span data-ttu-id="60a95-116">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="60a95-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="60a95-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a95-117">CommonParameters</span></span>
<span data-ttu-id="60a95-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a95-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a95-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a95-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a95-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60a95-120">INPUTS</span></span>

### <span data-ttu-id="60a95-121">System. String</span><span class="sxs-lookup"><span data-stu-id="60a95-121">System.String</span></span>

## <span data-ttu-id="60a95-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60a95-122">OUTPUTS</span></span>

### <span data-ttu-id="60a95-123">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="60a95-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="60a95-124">Note</span><span class="sxs-lookup"><span data-stu-id="60a95-124">NOTES</span></span>
* <span data-ttu-id="60a95-125">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="60a95-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="60a95-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60a95-126">RELATED LINKS</span></span>

[<span data-ttu-id="60a95-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="60a95-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="60a95-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="60a95-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="60a95-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="60a95-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


