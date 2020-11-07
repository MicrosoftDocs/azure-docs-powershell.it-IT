---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCache.md
ms.openlocfilehash: 1e7f57ce251c6f95a74b2ca0a55aa1caa92349a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677520"
---
# <span data-ttu-id="8468d-101">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468d-101">Get-AzRedisCache</span></span>

## <span data-ttu-id="8468d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8468d-102">SYNOPSIS</span></span>
<span data-ttu-id="8468d-103">Ottiene una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="8468d-103">Gets a Redis Cache.</span></span>

## <span data-ttu-id="8468d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8468d-104">SYNTAX</span></span>

```
Get-AzRedisCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8468d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8468d-105">DESCRIPTION</span></span>
<span data-ttu-id="8468d-106">Il cmdlet **Get-AzRedisCache** ottiene la cache di Azure Redis specificata.</span><span class="sxs-lookup"><span data-stu-id="8468d-106">The **Get-AzRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="8468d-107">Se non si specificano parametri, questa operazione ottiene ogni cache di redis per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8468d-107">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="8468d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8468d-108">EXAMPLES</span></span>

### <span data-ttu-id="8468d-109">Esempio 1: ottenere una cache Redis per nome</span><span class="sxs-lookup"><span data-stu-id="8468d-109">Example 1: Get a Redis Cache by name</span></span>
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

<span data-ttu-id="8468d-110">Questo comando consente di ottenere la cache Redis denominata esisto.</span><span class="sxs-lookup"><span data-stu-id="8468d-110">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="8468d-111">Esempio 2: ottenere ogni cache di redis in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8468d-111">Example 2: Get every Redis Cache in a resource group</span></span>
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

<span data-ttu-id="8468d-112">Questo comando consente di ottenere ogni cache di redis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8468d-112">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="8468d-113">Esempio 3: ottenere ogni cache di redis nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="8468d-113">Example 3: Get every Redis Cache in the current subscription</span></span>
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

<span data-ttu-id="8468d-114">Questo comando ottiene ogni cache di redis nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8468d-114">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="8468d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8468d-115">PARAMETERS</span></span>

### <span data-ttu-id="8468d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8468d-116">-DefaultProfile</span></span>
<span data-ttu-id="8468d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8468d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8468d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8468d-118">-Name</span></span>
<span data-ttu-id="8468d-119">Specifica il nome della cache Redis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="8468d-119">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="8468d-120">Usare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="8468d-120">Use with the *ResourceGroupName* parameter.</span></span>

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

### <span data-ttu-id="8468d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8468d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8468d-122">Specifica il nome del gruppo di risorse che contiene la cache Redis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="8468d-122">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>
<span data-ttu-id="8468d-123">Se specifichi solo il parametro *ResourceGroupName* , questa operazione ottiene ogni cache Redis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="8468d-123">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

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

### <span data-ttu-id="8468d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8468d-124">CommonParameters</span></span>
<span data-ttu-id="8468d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8468d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8468d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8468d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8468d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8468d-127">INPUTS</span></span>

### <span data-ttu-id="8468d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8468d-128">System.String</span></span>

## <span data-ttu-id="8468d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8468d-129">OUTPUTS</span></span>

### <span data-ttu-id="8468d-130">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="8468d-130">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="8468d-131">Note</span><span class="sxs-lookup"><span data-stu-id="8468d-131">NOTES</span></span>

## <span data-ttu-id="8468d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8468d-132">RELATED LINKS</span></span>

[<span data-ttu-id="8468d-133">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468d-133">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="8468d-134">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468d-134">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="8468d-135">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="8468d-135">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

