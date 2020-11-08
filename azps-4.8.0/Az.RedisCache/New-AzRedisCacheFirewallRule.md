---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191967"
---
# <span data-ttu-id="7284d-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7284d-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="7284d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7284d-102">SYNOPSIS</span></span>
<span data-ttu-id="7284d-103">Creare una regola del firewall in una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="7284d-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="7284d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7284d-104">SYNTAX</span></span>

### <span data-ttu-id="7284d-105">NormalParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7284d-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7284d-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="7284d-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7284d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7284d-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7284d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7284d-108">DESCRIPTION</span></span>
<span data-ttu-id="7284d-109">Creare una regola del firewall in una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="7284d-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="7284d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7284d-110">EXAMPLES</span></span>

### <span data-ttu-id="7284d-111">Esempio 1: creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="7284d-111">Example 1: Create a firewall rule</span></span>
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

<span data-ttu-id="7284d-112">Questo comando crea la regola del firewall denominata ruleone nella cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="7284d-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="7284d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7284d-113">PARAMETERS</span></span>

### <span data-ttu-id="7284d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7284d-114">-DefaultProfile</span></span>
<span data-ttu-id="7284d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7284d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7284d-116">-FineIP</span><span class="sxs-lookup"><span data-stu-id="7284d-116">-EndIP</span></span>
<span data-ttu-id="7284d-117">Indirizzo IP finale.</span><span class="sxs-lookup"><span data-stu-id="7284d-117">Ending IP address.</span></span>

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

### <span data-ttu-id="7284d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7284d-118">-InputObject</span></span>
<span data-ttu-id="7284d-119">oggetto di tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="7284d-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="7284d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7284d-120">-Name</span></span>
<span data-ttu-id="7284d-121">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="7284d-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="7284d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7284d-122">-ResourceGroupName</span></span>
<span data-ttu-id="7284d-123">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="7284d-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="7284d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7284d-124">-ResourceId</span></span>
<span data-ttu-id="7284d-125">ID ARM della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="7284d-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="7284d-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="7284d-126">-RuleName</span></span>
<span data-ttu-id="7284d-127">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="7284d-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="7284d-128">-IPIniziale</span><span class="sxs-lookup"><span data-stu-id="7284d-128">-StartIP</span></span>
<span data-ttu-id="7284d-129">Indirizzo IP iniziale.</span><span class="sxs-lookup"><span data-stu-id="7284d-129">Starting IP address.</span></span>

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

### <span data-ttu-id="7284d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7284d-130">-Confirm</span></span>
<span data-ttu-id="7284d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7284d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7284d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7284d-132">-WhatIf</span></span>
<span data-ttu-id="7284d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7284d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7284d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7284d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7284d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7284d-135">CommonParameters</span></span>
<span data-ttu-id="7284d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7284d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7284d-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7284d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7284d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7284d-138">INPUTS</span></span>

### <span data-ttu-id="7284d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7284d-139">System.String</span></span>

### <span data-ttu-id="7284d-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="7284d-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="7284d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7284d-141">OUTPUTS</span></span>

### <span data-ttu-id="7284d-142">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7284d-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="7284d-143">Note</span><span class="sxs-lookup"><span data-stu-id="7284d-143">NOTES</span></span>

## <span data-ttu-id="7284d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7284d-144">RELATED LINKS</span></span>

[<span data-ttu-id="7284d-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7284d-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7284d-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7284d-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="7284d-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7284d-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="7284d-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7284d-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7284d-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7284d-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="7284d-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7284d-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)