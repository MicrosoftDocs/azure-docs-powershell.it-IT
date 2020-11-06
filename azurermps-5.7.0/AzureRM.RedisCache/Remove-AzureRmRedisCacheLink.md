---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: a0532feb24966cfe05b0175080fa2333307f33e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514176"
---
# <span data-ttu-id="a7bb4-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a7bb4-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="a7bb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bb4-103">Rimuovere un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7bb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7bb4-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7bb4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="a7bb4-106">Rimuovere un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="a7bb4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="a7bb4-108">Esempio 1: rimuovere un collegamento di replica geo</span><span class="sxs-lookup"><span data-stu-id="a7bb4-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="a7bb4-109">Questo comando rimuove i collegamenti di Geo-replica in cui la cache di redis denominata myCache1 è primaria e la cache di redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="a7bb4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7bb4-110">PARAMETERS</span></span>

### <span data-ttu-id="a7bb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bb4-111">-DefaultProfile</span></span>
<span data-ttu-id="a7bb4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7bb4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7bb4-113">-PassThru</span></span>
<span data-ttu-id="a7bb4-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a7bb4-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bb4-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="a7bb4-115">-PrimaryServerName</span></span>
<span data-ttu-id="a7bb4-116">Nome della cache di redis principale in collegamento.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="a7bb4-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="a7bb4-117">-SecondaryServerName</span></span>
<span data-ttu-id="a7bb4-118">Nome della cache di redis secondaria in collegamento.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="a7bb4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a7bb4-119">-Confirm</span></span>
<span data-ttu-id="a7bb4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bb4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7bb4-121">-WhatIf</span></span>
<span data-ttu-id="a7bb4-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7bb4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bb4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bb4-124">CommonParameters</span></span>
<span data-ttu-id="a7bb4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7bb4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bb4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7bb4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bb4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7bb4-127">INPUTS</span></span>

### <span data-ttu-id="a7bb4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a7bb4-128">System.String</span></span>

## <span data-ttu-id="a7bb4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7bb4-129">OUTPUTS</span></span>

### <span data-ttu-id="a7bb4-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7bb4-130">System.Boolean</span></span>

## <span data-ttu-id="a7bb4-131">Note</span><span class="sxs-lookup"><span data-stu-id="a7bb4-131">NOTES</span></span>

## <span data-ttu-id="a7bb4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7bb4-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7bb4-133">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a7bb4-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="a7bb4-134">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="a7bb4-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="a7bb4-135">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bb4-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="a7bb4-136">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bb4-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a7bb4-137">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bb4-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="a7bb4-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bb4-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
