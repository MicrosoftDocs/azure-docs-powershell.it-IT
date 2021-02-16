---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201982"
---
# <span data-ttu-id="71d65-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71d65-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="71d65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71d65-102">SYNOPSIS</span></span>
<span data-ttu-id="71d65-103">Rimuovere una regola del firewall da una cache di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="71d65-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="71d65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71d65-104">SYNTAX</span></span>

### <span data-ttu-id="71d65-105">NormalParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71d65-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71d65-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="71d65-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71d65-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71d65-107">DESCRIPTION</span></span>
<span data-ttu-id="71d65-108">Rimuovere una regola del firewall da una cache di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="71d65-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="71d65-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71d65-109">EXAMPLES</span></span>

### <span data-ttu-id="71d65-110">Esempio 1: Rimuovere una singola regola del firewall</span><span class="sxs-lookup"><span data-stu-id="71d65-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="71d65-111">Questo comando rimuove dalla cache di Redis una regola del firewall denominata ruleone denominata mycache.</span><span class="sxs-lookup"><span data-stu-id="71d65-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="71d65-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71d65-112">PARAMETERS</span></span>

### <span data-ttu-id="71d65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d65-113">-DefaultProfile</span></span>
<span data-ttu-id="71d65-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71d65-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71d65-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71d65-115">-InputObject</span></span>
<span data-ttu-id="71d65-116">Oggetto di tipo PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71d65-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="71d65-117">-Name</span><span class="sxs-lookup"><span data-stu-id="71d65-117">-Name</span></span>
<span data-ttu-id="71d65-118">Nome della cache ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="71d65-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="71d65-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71d65-119">-PassThru</span></span>
<span data-ttu-id="71d65-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="71d65-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="71d65-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d65-121">-ResourceGroupName</span></span>
<span data-ttu-id="71d65-122">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="71d65-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="71d65-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="71d65-123">-RuleName</span></span>
<span data-ttu-id="71d65-124">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="71d65-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="71d65-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71d65-125">-Confirm</span></span>
<span data-ttu-id="71d65-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71d65-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71d65-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71d65-127">-WhatIf</span></span>
<span data-ttu-id="71d65-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71d65-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71d65-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71d65-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71d65-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d65-130">CommonParameters</span></span>
<span data-ttu-id="71d65-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d65-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d65-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d65-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d65-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="71d65-133">INPUTS</span></span>

### <span data-ttu-id="71d65-134">System.String</span><span class="sxs-lookup"><span data-stu-id="71d65-134">System.String</span></span>

### <span data-ttu-id="71d65-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71d65-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="71d65-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71d65-136">OUTPUTS</span></span>

### <span data-ttu-id="71d65-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71d65-137">System.Boolean</span></span>

## <span data-ttu-id="71d65-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="71d65-138">NOTES</span></span>

## <span data-ttu-id="71d65-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71d65-139">RELATED LINKS</span></span>

[<span data-ttu-id="71d65-140">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71d65-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="71d65-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71d65-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="71d65-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="71d65-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="71d65-143">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="71d65-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="71d65-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="71d65-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="71d65-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="71d65-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)