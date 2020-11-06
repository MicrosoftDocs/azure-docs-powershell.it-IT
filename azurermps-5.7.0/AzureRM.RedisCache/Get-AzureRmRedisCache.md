---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 1e91aa946e89b8231ea2c58b28c686d603855ada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514191"
---
# <span data-ttu-id="02b54-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02b54-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="02b54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02b54-102">SYNOPSIS</span></span>
<span data-ttu-id="02b54-103">Ottiene una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="02b54-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02b54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02b54-104">SYNTAX</span></span>

```
Get-AzureRmRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02b54-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02b54-105">DESCRIPTION</span></span>
<span data-ttu-id="02b54-106">Il cmdlet **Get-AzureRmRedisCache** ottiene la cache di Azure Redis specificata.</span><span class="sxs-lookup"><span data-stu-id="02b54-106">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="02b54-107">Se non si specificano parametri, questa operazione ottiene ogni cache di redis per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="02b54-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="02b54-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02b54-108">EXAMPLES</span></span>

### <span data-ttu-id="02b54-109">Esempio 1: ottenere una cache Redis per nome</span><span class="sxs-lookup"><span data-stu-id="02b54-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -Name "myexists"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="02b54-110">Questo comando consente di ottenere la cache Redis denominata esisto.</span><span class="sxs-lookup"><span data-stu-id="02b54-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="02b54-111">Esempio 2: ottenere ogni cache di redis in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="02b54-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="02b54-112">Questo comando consente di ottenere ogni cache di redis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="02b54-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="02b54-113">Esempio 3: ottenere ogni cache di redis nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="02b54-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzureRmRedisCache

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
        Location           : North Central US
        Name               : myexists
        Type               : Microsoft.Cache/Redis
        HostName           : myexists.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 1GB
        Sku                : Basic
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
        Location           : North Central US
        Name               : myearlier
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : True
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Standard
        Tag                : {}
        Zone               : []

        ResourceGroupName  : myGroup2
        Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
        Location           : North Central US
        Name               : myearlier2
        Type               : Microsoft.Cache/Redis
        HostName           : myearlier2.redis.cache.windows.net
        Port               : 6379
        ProvisioningState  : succeeded
        SslPort            : 6380
        RedisConfiguration : {}
        EnableNonSslPort   : False
        RedisVersion       : 2.8
        Size               : 250MB
        Sku                : Basic
        Tag                : {}
        Zone               : []
```

<span data-ttu-id="02b54-114">Questo comando ottiene ogni cache di redis nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="02b54-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="02b54-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02b54-115">PARAMETERS</span></span>

### <span data-ttu-id="02b54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b54-116">-DefaultProfile</span></span>
<span data-ttu-id="02b54-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02b54-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02b54-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="02b54-118">-Name</span></span>
<span data-ttu-id="02b54-119">Specifica il nome della cache Redis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="02b54-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="02b54-120">Usare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="02b54-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="02b54-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02b54-121">-ResourceGroupName</span></span>
<span data-ttu-id="02b54-122">Specifica il nome del gruppo di risorse che contiene la cache Redis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="02b54-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="02b54-123">Se specifichi solo il parametro *ResourceGroupName* , questa operazione ottiene ogni cache Redis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="02b54-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="02b54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b54-124">CommonParameters</span></span>
<span data-ttu-id="02b54-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b54-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b54-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b54-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02b54-127">INPUTS</span></span>

### <span data-ttu-id="02b54-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="02b54-128">None</span></span>
<span data-ttu-id="02b54-129">È possibile reindirizzare l'input a questo cmdlet per nome, ma non per valore.</span><span class="sxs-lookup"><span data-stu-id="02b54-129">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="02b54-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02b54-130">OUTPUTS</span></span>

### <span data-ttu-id="02b54-131">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="02b54-131">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="02b54-132">Restituisce una matrice di oggetti **RedisCacheAttributes** .</span><span class="sxs-lookup"><span data-stu-id="02b54-132">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="02b54-133">Note</span><span class="sxs-lookup"><span data-stu-id="02b54-133">NOTES</span></span>

## <span data-ttu-id="02b54-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02b54-134">RELATED LINKS</span></span>

[<span data-ttu-id="02b54-135">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02b54-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="02b54-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02b54-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="02b54-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="02b54-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


