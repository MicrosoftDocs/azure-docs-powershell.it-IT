---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 8423c098542a621ec66a5de3255ccf62c3e8ec94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950989"
---
# <span data-ttu-id="f75bf-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f75bf-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="f75bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f75bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f75bf-103">Recupera una cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="f75bf-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="f75bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f75bf-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f75bf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f75bf-105">DESCRIPTION</span></span>
<span data-ttu-id="f75bf-106">Il cmdlet **Get-AzRedisCache** ottiene la cache di Azure Redis specificata.</span><span class="sxs-lookup"><span data-stu-id="f75bf-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="f75bf-107">Se non si specifica alcun parametro, questa operazione recupera ogni cache di Ridisposizione per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f75bf-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="f75bf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f75bf-108">EXAMPLES</span></span>

### <span data-ttu-id="f75bf-109">Esempio 1: Ottenere una cache di Ridis in base al nome</span><span class="sxs-lookup"><span data-stu-id="f75bf-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="f75bf-110">Questo comando recupera la cache di Redis denominata myexists.</span><span class="sxs-lookup"><span data-stu-id="f75bf-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="f75bf-111">Esempio 2: Ottenere ogni cache di Ridis in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f75bf-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="f75bf-112">Questo comando recupera ogni cache di Ridis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="f75bf-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="f75bf-113">Esempio 3: Ottenere ogni cache di Ridis nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="f75bf-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="f75bf-114">Questo comando recupera ogni cache di Ridis nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f75bf-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="f75bf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f75bf-115">PARAMETERS</span></span>

### <span data-ttu-id="f75bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75bf-116">-DefaultProfile</span></span>
<span data-ttu-id="f75bf-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f75bf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f75bf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f75bf-118">-Name</span></span>
<span data-ttu-id="f75bf-119">Specifica il nome della cache di Ridis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f75bf-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="f75bf-120">Usare con il *parametro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="f75bf-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="f75bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="f75bf-122">Specifica il nome del gruppo di risorse che contiene la cache di Ridis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f75bf-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="f75bf-123">Se si specifica solo il *parametro ResourceGroupName,* questa operazione recupera ogni cache di ridisposizione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="f75bf-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="f75bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75bf-124">CommonParameters</span></span>
<span data-ttu-id="f75bf-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75bf-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f75bf-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75bf-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="f75bf-127">INPUTS</span></span>

### <span data-ttu-id="f75bf-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f75bf-128">System.String</span></span>

## <span data-ttu-id="f75bf-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f75bf-129">OUTPUTS</span></span>

### <span data-ttu-id="f75bf-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="f75bf-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="f75bf-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="f75bf-131">NOTES</span></span>

## <span data-ttu-id="f75bf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f75bf-132">RELATED LINKS</span></span>

[<span data-ttu-id="f75bf-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f75bf-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f75bf-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f75bf-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f75bf-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f75bf-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


