---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 91eff9b6a096263b96ecae0cf9901f6dbce26c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519720"
---
# <span data-ttu-id="a551a-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a551a-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="a551a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a551a-102">SYNOPSIS</span></span>
<span data-ttu-id="a551a-103">Ottenere le regole del firewall impostate nella cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a551a-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a551a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a551a-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a551a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a551a-105">DESCRIPTION</span></span>
<span data-ttu-id="a551a-106">Se il parametro **RuleName** , se disponibile, cmdlet **Get-AzureRmRedisCacheFirewallRule** ottiene dettagli sulla regola del firewall specificata nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a551a-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="a551a-107">Se viene specificata solo **Name** , questa operazione consente di ottenere tutte le regole del firewall disponibili nella cache Redis.</span><span class="sxs-lookup"><span data-stu-id="a551a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="a551a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a551a-108">EXAMPLES</span></span>

### <span data-ttu-id="a551a-109">Esempio 1: ottenere una singola regola del firewall</span><span class="sxs-lookup"><span data-stu-id="a551a-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="a551a-110">Questo comando ottiene la regola del firewall denominata ruleone dalla cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="a551a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="a551a-111">Esempio 2: ottenere tutte le regole del firewall</span><span class="sxs-lookup"><span data-stu-id="a551a-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="a551a-112">Questo comando consente di ottenere tutte le regole del firewall dalla cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="a551a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="a551a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a551a-113">PARAMETERS</span></span>

### <span data-ttu-id="a551a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a551a-114">-DefaultProfile</span></span>
<span data-ttu-id="a551a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a551a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a551a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a551a-116">-Name</span></span>
<span data-ttu-id="a551a-117">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="a551a-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="a551a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a551a-118">-ResourceGroupName</span></span>
<span data-ttu-id="a551a-119">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="a551a-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="a551a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="a551a-120">-RuleName</span></span>
<span data-ttu-id="a551a-121">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="a551a-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="a551a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a551a-122">CommonParameters</span></span>
<span data-ttu-id="a551a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a551a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a551a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a551a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a551a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a551a-125">INPUTS</span></span>

### <span data-ttu-id="a551a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a551a-126">System.String</span></span>

## <span data-ttu-id="a551a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a551a-127">OUTPUTS</span></span>

### <span data-ttu-id="a551a-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a551a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="a551a-129">Note</span><span class="sxs-lookup"><span data-stu-id="a551a-129">NOTES</span></span>

## <span data-ttu-id="a551a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a551a-130">RELATED LINKS</span></span>

[<span data-ttu-id="a551a-131">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a551a-131">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="a551a-132">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a551a-132">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="a551a-133">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a551a-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="a551a-134">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a551a-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a551a-135">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a551a-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="a551a-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a551a-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
