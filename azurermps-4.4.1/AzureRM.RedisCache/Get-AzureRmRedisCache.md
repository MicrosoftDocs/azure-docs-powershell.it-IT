---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521146"
---
# <span data-ttu-id="a8f6b-101">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8f6b-101">Get-AzureRmRedisCache</span></span>

## <span data-ttu-id="a8f6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="a8f6b-103">Ottiene una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-103">Gets a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8f6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8f6b-104">SYNTAX</span></span>

### <span data-ttu-id="a8f6b-105">Tutti in abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8f6b-105">All In Subscription (Default)</span></span>
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8f6b-106">Tutti nel gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a8f6b-106">All In Resource Group</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8f6b-107">Cache Redis specifica</span><span class="sxs-lookup"><span data-stu-id="a8f6b-107">Specific Redis Cache</span></span>
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8f6b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8f6b-108">DESCRIPTION</span></span>
<span data-ttu-id="a8f6b-109">Il cmdlet **Get-AzureRmRedisCache** ottiene la cache di Azure Redis specificata.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-109">The **Get-AzureRmRedisCache** cmdlet gets the specified Azure Redis Cache.</span></span>
<span data-ttu-id="a8f6b-110">Se non si specificano parametri, questa operazione ottiene ogni cache di redis per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-110">If you specify no parameters, this operation gets every Redis Cache for the current subscription.</span></span>

## <span data-ttu-id="a8f6b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8f6b-111">EXAMPLES</span></span>

### <span data-ttu-id="a8f6b-112">Esempio 1: ottenere una cache Redis per nome</span><span class="sxs-lookup"><span data-stu-id="a8f6b-112">Example 1: Get a Redis Cache by name</span></span>
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

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
```

<span data-ttu-id="a8f6b-113">Questo comando consente di ottenere la cache Redis denominata esisto.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-113">This command gets the Redis Cache named myexists.</span></span>

### <span data-ttu-id="a8f6b-114">Esempio 2: ottenere ogni cache di redis in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a8f6b-114">Example 2: Get every Redis Cache in a resource group</span></span>
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
```

<span data-ttu-id="a8f6b-115">Questo comando consente di ottenere ogni cache di redis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-115">This command gets every Redis Cache in the specified resource group.</span></span>

### <span data-ttu-id="a8f6b-116">Esempio 3: ottenere ogni cache di redis nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="a8f6b-116">Example 3: Get every Redis Cache in the current subscription</span></span>
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
```

<span data-ttu-id="a8f6b-117">Questo comando ottiene ogni cache di redis nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-117">This command gets every Redis Cache in the current subscription.</span></span>

## <span data-ttu-id="a8f6b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8f6b-118">PARAMETERS</span></span>

### <span data-ttu-id="a8f6b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8f6b-119">-Name</span></span>
<span data-ttu-id="a8f6b-120">Specifica il nome della cache Redis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-120">Specifies the name of the Redis Cache to get.</span></span>
<span data-ttu-id="a8f6b-121">Usare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a8f6b-121">Use with the *ResourceGroupName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f6b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8f6b-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8f6b-123">Specifica il nome del gruppo di risorse che contiene la cache Redis da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-123">Specifies the name of the resource group that contains the Redis Cache to get.</span></span>

<span data-ttu-id="a8f6b-124">Se specifichi solo il parametro *ResourceGroupName* , questa operazione ottiene ogni cache Redis nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-124">If you specify only the *ResourceGroupName* parameter, this operation gets every Redis Cache in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8f6b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8f6b-125">-DefaultProfile</span></span>
<span data-ttu-id="a8f6b-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8f6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8f6b-127">CommonParameters</span></span>
<span data-ttu-id="a8f6b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8f6b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8f6b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8f6b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8f6b-130">INPUTS</span></span>

### <span data-ttu-id="a8f6b-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a8f6b-131">None</span></span>
<span data-ttu-id="a8f6b-132">È possibile reindirizzare l'input a questo cmdlet per nome, ma non per valore.</span><span class="sxs-lookup"><span data-stu-id="a8f6b-132">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="a8f6b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8f6b-133">OUTPUTS</span></span>

### <span data-ttu-id="a8f6b-134">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="a8f6b-134">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="a8f6b-135">Restituisce una matrice di oggetti **RedisCacheAttributes** .</span><span class="sxs-lookup"><span data-stu-id="a8f6b-135">Returns an array of **RedisCacheAttributes** objects.</span></span>

## <span data-ttu-id="a8f6b-136">Note</span><span class="sxs-lookup"><span data-stu-id="a8f6b-136">NOTES</span></span>

## <span data-ttu-id="a8f6b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8f6b-137">RELATED LINKS</span></span>

[<span data-ttu-id="a8f6b-138">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8f6b-138">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a8f6b-139">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8f6b-139">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="a8f6b-140">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a8f6b-140">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


