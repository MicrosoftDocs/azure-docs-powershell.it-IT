---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: a5f60588a0db848d0b96aa0611b8647142db2b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677986"
---
# <span data-ttu-id="19f29-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f29-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="19f29-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19f29-102">SYNOPSIS</span></span>
<span data-ttu-id="19f29-103">Modifica la configurazione WAF di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19f29-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="19f29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19f29-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19f29-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19f29-105">DESCRIPTION</span></span>
<span data-ttu-id="19f29-106">Il cmdlet **set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione WAF (Web Application Firewall) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19f29-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="19f29-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19f29-107">EXAMPLES</span></span>

### <span data-ttu-id="19f29-108">Esempio 1: aggiornare la configurazione del firewall applicazione Web gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="19f29-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="19f29-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="19f29-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="19f29-110">Il secondo comando Abilita la configurazione del firewall per il gateway dell'applicazione archiviata in $AppGw e imposta la modalità firewall su "Detection", RuleSetType su "OWASP" e RuleSetVersion su "3,0".</span><span class="sxs-lookup"><span data-stu-id="19f29-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="19f29-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19f29-111">PARAMETERS</span></span>

### <span data-ttu-id="19f29-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f29-112">-ApplicationGateway</span></span>
<span data-ttu-id="19f29-113">Specifica un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19f29-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="19f29-114">Puoi usare il cmdlet Get-AzApplicationGateway per ottenere un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19f29-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19f29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19f29-115">-DefaultProfile</span></span>
<span data-ttu-id="19f29-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19f29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19f29-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="19f29-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="19f29-118">Gruppi di regole disabilitati.</span><span class="sxs-lookup"><span data-stu-id="19f29-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="19f29-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="19f29-119">-Enabled</span></span>
<span data-ttu-id="19f29-120">Indica se il firewall applicazione Web è abilitato.</span><span class="sxs-lookup"><span data-stu-id="19f29-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="19f29-121">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="19f29-121">-Exclusion</span></span>
<span data-ttu-id="19f29-122">Elenchi di esclusione.</span><span class="sxs-lookup"><span data-stu-id="19f29-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="19f29-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="19f29-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="19f29-124">Limite massimo per il caricamento di file in MB.</span><span class="sxs-lookup"><span data-stu-id="19f29-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="19f29-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="19f29-125">-FirewallMode</span></span>
<span data-ttu-id="19f29-126">Specifica la modalità firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="19f29-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="19f29-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="19f29-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19f29-128">Rilevamento</span><span class="sxs-lookup"><span data-stu-id="19f29-128">Detection</span></span>
- <span data-ttu-id="19f29-129">Prevenzione</span><span class="sxs-lookup"><span data-stu-id="19f29-129">Prevention</span></span>

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

### <span data-ttu-id="19f29-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="19f29-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="19f29-131">Dimensioni massime della richiesta in KB.</span><span class="sxs-lookup"><span data-stu-id="19f29-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="19f29-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="19f29-132">-RequestBodyCheck</span></span>
<span data-ttu-id="19f29-133">Se il corpo della richiesta è selezionato o meno.</span><span class="sxs-lookup"><span data-stu-id="19f29-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="19f29-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="19f29-134">-RuleSetType</span></span>
<span data-ttu-id="19f29-135">Tipo del set di regole del firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="19f29-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="19f29-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="19f29-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="19f29-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="19f29-137">OWASP</span></span>

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

### <span data-ttu-id="19f29-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="19f29-138">-RuleSetVersion</span></span>
<span data-ttu-id="19f29-139">Versione del tipo di set di regole.</span><span class="sxs-lookup"><span data-stu-id="19f29-139">The version of the rule set type.</span></span>
<span data-ttu-id="19f29-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="19f29-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="19f29-141">3,0</span><span class="sxs-lookup"><span data-stu-id="19f29-141">3.0</span></span>
- <span data-ttu-id="19f29-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="19f29-142">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f29-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19f29-143">-Confirm</span></span>
<span data-ttu-id="19f29-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19f29-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19f29-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19f29-145">-WhatIf</span></span>
<span data-ttu-id="19f29-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19f29-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19f29-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19f29-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19f29-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f29-148">CommonParameters</span></span>
<span data-ttu-id="19f29-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19f29-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f29-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f29-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f29-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19f29-151">INPUTS</span></span>

### <span data-ttu-id="19f29-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f29-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19f29-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19f29-153">OUTPUTS</span></span>

### <span data-ttu-id="19f29-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f29-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="19f29-155">Note</span><span class="sxs-lookup"><span data-stu-id="19f29-155">NOTES</span></span>

## <span data-ttu-id="19f29-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19f29-156">RELATED LINKS</span></span>

[<span data-ttu-id="19f29-157">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="19f29-157">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="19f29-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f29-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="19f29-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="19f29-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


