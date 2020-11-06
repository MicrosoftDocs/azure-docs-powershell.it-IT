---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: e5e909107d740f67e3407347625270226c87839d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519714"
---
# <span data-ttu-id="e70e2-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e70e2-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="e70e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e70e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e70e2-103">Creare una regola del firewall in una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="e70e2-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e70e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e70e2-104">SYNTAX</span></span>

### <span data-ttu-id="e70e2-105">NormalParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e70e2-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e70e2-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="e70e2-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e70e2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e70e2-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e70e2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e70e2-108">DESCRIPTION</span></span>
<span data-ttu-id="e70e2-109">Creare una regola del firewall in una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="e70e2-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="e70e2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e70e2-110">EXAMPLES</span></span>

### <span data-ttu-id="e70e2-111">Esempio 1: creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e70e2-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="e70e2-112">Questo comando crea la regola del firewall denominata ruleone nella cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="e70e2-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="e70e2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e70e2-113">PARAMETERS</span></span>

### <span data-ttu-id="e70e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e70e2-114">-DefaultProfile</span></span>
<span data-ttu-id="e70e2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e70e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e70e2-116">-FineIP</span><span class="sxs-lookup"><span data-stu-id="e70e2-116">-EndIP</span></span>
<span data-ttu-id="e70e2-117">Indirizzo IP finale.</span><span class="sxs-lookup"><span data-stu-id="e70e2-117">Ending IP address.</span></span>

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

### <span data-ttu-id="e70e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e70e2-118">-InputObject</span></span>
<span data-ttu-id="e70e2-119">oggetto di tipo RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="e70e2-119">object of type RedisCacheAttributes</span></span>

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

### <span data-ttu-id="e70e2-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e70e2-120">-Name</span></span>
<span data-ttu-id="e70e2-121">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="e70e2-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="e70e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e70e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="e70e2-123">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="e70e2-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="e70e2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e70e2-124">-ResourceId</span></span>
<span data-ttu-id="e70e2-125">ID ARM della cache Redis.</span><span class="sxs-lookup"><span data-stu-id="e70e2-125">ARM Id of Redis Cache.</span></span>

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

### <span data-ttu-id="e70e2-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e70e2-126">-RuleName</span></span>
<span data-ttu-id="e70e2-127">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e70e2-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="e70e2-128">-IPIniziale</span><span class="sxs-lookup"><span data-stu-id="e70e2-128">-StartIP</span></span>
<span data-ttu-id="e70e2-129">Indirizzo IP iniziale.</span><span class="sxs-lookup"><span data-stu-id="e70e2-129">Starting IP address.</span></span>

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

### <span data-ttu-id="e70e2-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e70e2-130">-Confirm</span></span>
<span data-ttu-id="e70e2-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e70e2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e70e2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e70e2-132">-WhatIf</span></span>
<span data-ttu-id="e70e2-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e70e2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e70e2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e70e2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e70e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e70e2-135">CommonParameters</span></span>
<span data-ttu-id="e70e2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e70e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e70e2-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e70e2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e70e2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e70e2-138">INPUTS</span></span>

### <span data-ttu-id="e70e2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e70e2-139">System.String</span></span>

### <span data-ttu-id="e70e2-140">Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="e70e2-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>
<span data-ttu-id="e70e2-141">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e70e2-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e70e2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e70e2-142">OUTPUTS</span></span>

### <span data-ttu-id="e70e2-143">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e70e2-143">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="e70e2-144">Note</span><span class="sxs-lookup"><span data-stu-id="e70e2-144">NOTES</span></span>

## <span data-ttu-id="e70e2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e70e2-145">RELATED LINKS</span></span>

[<span data-ttu-id="e70e2-146">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e70e2-146">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e70e2-147">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e70e2-147">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="e70e2-148">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e70e2-148">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="e70e2-149">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e70e2-149">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e70e2-150">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e70e2-150">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e70e2-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e70e2-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
