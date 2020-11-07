---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: dd9e070a0228cf9bc492f8680917ae0f308e9019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687018"
---
# <span data-ttu-id="7da97-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7da97-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="7da97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7da97-102">SYNOPSIS</span></span>
<span data-ttu-id="7da97-103">Creare un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="7da97-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7da97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7da97-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7da97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7da97-105">DESCRIPTION</span></span>
<span data-ttu-id="7da97-106">Creare un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="7da97-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="7da97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7da97-107">EXAMPLES</span></span>

### <span data-ttu-id="7da97-108">Esempio 1: creare un collegamento tra due cache</span><span class="sxs-lookup"><span data-stu-id="7da97-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="7da97-109">Questo comando crea un collegamento di replica geografica tra le cache di redis myCache1 e mycache2.</span><span class="sxs-lookup"><span data-stu-id="7da97-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="7da97-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7da97-110">PARAMETERS</span></span>

### <span data-ttu-id="7da97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da97-111">-DefaultProfile</span></span>
<span data-ttu-id="7da97-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7da97-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7da97-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="7da97-113">-PrimaryServerName</span></span>
<span data-ttu-id="7da97-114">Nome della cache di redis principale in collegamento.</span><span class="sxs-lookup"><span data-stu-id="7da97-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="7da97-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="7da97-115">-SecondaryServerName</span></span>
<span data-ttu-id="7da97-116">Nome della cache di redis secondaria in collegamento.</span><span class="sxs-lookup"><span data-stu-id="7da97-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="7da97-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7da97-117">-Confirm</span></span>
<span data-ttu-id="7da97-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7da97-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7da97-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7da97-119">-WhatIf</span></span>
<span data-ttu-id="7da97-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7da97-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7da97-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7da97-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7da97-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da97-122">CommonParameters</span></span>
<span data-ttu-id="7da97-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da97-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da97-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da97-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da97-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7da97-125">INPUTS</span></span>

### <span data-ttu-id="7da97-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7da97-126">System.String</span></span>

## <span data-ttu-id="7da97-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7da97-127">OUTPUTS</span></span>

### <span data-ttu-id="7da97-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="7da97-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="7da97-129">Note</span><span class="sxs-lookup"><span data-stu-id="7da97-129">NOTES</span></span>

## <span data-ttu-id="7da97-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7da97-130">RELATED LINKS</span></span>

[<span data-ttu-id="7da97-131">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7da97-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="7da97-132">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="7da97-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="7da97-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7da97-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="7da97-134">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7da97-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="7da97-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7da97-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="7da97-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7da97-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)