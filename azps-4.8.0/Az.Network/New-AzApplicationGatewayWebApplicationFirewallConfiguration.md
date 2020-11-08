---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192823"
---
# <span data-ttu-id="9aaaa-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9aaaa-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="9aaaa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9aaaa-102">SYNOPSIS</span></span>
<span data-ttu-id="9aaaa-103">Crea una configurazione WAF per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="9aaaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9aaaa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aaaa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aaaa-105">DESCRIPTION</span></span>
<span data-ttu-id="9aaaa-106">Il cmdlet **New-AzApplicationGatewayWebApplicationFirewallConfiguration** crea una configurazione WAF (Web Application Firewall) per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="9aaaa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9aaaa-107">EXAMPLES</span></span>

### <span data-ttu-id="9aaaa-108">Esempio 1: creare una configurazione firewall applicazione Web per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9aaaa-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="9aaaa-109">Il primo comando crea una nuova configurazione del gruppo di regole disabilitata per il gruppo di regole denominato "REQUEST-942-APPLICATION-ATTACK-SQLI" con la regola 942130 e la regola 942140 disabilitata.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="9aaaa-110">Il secondo comando crea un'altra configurazione del gruppo di regole disabilitata per un gruppo di regole denominato "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="9aaaa-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="9aaaa-111">Nessuna regola viene approvata in modo specifico e quindi tutte le regole del gruppo di regole verranno disabilitate.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="9aaaa-112">L'ultimo comando crea quindi una configurazione WAF con le regole del firewall disabilitate come configurate in $disabledRuleGroup 1 e $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="9aaaa-113">La nuova configurazione di WAF viene archiviata nella variabile $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="9aaaa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9aaaa-114">PARAMETERS</span></span>

### <span data-ttu-id="9aaaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aaaa-115">-DefaultProfile</span></span>
<span data-ttu-id="9aaaa-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aaaa-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="9aaaa-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="9aaaa-118">Gruppi di regole disabilitati.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9aaaa-119">-Enabled</span></span>
<span data-ttu-id="9aaaa-120">Indica se WAF è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-121">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="9aaaa-121">-Exclusion</span></span>
<span data-ttu-id="9aaaa-122">Elenchi di esclusione.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="9aaaa-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="9aaaa-124">Limite massimo per il caricamento di file in MB.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="9aaaa-125">-FirewallMode</span></span>
<span data-ttu-id="9aaaa-126">Specifica la modalità firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="9aaaa-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9aaaa-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9aaaa-128">Rilevamento</span><span class="sxs-lookup"><span data-stu-id="9aaaa-128">Detection</span></span>
- <span data-ttu-id="9aaaa-129">Prevenzione</span><span class="sxs-lookup"><span data-stu-id="9aaaa-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="9aaaa-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="9aaaa-131">Dimensioni massime della richiesta in KB.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="9aaaa-132">-RequestBodyCheck</span></span>
<span data-ttu-id="9aaaa-133">Se il corpo della richiesta è selezionato o meno.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="9aaaa-134">-RuleSetType</span></span>
<span data-ttu-id="9aaaa-135">Tipo del set di regole del firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="9aaaa-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9aaaa-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="9aaaa-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="9aaaa-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="9aaaa-138">-RuleSetVersion</span></span>
<span data-ttu-id="9aaaa-139">Versione del tipo di set di regole.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9aaaa-140">-Confirm</span></span>
<span data-ttu-id="9aaaa-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aaaa-142">-WhatIf</span></span>
<span data-ttu-id="9aaaa-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9aaaa-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aaaa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aaaa-145">CommonParameters</span></span>
<span data-ttu-id="9aaaa-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aaaa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aaaa-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aaaa-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aaaa-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9aaaa-148">INPUTS</span></span>

### <span data-ttu-id="9aaaa-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9aaaa-149">None</span></span>

## <span data-ttu-id="9aaaa-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9aaaa-150">OUTPUTS</span></span>

### <span data-ttu-id="9aaaa-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9aaaa-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="9aaaa-152">Note</span><span class="sxs-lookup"><span data-stu-id="9aaaa-152">NOTES</span></span>

## <span data-ttu-id="9aaaa-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9aaaa-153">RELATED LINKS</span></span>

[<span data-ttu-id="9aaaa-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9aaaa-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="9aaaa-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9aaaa-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

