---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 091d3d52da1319842d221881f03fca2b21353fa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685608"
---
# <span data-ttu-id="bb299-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="bb299-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="bb299-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb299-102">SYNOPSIS</span></span>
<span data-ttu-id="bb299-103">Ottiene una pianificazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="bb299-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb299-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb299-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb299-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb299-105">DESCRIPTION</span></span>
<span data-ttu-id="bb299-106">Il cmdlet **Get-AzureRmRedisCachePatchSchedule** ottiene una pianificazione delle patch per una cache in Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="bb299-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="bb299-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb299-107">EXAMPLES</span></span>

### <span data-ttu-id="bb299-108">Esempio 1: ottenere la pianificazione della patch</span><span class="sxs-lookup"><span data-stu-id="bb299-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="bb299-109">Questo comando consente di ottenere la pianificazione della patch dalla cache denominata RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="bb299-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="bb299-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb299-110">PARAMETERS</span></span>

### <span data-ttu-id="bb299-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb299-111">-DefaultProfile</span></span>
<span data-ttu-id="bb299-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb299-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb299-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb299-113">-Name</span></span>
<span data-ttu-id="bb299-114">Specifica il nome di una cache.</span><span class="sxs-lookup"><span data-stu-id="bb299-114">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb299-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb299-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb299-116">Specifica il nome del gruppo di risorse che contiene la cache.</span><span class="sxs-lookup"><span data-stu-id="bb299-116">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb299-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb299-117">CommonParameters</span></span>
<span data-ttu-id="bb299-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb299-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb299-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb299-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb299-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb299-120">INPUTS</span></span>

### <span data-ttu-id="bb299-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bb299-121">None</span></span>
<span data-ttu-id="bb299-122">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="bb299-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="bb299-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb299-123">OUTPUTS</span></span>

### <span data-ttu-id="bb299-124">Microsoft. Azure. Commands. RedisCache. Models. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="bb299-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="bb299-125">Questo cmdlet restituisce le voci della pianificazione delle patch impostate nella cache.</span><span class="sxs-lookup"><span data-stu-id="bb299-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="bb299-126">Note</span><span class="sxs-lookup"><span data-stu-id="bb299-126">NOTES</span></span>
* <span data-ttu-id="bb299-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, Web App, sito Web</span><span class="sxs-lookup"><span data-stu-id="bb299-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bb299-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb299-128">RELATED LINKS</span></span>

[<span data-ttu-id="bb299-129">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="bb299-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="bb299-130">New-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="bb299-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="bb299-131">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="bb299-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


