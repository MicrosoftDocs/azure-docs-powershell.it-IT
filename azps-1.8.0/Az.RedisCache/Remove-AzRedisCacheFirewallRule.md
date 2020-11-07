---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: e24ea6e0b5bf88b17a6209f2ea69634200a10a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677489"
---
# <span data-ttu-id="73de3-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="73de3-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="73de3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73de3-102">SYNOPSIS</span></span>
<span data-ttu-id="73de3-103">Rimuovere una regola del firewall da una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="73de3-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="73de3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73de3-104">SYNTAX</span></span>

### <span data-ttu-id="73de3-105">NormalParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73de3-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73de3-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="73de3-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73de3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73de3-107">DESCRIPTION</span></span>
<span data-ttu-id="73de3-108">Rimuovere una regola del firewall da una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="73de3-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="73de3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73de3-109">EXAMPLES</span></span>

### <span data-ttu-id="73de3-110">Esempio 1: rimuovere una singola regola del firewall</span><span class="sxs-lookup"><span data-stu-id="73de3-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="73de3-111">Questo comando rimuove una regola del firewall denominata ruleone dalla cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="73de3-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="73de3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73de3-112">PARAMETERS</span></span>

### <span data-ttu-id="73de3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73de3-113">-DefaultProfile</span></span>
<span data-ttu-id="73de3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73de3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73de3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73de3-115">-InputObject</span></span>
<span data-ttu-id="73de3-116">oggetto di tipo PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="73de3-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73de3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="73de3-117">-Name</span></span>
<span data-ttu-id="73de3-118">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="73de3-118">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73de3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73de3-119">-PassThru</span></span>
<span data-ttu-id="73de3-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="73de3-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="73de3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73de3-121">-ResourceGroupName</span></span>
<span data-ttu-id="73de3-122">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="73de3-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73de3-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="73de3-123">-RuleName</span></span>
<span data-ttu-id="73de3-124">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="73de3-124">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73de3-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="73de3-125">-Confirm</span></span>
<span data-ttu-id="73de3-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73de3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73de3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73de3-127">-WhatIf</span></span>
<span data-ttu-id="73de3-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73de3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73de3-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73de3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73de3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73de3-130">CommonParameters</span></span>
<span data-ttu-id="73de3-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73de3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73de3-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73de3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73de3-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73de3-133">INPUTS</span></span>

### <span data-ttu-id="73de3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="73de3-134">System.String</span></span>

### <span data-ttu-id="73de3-135">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="73de3-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="73de3-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73de3-136">OUTPUTS</span></span>

### <span data-ttu-id="73de3-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73de3-137">System.Boolean</span></span>

## <span data-ttu-id="73de3-138">Note</span><span class="sxs-lookup"><span data-stu-id="73de3-138">NOTES</span></span>

## <span data-ttu-id="73de3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73de3-139">RELATED LINKS</span></span>

[<span data-ttu-id="73de3-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="73de3-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="73de3-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="73de3-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="73de3-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="73de3-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="73de3-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="73de3-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="73de3-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="73de3-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="73de3-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="73de3-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)