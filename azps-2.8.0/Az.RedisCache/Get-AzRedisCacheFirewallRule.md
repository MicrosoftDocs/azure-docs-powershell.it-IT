---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 1bf6394621435293be1d00d4a9e9f435c160e668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855598"
---
# <span data-ttu-id="49884-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="49884-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="49884-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49884-102">SYNOPSIS</span></span>
<span data-ttu-id="49884-103">Ottenere le regole del firewall impostate nella cache Redis.</span><span class="sxs-lookup"><span data-stu-id="49884-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="49884-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49884-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49884-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49884-105">DESCRIPTION</span></span>
<span data-ttu-id="49884-106">Se il parametro **RuleName** , se disponibile, cmdlet **Get-AzRedisCacheFirewallRule** ottiene dettagli sulla regola del firewall specificata nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="49884-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="49884-107">Se viene specificata solo **Name** , questa operazione consente di ottenere tutte le regole del firewall disponibili nella cache Redis.</span><span class="sxs-lookup"><span data-stu-id="49884-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="49884-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49884-108">EXAMPLES</span></span>

### <span data-ttu-id="49884-109">Esempio 1: ottenere una singola regola del firewall</span><span class="sxs-lookup"><span data-stu-id="49884-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="49884-110">Questo comando ottiene la regola del firewall denominata ruleone dalla cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="49884-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="49884-111">Esempio 2: ottenere tutte le regole del firewall</span><span class="sxs-lookup"><span data-stu-id="49884-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="49884-112">Questo comando consente di ottenere tutte le regole del firewall dalla cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="49884-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="49884-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49884-113">PARAMETERS</span></span>

### <span data-ttu-id="49884-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49884-114">-DefaultProfile</span></span>
<span data-ttu-id="49884-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49884-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49884-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="49884-116">-Name</span></span>
<span data-ttu-id="49884-117">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="49884-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="49884-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49884-118">-ResourceGroupName</span></span>
<span data-ttu-id="49884-119">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="49884-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="49884-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="49884-120">-RuleName</span></span>
<span data-ttu-id="49884-121">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="49884-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="49884-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49884-122">CommonParameters</span></span>
<span data-ttu-id="49884-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49884-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49884-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49884-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49884-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49884-125">INPUTS</span></span>

### <span data-ttu-id="49884-126">System. String</span><span class="sxs-lookup"><span data-stu-id="49884-126">System.String</span></span>

## <span data-ttu-id="49884-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49884-127">OUTPUTS</span></span>

### <span data-ttu-id="49884-128">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="49884-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="49884-129">Note</span><span class="sxs-lookup"><span data-stu-id="49884-129">NOTES</span></span>

## <span data-ttu-id="49884-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49884-130">RELATED LINKS</span></span>

[<span data-ttu-id="49884-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="49884-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="49884-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="49884-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="49884-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49884-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="49884-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49884-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="49884-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49884-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="49884-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49884-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)