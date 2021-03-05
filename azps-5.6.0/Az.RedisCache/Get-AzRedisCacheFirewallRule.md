---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 5e17eced3525a7aa318cbba19b632d3ae11d79a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014926"
---
# <span data-ttu-id="4b82a-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b82a-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="4b82a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b82a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b82a-103">Ottenere le regole del firewall impostate nella cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="4b82a-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="4b82a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b82a-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b82a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4b82a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b82a-106">Se viene specificato il parametro **RuleName,** il cmdlet **Get-AzRedisCacheFirewallRule** ottiene informazioni dettagliate sulla regola del firewall specificata nella cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="4b82a-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="4b82a-107">Se si **specifica solo il** nome, questa operazione consente di ottenere tutte le regole del firewall disponibili nella cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="4b82a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="4b82a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b82a-108">EXAMPLES</span></span>

### <span data-ttu-id="4b82a-109">Esempio 1: Ottenere una singola regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4b82a-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="4b82a-110">Questo comando recupera dalla cache di Redis la regola del firewall denominata ruleone denominata mycache.</span><span class="sxs-lookup"><span data-stu-id="4b82a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="4b82a-111">Esempio 2: Ottenere tutte le regole del firewall</span><span class="sxs-lookup"><span data-stu-id="4b82a-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="4b82a-112">Questo comando recupera tutte le regole del firewall dalla cache di Redis denominata mycache.</span><span class="sxs-lookup"><span data-stu-id="4b82a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="4b82a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b82a-113">PARAMETERS</span></span>

### <span data-ttu-id="4b82a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b82a-114">-DefaultProfile</span></span>
<span data-ttu-id="4b82a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b82a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b82a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4b82a-116">-Name</span></span>
<span data-ttu-id="4b82a-117">Nome della cache ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="4b82a-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="4b82a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b82a-118">-ResourceGroupName</span></span>
<span data-ttu-id="4b82a-119">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="4b82a-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="4b82a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4b82a-120">-RuleName</span></span>
<span data-ttu-id="4b82a-121">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="4b82a-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="4b82a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b82a-122">CommonParameters</span></span>
<span data-ttu-id="4b82a-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b82a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b82a-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b82a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b82a-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="4b82a-125">INPUTS</span></span>

### <span data-ttu-id="4b82a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4b82a-126">System.String</span></span>

## <span data-ttu-id="4b82a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b82a-127">OUTPUTS</span></span>

### <span data-ttu-id="4b82a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b82a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="4b82a-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="4b82a-129">NOTES</span></span>

## <span data-ttu-id="4b82a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b82a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4b82a-131">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b82a-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="4b82a-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b82a-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="4b82a-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4b82a-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="4b82a-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4b82a-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="4b82a-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4b82a-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="4b82a-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="4b82a-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)