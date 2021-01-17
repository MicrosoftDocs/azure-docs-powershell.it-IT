---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474378"
---
# <span data-ttu-id="3e221-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3e221-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="3e221-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e221-102">SYNOPSIS</span></span>
<span data-ttu-id="3e221-103">Creare un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="3e221-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="3e221-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e221-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e221-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e221-105">DESCRIPTION</span></span>
<span data-ttu-id="3e221-106">Creare un collegamento di replica geo tra due cache Redis.</span><span class="sxs-lookup"><span data-stu-id="3e221-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="3e221-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e221-107">EXAMPLES</span></span>

### <span data-ttu-id="3e221-108">Esempio 1: creare un collegamento tra due cache</span><span class="sxs-lookup"><span data-stu-id="3e221-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="3e221-109">Questo comando crea un collegamento di replica geografica tra le cache di redis myCache1 e mycache2.</span><span class="sxs-lookup"><span data-stu-id="3e221-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="3e221-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e221-110">PARAMETERS</span></span>

### <span data-ttu-id="3e221-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e221-111">-DefaultProfile</span></span>
<span data-ttu-id="3e221-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e221-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e221-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="3e221-113">-PrimaryServerName</span></span>
<span data-ttu-id="3e221-114">Nome della cache di redis principale in collegamento.</span><span class="sxs-lookup"><span data-stu-id="3e221-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="3e221-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="3e221-115">-SecondaryServerName</span></span>
<span data-ttu-id="3e221-116">Nome della cache di redis secondaria in collegamento.</span><span class="sxs-lookup"><span data-stu-id="3e221-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="3e221-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e221-117">-Confirm</span></span>
<span data-ttu-id="3e221-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e221-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e221-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e221-119">-WhatIf</span></span>
<span data-ttu-id="3e221-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e221-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e221-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e221-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e221-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e221-122">CommonParameters</span></span>
<span data-ttu-id="3e221-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e221-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e221-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e221-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e221-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e221-125">INPUTS</span></span>

### <span data-ttu-id="3e221-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3e221-126">System.String</span></span>

## <span data-ttu-id="3e221-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e221-127">OUTPUTS</span></span>

### <span data-ttu-id="3e221-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="3e221-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="3e221-129">Note</span><span class="sxs-lookup"><span data-stu-id="3e221-129">NOTES</span></span>

## <span data-ttu-id="3e221-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e221-130">RELATED LINKS</span></span>

[<span data-ttu-id="3e221-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3e221-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="3e221-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="3e221-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="3e221-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e221-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="3e221-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e221-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3e221-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e221-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3e221-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e221-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)