---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189238"
---
# <span data-ttu-id="f90eb-101">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f90eb-101">Get-AzRedisCacheLink</span></span>

## <span data-ttu-id="f90eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f90eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f90eb-103">Ottenere il collegamento di replica geografica per la cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="f90eb-103">Get geo replication link for Redis Cache.</span></span>

## <span data-ttu-id="f90eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f90eb-104">SYNTAX</span></span>

### <span data-ttu-id="f90eb-105">AllLinksForCache (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f90eb-105">AllLinksForCache (Default)</span></span>
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f90eb-106">AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-106">AllLinksForPrimaryCache</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f90eb-107">SingleLink</span><span class="sxs-lookup"><span data-stu-id="f90eb-107">SingleLink</span></span>
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f90eb-108">AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-108">AllLinksForSecondaryCache</span></span>
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f90eb-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f90eb-109">DESCRIPTION</span></span>
<span data-ttu-id="f90eb-110">Esistono quattro diversi modi per ottenere i dettagli del collegamento di replica geografica.</span><span class="sxs-lookup"><span data-stu-id="f90eb-110">There are four different ways to get geo-replication link detail.</span></span> <span data-ttu-id="f90eb-111">Fornire il parametro Name o PrimaryServerName e/o SecondaryServerName.</span><span class="sxs-lookup"><span data-stu-id="f90eb-111">Either provide parameter Name or PrimaryServerName and/or SecondaryServerName.</span></span> <span data-ttu-id="f90eb-112">Viene assegnato il nome, quindi vengono restituiti tutti i collegamenti in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="f90eb-112">Name is given then all link where cache exists will be returned.</span></span> <span data-ttu-id="f90eb-113">Se viene assegnato solo PrimaryServerName, verranno restituiti tutti i collegamenti in cui la cache è primaria.</span><span class="sxs-lookup"><span data-stu-id="f90eb-113">If only PrimaryServerName is given then all links where cache is primary will be returned.</span></span> <span data-ttu-id="f90eb-114">Se viene assegnato solo SecondaryServerName, verranno restituiti tutti i collegamenti in cui la cache è secondaria.</span><span class="sxs-lookup"><span data-stu-id="f90eb-114">If only SecondaryServerName is given then all links where cache is secondary will be returned.</span></span> <span data-ttu-id="f90eb-115">Se vengono fornite entrambe le proprietà PrimaryServerName e SecondaryServerName, verrà restituito un collegamento specifico con il ruolo corretto.</span><span class="sxs-lookup"><span data-stu-id="f90eb-115">If PrimaryServerName and SecondaryServerName both are given then specific link with correct role will be returned.</span></span> 

## <span data-ttu-id="f90eb-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f90eb-116">EXAMPLES</span></span>

### <span data-ttu-id="f90eb-117">Esempio 1: Ottenere il set di parametri Using AllLinksForCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-117">Example 1: Get using parameter set AllLinksForCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f90eb-118">Questo comando recupera tutti i collegamenti di replica geografica per la cache di Redis denominata mycache1.</span><span class="sxs-lookup"><span data-stu-id="f90eb-118">This command gets all geo-replication links for Redis Cache named mycache1.</span></span>

### <span data-ttu-id="f90eb-119">Esempio 2: Ottenere l'uso del set di parametri AllLinksForPrimaryCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-119">Example 2: Get using parameter set AllLinksForPrimaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f90eb-120">Questo comando recupera i collegamenti di replica geografica in cui la cache di Redis denominata mycache1 è primaria.</span><span class="sxs-lookup"><span data-stu-id="f90eb-120">This command gets geo-replication links where Redis Cache named mycache1 is primary.</span></span>

### <span data-ttu-id="f90eb-121">Esempio 3: Ottenere l'uso del set di parametri AllLinksForSecondaryCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-121">Example 3: Get using parameter set AllLinksForSecondaryCache</span></span>
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f90eb-122">Questo comando recupera i collegamenti di replica geografica in cui la cache di Redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="f90eb-122">This command gets geo-replication links where Redis Cache named mycache2 is secondary.</span></span>

### <span data-ttu-id="f90eb-123">Esempio 4: Usare il set di parametri SingleLink</span><span class="sxs-lookup"><span data-stu-id="f90eb-123">Example 4: Get using parameter set SingleLink</span></span>
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

<span data-ttu-id="f90eb-124">Questo comando recupera un singolo collegamento di replica geografica in cui la cache di Redis denominata mycache1 è primaria e la cache di Redis denominata mycache2 è secondaria.</span><span class="sxs-lookup"><span data-stu-id="f90eb-124">This command gets a single geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="f90eb-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f90eb-125">PARAMETERS</span></span>

### <span data-ttu-id="f90eb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f90eb-126">-DefaultProfile</span></span>
<span data-ttu-id="f90eb-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f90eb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f90eb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f90eb-128">-Name</span></span>
<span data-ttu-id="f90eb-129">Nome della cache ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="f90eb-129">Name of redis cache.</span></span>

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

### <span data-ttu-id="f90eb-130">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="f90eb-130">-PrimaryServerName</span></span>
<span data-ttu-id="f90eb-131">Nome della cache dei ridisattivati primari nel collegamento.</span><span class="sxs-lookup"><span data-stu-id="f90eb-131">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="f90eb-132">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="f90eb-132">-SecondaryServerName</span></span>
<span data-ttu-id="f90eb-133">Nome della cache di ridisposizione secondaria nel collegamento.</span><span class="sxs-lookup"><span data-stu-id="f90eb-133">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="f90eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f90eb-134">CommonParameters</span></span>
<span data-ttu-id="f90eb-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f90eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f90eb-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f90eb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f90eb-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="f90eb-137">INPUTS</span></span>

### <span data-ttu-id="f90eb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f90eb-138">System.String</span></span>

## <span data-ttu-id="f90eb-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f90eb-139">OUTPUTS</span></span>

### <span data-ttu-id="f90eb-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="f90eb-140">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="f90eb-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="f90eb-141">NOTES</span></span>

## <span data-ttu-id="f90eb-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f90eb-142">RELATED LINKS</span></span>

[<span data-ttu-id="f90eb-143">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f90eb-143">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="f90eb-144">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="f90eb-144">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="f90eb-145">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-145">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="f90eb-146">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-146">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="f90eb-147">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-147">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="f90eb-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="f90eb-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)