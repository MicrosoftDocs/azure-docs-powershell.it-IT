---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bcc40b77208506712a319d7f43d74f8928e18927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511080"
---
# <span data-ttu-id="b56d8-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b56d8-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="b56d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b56d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b56d8-103">Crea una configurazione WAF per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b56d8-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b56d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b56d8-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b56d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b56d8-105">DESCRIPTION</span></span>
<span data-ttu-id="b56d8-106">Il cmdlet **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** crea una configurazione WAF (Web Application Firewall) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b56d8-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="b56d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b56d8-107">EXAMPLES</span></span>

### <span data-ttu-id="b56d8-108">Esempio 1: creare una configurazione firewall applicazione Web per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="b56d8-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="b56d8-109">Il primo comando crea una nuova configurazione del gruppo di regole disabilitata per il gruppo di regole denominato "REQUEST-942-APPLICATION-ATTACK-SQLI" con la regola 942130 e la regola 942140 disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b56d8-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="b56d8-110">Il secondo comando crea un'altra configurazione del gruppo di regole disabilitata per un gruppo di regole denominato "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="b56d8-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="b56d8-111">Nessuna regola viene approvata in modo specifico e quindi tutte le regole del gruppo di regole verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="b56d8-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="b56d8-112">L'ultimo comando crea quindi una configurazione WAF con le regole del firewall disabilitate come configurate in $disabledRuleGroup 1 e $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="b56d8-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="b56d8-113">La nuova configurazione di WAF viene archiviata nella variabile $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="b56d8-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="b56d8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b56d8-114">PARAMETERS</span></span>

### <span data-ttu-id="b56d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56d8-115">-DefaultProfile</span></span>
<span data-ttu-id="b56d8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b56d8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="b56d8-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="b56d8-118">Gruppi di regole disabilitati.</span><span class="sxs-lookup"><span data-stu-id="b56d8-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b56d8-119">-Enabled</span></span>
<span data-ttu-id="b56d8-120">Indica se WAF è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b56d8-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="b56d8-121">-FirewallMode</span></span>
<span data-ttu-id="b56d8-122">Specifica la modalità firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="b56d8-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="b56d8-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b56d8-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b56d8-124">Rilevamento</span><span class="sxs-lookup"><span data-stu-id="b56d8-124">Detection</span></span>
- <span data-ttu-id="b56d8-125">Prevenzione</span><span class="sxs-lookup"><span data-stu-id="b56d8-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="b56d8-126">-RuleSetType</span></span>
<span data-ttu-id="b56d8-127">Tipo del set di regole del firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="b56d8-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="b56d8-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b56d8-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="b56d8-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="b56d8-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="b56d8-130">-RuleSetVersion</span></span>
<span data-ttu-id="b56d8-131">Versione del tipo di set di regole.</span><span class="sxs-lookup"><span data-stu-id="b56d8-131">The version of the rule set type.</span></span>
<span data-ttu-id="b56d8-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b56d8-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="b56d8-133">3,0</span><span class="sxs-lookup"><span data-stu-id="b56d8-133">3.0</span></span>
- <span data-ttu-id="b56d8-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="b56d8-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b56d8-135">-Confirm</span></span>
<span data-ttu-id="b56d8-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b56d8-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b56d8-137">-WhatIf</span></span>
<span data-ttu-id="b56d8-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b56d8-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b56d8-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b56d8-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56d8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56d8-140">CommonParameters</span></span>
<span data-ttu-id="b56d8-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b56d8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56d8-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56d8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56d8-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b56d8-143">INPUTS</span></span>

### <span data-ttu-id="b56d8-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b56d8-144">None</span></span>
<span data-ttu-id="b56d8-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b56d8-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b56d8-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b56d8-146">OUTPUTS</span></span>

### <span data-ttu-id="b56d8-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b56d8-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="b56d8-148">Note</span><span class="sxs-lookup"><span data-stu-id="b56d8-148">NOTES</span></span>

## <span data-ttu-id="b56d8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b56d8-149">RELATED LINKS</span></span>

[<span data-ttu-id="b56d8-150">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b56d8-150">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="b56d8-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b56d8-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

