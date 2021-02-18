---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206163"
---
# <span data-ttu-id="678db-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="678db-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="678db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="678db-102">SYNOPSIS</span></span>
<span data-ttu-id="678db-103">Creare una regola del firewall in una cache di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="678db-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="678db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="678db-104">SYNTAX</span></span>

### <span data-ttu-id="678db-105">NormalParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="678db-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678db-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="678db-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678db-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="678db-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="678db-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="678db-108">DESCRIPTION</span></span>
<span data-ttu-id="678db-109">Creare una regola del firewall in una cache di Ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="678db-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="678db-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="678db-110">EXAMPLES</span></span>

### <span data-ttu-id="678db-111">Esempio 1: Creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="678db-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="678db-112">Questo comando crea una regola del firewall denominata ruleone nella cache di Redis denominata mycache.</span><span class="sxs-lookup"><span data-stu-id="678db-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="678db-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="678db-113">PARAMETERS</span></span>

### <span data-ttu-id="678db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678db-114">-DefaultProfile</span></span>
<span data-ttu-id="678db-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="678db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="678db-116">-EndIP</span><span class="sxs-lookup"><span data-stu-id="678db-116">-EndIP</span></span>
<span data-ttu-id="678db-117">Indirizzo IP finale.</span><span class="sxs-lookup"><span data-stu-id="678db-117">Ending IP address.</span></span>

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

### <span data-ttu-id="678db-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="678db-118">-InputObject</span></span>
<span data-ttu-id="678db-119">Oggetto di tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="678db-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678db-120">-Name</span><span class="sxs-lookup"><span data-stu-id="678db-120">-Name</span></span>
<span data-ttu-id="678db-121">Nome della cache ridisposizione.</span><span class="sxs-lookup"><span data-stu-id="678db-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="678db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678db-122">-ResourceGroupName</span></span>
<span data-ttu-id="678db-123">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="678db-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="678db-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="678db-124">-ResourceId</span></span>
<span data-ttu-id="678db-125">ARM ID della cache di Ridis.</span><span class="sxs-lookup"><span data-stu-id="678db-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678db-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="678db-126">-RuleName</span></span>
<span data-ttu-id="678db-127">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="678db-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="678db-128">-StartIP</span><span class="sxs-lookup"><span data-stu-id="678db-128">-StartIP</span></span>
<span data-ttu-id="678db-129">Indirizzo IP iniziale.</span><span class="sxs-lookup"><span data-stu-id="678db-129">Starting IP address.</span></span>

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

### <span data-ttu-id="678db-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="678db-130">-Confirm</span></span>
<span data-ttu-id="678db-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="678db-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="678db-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678db-132">-WhatIf</span></span>
<span data-ttu-id="678db-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="678db-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="678db-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="678db-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="678db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678db-135">CommonParameters</span></span>
<span data-ttu-id="678db-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678db-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678db-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678db-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="678db-138">INPUTS</span></span>

### <span data-ttu-id="678db-139">System.String</span><span class="sxs-lookup"><span data-stu-id="678db-139">System.String</span></span>

### <span data-ttu-id="678db-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="678db-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="678db-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="678db-141">OUTPUTS</span></span>

### <span data-ttu-id="678db-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="678db-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="678db-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="678db-143">NOTES</span></span>

## <span data-ttu-id="678db-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="678db-144">RELATED LINKS</span></span>

[<span data-ttu-id="678db-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="678db-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="678db-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="678db-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="678db-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="678db-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="678db-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="678db-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="678db-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="678db-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="678db-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="678db-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)