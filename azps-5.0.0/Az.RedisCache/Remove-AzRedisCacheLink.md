---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 38c72a19e73d87272fb91fb6472a41496658e7d6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201138"
---
# <span data-ttu-id="9e666-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9e666-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="9e666-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e666-102">SYNOPSIS</span></span>
<span data-ttu-id="9e666-103">Rimuovere un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="9e666-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="9e666-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e666-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e666-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e666-105">DESCRIPTION</span></span>
<span data-ttu-id="9e666-106">Rimuovere un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="9e666-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="9e666-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e666-107">EXAMPLES</span></span>

### <span data-ttu-id="9e666-108">Esempio 1: rimuovere un collegamento di replica geo</span><span class="sxs-lookup"><span data-stu-id="9e666-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="9e666-109">Questo comando rimuove i collegamenti di Geo-replica in cui la cache di redis denominata myCache1 è primaria e la cache di redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="9e666-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="9e666-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e666-110">PARAMETERS</span></span>

### <span data-ttu-id="9e666-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e666-111">-DefaultProfile</span></span>
<span data-ttu-id="9e666-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e666-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e666-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e666-113">-PassThru</span></span>
<span data-ttu-id="9e666-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9e666-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e666-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="9e666-115">-PrimaryServerName</span></span>
<span data-ttu-id="9e666-116">Nome della cache di redis principale in collegamento.</span><span class="sxs-lookup"><span data-stu-id="9e666-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="9e666-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="9e666-117">-SecondaryServerName</span></span>
<span data-ttu-id="9e666-118">Nome della cache di redis secondaria in collegamento.</span><span class="sxs-lookup"><span data-stu-id="9e666-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="9e666-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e666-119">-Confirm</span></span>
<span data-ttu-id="9e666-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e666-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e666-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e666-121">-WhatIf</span></span>
<span data-ttu-id="9e666-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e666-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e666-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e666-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e666-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e666-124">CommonParameters</span></span>
<span data-ttu-id="9e666-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e666-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e666-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e666-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e666-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e666-127">INPUTS</span></span>

### <span data-ttu-id="9e666-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9e666-128">System.String</span></span>

## <span data-ttu-id="9e666-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e666-129">OUTPUTS</span></span>

### <span data-ttu-id="9e666-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e666-130">System.Boolean</span></span>

## <span data-ttu-id="9e666-131">Note</span><span class="sxs-lookup"><span data-stu-id="9e666-131">NOTES</span></span>

## <span data-ttu-id="9e666-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e666-132">RELATED LINKS</span></span>

[<span data-ttu-id="9e666-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9e666-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="9e666-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="9e666-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="9e666-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e666-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="9e666-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e666-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="9e666-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e666-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="9e666-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="9e666-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)