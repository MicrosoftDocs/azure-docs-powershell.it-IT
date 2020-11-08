---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192653"
---
# <span data-ttu-id="d212c-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d212c-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="d212c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d212c-102">SYNOPSIS</span></span>
<span data-ttu-id="d212c-103">Ottenere il collegamento Geo Replication per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="d212c-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="d212c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d212c-104">SYNTAX</span></span>

### <span data-ttu-id="d212c-105">AllLinksForCache (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d212c-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d212c-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="d212c-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d212c-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="d212c-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d212c-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="d212c-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d212c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d212c-109">DESCRIPTION</span></span>
<span data-ttu-id="d212c-110">Sono disponibili quattro modi diversi per ottenere i dettagli del collegamento alla replica geografica.</span><span class="sxs-lookup"><span data-stu-id="d212c-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="d212c-111">Specificare il nome del parametro o PrimaryServerName e/o SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="d212c-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="d212c-112">Viene assegnato il nome di tutti i collegamenti in cui verrà restituita la cache.</span><span class="sxs-lookup"><span data-stu-id="d212c-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="d212c-113">Se viene assegnato solo PrimaryServerName, verranno restituiti tutti i collegamenti in cui viene restituita la cache primaria.</span><span class="sxs-lookup"><span data-stu-id="d212c-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="d212c-114">Se viene assegnato solo SecondaryServerName, verranno restituiti tutti i collegamenti in cui viene restituita la cache secondaria.</span><span class="sxs-lookup"><span data-stu-id="d212c-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="d212c-115">Se PrimaryServerName e SecondaryServerName vengono entrambi assegnati, verrà restituito un collegamento specifico con il ruolo corretto.</span><span class="sxs-lookup"><span data-stu-id="d212c-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="d212c-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d212c-116">EXAMPLES</span></span>

### <span data-ttu-id="d212c-117">Esempio 1: ottenere using set di parametri AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="d212c-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="d212c-118">Questo comando ottiene tutti i collegamenti di replica geografica per la cache di redis denominata myCache1.</span><span class="sxs-lookup"><span data-stu-id="d212c-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="d212c-119">Esempio 2: ottenere usando set di parametri AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="d212c-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="d212c-120">Questo comando ottiene collegamenti di Geo-replica in cui la cache di redis denominata myCache1 è primaria.</span><span class="sxs-lookup"><span data-stu-id="d212c-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="d212c-121">Esempio 3: ottenere usando set di parametri AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="d212c-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="d212c-122">Questo comando ottiene collegamenti di Geo-replica in cui la cache di redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="d212c-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="d212c-123">Esempio 4: ottenere usando set di parametri SingleLink</span><span class="sxs-lookup"><span data-stu-id="d212c-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="d212c-124">Questo comando ottiene un singolo collegamento di Geo-replica in cui la cache di redis denominata myCache1 è primaria e la cache di redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="d212c-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="d212c-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d212c-125">PARAMETERS</span></span>

### <span data-ttu-id="d212c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d212c-126">-DefaultProfile</span></span>
<span data-ttu-id="d212c-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d212c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d212c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d212c-128">-Name</span></span>
<span data-ttu-id="d212c-129">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="d212c-129">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d212c-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="d212c-130">-PrimaryServerName</span></span>
<span data-ttu-id="d212c-131">Nome della cache di redis principale in collegamento.</span><span class="sxs-lookup"><span data-stu-id="d212c-131">Name of primary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d212c-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="d212c-132">-SecondaryServerName</span></span>
<span data-ttu-id="d212c-133">Nome della cache di redis secondaria in collegamento.</span><span class="sxs-lookup"><span data-stu-id="d212c-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d212c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d212c-134">CommonParameters</span></span>
<span data-ttu-id="d212c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d212c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d212c-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d212c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d212c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d212c-137">INPUTS</span></span>

### <span data-ttu-id="d212c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d212c-138">System.String</span></span>

## <span data-ttu-id="d212c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d212c-139">OUTPUTS</span></span>

### <span data-ttu-id="d212c-140">Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="d212c-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="d212c-141">Note</span><span class="sxs-lookup"><span data-stu-id="d212c-141">NOTES</span></span>

## <span data-ttu-id="d212c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d212c-142">RELATED LINKS</span></span>

[<span data-ttu-id="d212c-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d212c-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="d212c-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="d212c-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="d212c-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d212c-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="d212c-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d212c-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d212c-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d212c-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d212c-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d212c-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)