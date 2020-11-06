---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512392"
---
# <span data-ttu-id="f668e-101">Get-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f668e-101">Get-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="f668e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f668e-102">SYNOPSIS</span></span>
<span data-ttu-id="f668e-103">Ottenere il collegamento Geo Replication per la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="f668e-103">Get geo replication link for Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f668e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f668e-104">SYNTAX</span></span>

### <span data-ttu-id="f668e-105">AllLinksForCache (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f668e-105">AllLinksForCache (Default)</span></span>
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f668e-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="f668e-106">AllLinksForPrimaryCache</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f668e-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="f668e-107">SingleLink</span></span>
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f668e-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="f668e-108">AllLinksForSecondaryCache</span></span>
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f668e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f668e-109">DESCRIPTION</span></span>
<span data-ttu-id="f668e-110">Sono disponibili quattro modi diversi per ottenere i dettagli del collegamento alla replica geografica.</span><span class="sxs-lookup"><span data-stu-id="f668e-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="f668e-111">Specificare il nome del parametro o PrimaryServerName e/o SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="f668e-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="f668e-112">Viene assegnato il nome di tutti i collegamenti in cui verrà restituita la cache.</span><span class="sxs-lookup"><span data-stu-id="f668e-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="f668e-113">Se viene assegnato solo PrimaryServerName, verranno restituiti tutti i collegamenti in cui viene restituita la cache primaria.</span><span class="sxs-lookup"><span data-stu-id="f668e-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="f668e-114">Se viene assegnato solo SecondaryServerName, verranno restituiti tutti i collegamenti in cui viene restituita la cache secondaria.</span><span class="sxs-lookup"><span data-stu-id="f668e-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="f668e-115">Se PrimaryServerName e SecondaryServerName vengono entrambi assegnati, verrà restituito un collegamento specifico con il ruolo corretto.</span><span class="sxs-lookup"><span data-stu-id="f668e-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="f668e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f668e-116">EXAMPLES</span></span>

### <span data-ttu-id="f668e-117">Esempio 1: ottenere using set di parametri AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="f668e-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f668e-118">Questo comando ottiene tutti i collegamenti di replica geografica per la cache di redis denominata myCache1.</span><span class="sxs-lookup"><span data-stu-id="f668e-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="f668e-119">Esempio 2: ottenere usando set di parametri AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="f668e-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f668e-120">Questo comando ottiene collegamenti di Geo-replica in cui la cache di redis denominata myCache1 è primaria.</span><span class="sxs-lookup"><span data-stu-id="f668e-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="f668e-121">Esempio 3: ottenere usando set di parametri AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="f668e-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f668e-122">Questo comando ottiene collegamenti di Geo-replica in cui la cache di redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="f668e-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="f668e-123">Esempio 4: ottenere usando set di parametri SingleLink</span><span class="sxs-lookup"><span data-stu-id="f668e-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f668e-124">Questo comando ottiene un singolo collegamento di Geo-replica in cui la cache di redis denominata myCache1 è primaria e la cache di redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="f668e-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="f668e-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f668e-125">PARAMETERS</span></span>

### <span data-ttu-id="f668e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f668e-126">-DefaultProfile</span></span>
<span data-ttu-id="f668e-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f668e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f668e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f668e-128">-Name</span></span>
<span data-ttu-id="f668e-129">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="f668e-129">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f668e-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="f668e-130">-PrimaryServerName</span></span>
<span data-ttu-id="f668e-131">Nome della cache di redis principale in collegamento.</span><span class="sxs-lookup"><span data-stu-id="f668e-131">Name of primary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f668e-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="f668e-132">-SecondaryServerName</span></span>
<span data-ttu-id="f668e-133">Nome della cache di redis secondaria in collegamento.</span><span class="sxs-lookup"><span data-stu-id="f668e-133">Name of secondary redis cache in link.</span></span>

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f668e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f668e-134">CommonParameters</span></span>
<span data-ttu-id="f668e-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f668e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f668e-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f668e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f668e-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f668e-137">INPUTS</span></span>

### <span data-ttu-id="f668e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f668e-138">System.String</span></span>
<span data-ttu-id="f668e-139">È possibile reindirizzare l'input a questo cmdlet per nome, ma non per valore.</span><span class="sxs-lookup"><span data-stu-id="f668e-139">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="f668e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f668e-140">OUTPUTS</span></span>

### <span data-ttu-id="f668e-141">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f668e-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f668e-142">Note</span><span class="sxs-lookup"><span data-stu-id="f668e-142">NOTES</span></span>

## <span data-ttu-id="f668e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f668e-143">RELATED LINKS</span></span>

[<span data-ttu-id="f668e-144">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f668e-144">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="f668e-145">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f668e-145">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="f668e-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f668e-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="f668e-147">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f668e-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="f668e-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f668e-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="f668e-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="f668e-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
