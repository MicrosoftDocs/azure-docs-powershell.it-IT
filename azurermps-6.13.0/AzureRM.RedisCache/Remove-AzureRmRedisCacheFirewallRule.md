---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 25c3d0c72539ecd74e25ed455b4afcf4211c0718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686900"
---
# <span data-ttu-id="4f857-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4f857-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="4f857-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f857-102">SYNOPSIS</span></span>
<span data-ttu-id="4f857-103">Rimuovere una regola del firewall da una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="4f857-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f857-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f857-104">SYNTAX</span></span>

### <span data-ttu-id="4f857-105">NormalParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f857-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f857-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="4f857-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f857-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f857-107">DESCRIPTION</span></span>
<span data-ttu-id="4f857-108">Rimuovere una regola del firewall da una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="4f857-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="4f857-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f857-109">EXAMPLES</span></span>

### <span data-ttu-id="4f857-110">Esempio 1: rimuovere una singola regola del firewall</span><span class="sxs-lookup"><span data-stu-id="4f857-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="4f857-111">Questo comando rimuove una regola del firewall denominata ruleone dalla cache Redis denominata cache.</span><span class="sxs-lookup"><span data-stu-id="4f857-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="4f857-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f857-112">PARAMETERS</span></span>

### <span data-ttu-id="4f857-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f857-113">-DefaultProfile</span></span>
<span data-ttu-id="4f857-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f857-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f857-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f857-115">-InputObject</span></span>
<span data-ttu-id="4f857-116">oggetto di tipo PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4f857-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="4f857-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f857-117">-Name</span></span>
<span data-ttu-id="4f857-118">Nome della cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="4f857-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="4f857-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f857-119">-PassThru</span></span>
<span data-ttu-id="4f857-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4f857-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4f857-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f857-121">-ResourceGroupName</span></span>
<span data-ttu-id="4f857-122">Nome del gruppo di risorse in cui è presente la cache.</span><span class="sxs-lookup"><span data-stu-id="4f857-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="4f857-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4f857-123">-RuleName</span></span>
<span data-ttu-id="4f857-124">Nome della regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="4f857-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="4f857-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f857-125">-Confirm</span></span>
<span data-ttu-id="4f857-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f857-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f857-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f857-127">-WhatIf</span></span>
<span data-ttu-id="4f857-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f857-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f857-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f857-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f857-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f857-130">CommonParameters</span></span>
<span data-ttu-id="4f857-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f857-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f857-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f857-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f857-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f857-133">INPUTS</span></span>

### <span data-ttu-id="4f857-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4f857-134">System.String</span></span>

### <span data-ttu-id="4f857-135">Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4f857-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>
<span data-ttu-id="4f857-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4f857-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4f857-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f857-137">OUTPUTS</span></span>

### <span data-ttu-id="4f857-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f857-138">System.Boolean</span></span>

## <span data-ttu-id="4f857-139">Note</span><span class="sxs-lookup"><span data-stu-id="4f857-139">NOTES</span></span>

## <span data-ttu-id="4f857-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f857-140">RELATED LINKS</span></span>

[<span data-ttu-id="4f857-141">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4f857-141">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="4f857-142">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4f857-142">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="4f857-143">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4f857-143">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="4f857-144">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4f857-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="4f857-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4f857-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="4f857-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4f857-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
