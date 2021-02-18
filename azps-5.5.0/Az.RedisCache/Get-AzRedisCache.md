---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: cc8d6ff7e7fb55c5ee71c82a8eca4cc661b98b07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206178"
---
# <span data-ttu-id="5f396-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5f396-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="5f396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f396-102">SYNOPSIS</span></span>
<span data-ttu-id="5f396-103">Recupera una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="5f396-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="5f396-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f396-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f396-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f396-105">DESCRIPTION</span></span>
<span data-ttu-id="5f396-106">Il cmdlet **Get-AzRedisCache** ottiene la cache di Azure Redis specificata.</span><span class="sxs-lookup"><span data-stu-id="5f396-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="5f396-107">Se non si specifica alcun parametro, questa operazione recupera ogni cache di Ridisposizione per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="5f396-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="5f396-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f396-108">EXAMPLES</span></span>

### <span data-ttu-id="5f396-109">Esempio 1: Ottenere una cache di Ridis in base al nome</span><span class="sxs-lookup"><span data-stu-id="5f396-109">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzRedisCache -Name "myexists"

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

<span data-ttu-id="5f396-110">Questo comando recupera la cache di Redis denominata myexists.</span><span class="sxs-lookup"><span data-stu-id="5f396-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="5f396-111">Esempio 2: Ottenere ogni cache di Ridis in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5f396-111">Example 2: Get every Redis Cache in a resource group</span></span>
```
PS C:\>Get-AzRedisCache -ResourceGroupName "myGroup"

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

<span data-ttu-id="5f396-112">Questo comando recupera ogni cache di Ridis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f396-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="5f396-113">Esempio 3: Ottenere ogni cache di Ridis nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="5f396-113">Example 3: Get every Redis Cache in the current subscription</span></span>
```
PS C:\>Get-AzRedisCache

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

<span data-ttu-id="5f396-114">Questo comando recupera tutte le credenziali della cache di Ridis nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="5f396-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="5f396-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f396-115">PARAMETERS</span></span>

### <span data-ttu-id="5f396-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f396-116">-DefaultProfile</span></span>
<span data-ttu-id="5f396-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f396-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f396-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5f396-118">-Name</span></span>
<span data-ttu-id="5f396-119">Specifica il nome della cache di Ridis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5f396-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="5f396-120">Usare con il *parametro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="5f396-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="5f396-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f396-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f396-122">Specifica il nome del gruppo di risorse che contiene la cache di Redis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5f396-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="5f396-123">Se si specifica solo il *parametro ResourceGroupName,* questa operazione recupera ogni cache di ridisposizione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f396-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="5f396-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f396-124">CommonParameters</span></span>
<span data-ttu-id="5f396-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f396-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f396-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f396-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f396-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f396-127">INPUTS</span></span>

### <span data-ttu-id="5f396-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f396-128">System.String</span></span>

## <span data-ttu-id="5f396-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f396-129">OUTPUTS</span></span>

### <span data-ttu-id="5f396-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="5f396-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="5f396-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f396-131">NOTES</span></span>

## <span data-ttu-id="5f396-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f396-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f396-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5f396-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="5f396-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5f396-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="5f396-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="5f396-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


