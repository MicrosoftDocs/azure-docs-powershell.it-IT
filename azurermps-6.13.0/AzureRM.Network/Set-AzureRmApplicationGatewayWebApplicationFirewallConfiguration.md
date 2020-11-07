---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 3b2de5d139c8addb448ac76609e13becf2e0153c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685423"
---
# <span data-ttu-id="f9822-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9822-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f9822-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9822-102">SYNOPSIS</span></span>
<span data-ttu-id="f9822-103">Modifica la configurazione WAF di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9822-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9822-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9822-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-RequestBodyCheck <Boolean>] [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9822-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9822-105">DESCRIPTION</span></span>
<span data-ttu-id="f9822-106">Il cmdlet **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione WAF (Web Application Firewall) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9822-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="f9822-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9822-107">EXAMPLES</span></span>

### <span data-ttu-id="f9822-108">Esempio 1: aggiornare la configurazione del firewall applicazione Web gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f9822-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="f9822-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f9822-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f9822-110">Il secondo comando Abilita la configurazione del firewall per il gateway dell'applicazione archiviata in $AppGw e imposta la modalità firewall su "Detection", RuleSetType su "OWASP" e RuleSetVersion su "3,0".</span><span class="sxs-lookup"><span data-stu-id="f9822-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="f9822-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9822-111">PARAMETERS</span></span>

### <span data-ttu-id="f9822-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9822-112">-ApplicationGateway</span></span>
<span data-ttu-id="f9822-113">Specifica un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9822-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="f9822-114">Puoi usare il cmdlet Get-AzureRmApplicationGateway per ottenere un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9822-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="f9822-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9822-115">-DefaultProfile</span></span>
<span data-ttu-id="f9822-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9822-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9822-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="f9822-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="f9822-118">Gruppi di regole disabilitati.</span><span class="sxs-lookup"><span data-stu-id="f9822-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9822-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="f9822-119">-Enabled</span></span>
<span data-ttu-id="f9822-120">Indica se il firewall applicazione Web è abilitato.</span><span class="sxs-lookup"><span data-stu-id="f9822-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="f9822-121">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="f9822-121">-Exclusion</span></span>
<span data-ttu-id="f9822-122">Elenchi di esclusione.</span><span class="sxs-lookup"><span data-stu-id="f9822-122">The exclusion lists.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9822-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="f9822-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="f9822-124">Limite massimo per il caricamento di file in MB.</span><span class="sxs-lookup"><span data-stu-id="f9822-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="f9822-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="f9822-125">-FirewallMode</span></span>
<span data-ttu-id="f9822-126">Specifica la modalità firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="f9822-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="f9822-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9822-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9822-128">Rilevamento</span><span class="sxs-lookup"><span data-stu-id="f9822-128">Detection</span></span>
- <span data-ttu-id="f9822-129">Prevenzione</span><span class="sxs-lookup"><span data-stu-id="f9822-129">Prevention</span></span>

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

### <span data-ttu-id="f9822-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="f9822-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="f9822-131">Dimensioni massime della richiesta in KB.</span><span class="sxs-lookup"><span data-stu-id="f9822-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="f9822-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="f9822-132">-RequestBodyCheck</span></span>
<span data-ttu-id="f9822-133">Se il corpo della richiesta è selezionato o meno.</span><span class="sxs-lookup"><span data-stu-id="f9822-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="f9822-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="f9822-134">-RuleSetType</span></span>
<span data-ttu-id="f9822-135">Tipo del set di regole del firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="f9822-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="f9822-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9822-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="f9822-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="f9822-137">OWASP</span></span>

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

### <span data-ttu-id="f9822-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="f9822-138">-RuleSetVersion</span></span>
<span data-ttu-id="f9822-139">Versione del tipo di set di regole.</span><span class="sxs-lookup"><span data-stu-id="f9822-139">The version of the rule set type.</span></span>
<span data-ttu-id="f9822-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9822-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="f9822-141">3,0</span><span class="sxs-lookup"><span data-stu-id="f9822-141">3.0</span></span>
- <span data-ttu-id="f9822-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="f9822-142">2.2.9</span></span>

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

### <span data-ttu-id="f9822-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9822-143">-Confirm</span></span>
<span data-ttu-id="f9822-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9822-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9822-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9822-145">-WhatIf</span></span>
<span data-ttu-id="f9822-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9822-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9822-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9822-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9822-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9822-148">CommonParameters</span></span>
<span data-ttu-id="f9822-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9822-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9822-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9822-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9822-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9822-151">INPUTS</span></span>

### <span data-ttu-id="f9822-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9822-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f9822-153">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f9822-153">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f9822-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9822-154">OUTPUTS</span></span>

### <span data-ttu-id="f9822-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9822-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f9822-156">Note</span><span class="sxs-lookup"><span data-stu-id="f9822-156">NOTES</span></span>

## <span data-ttu-id="f9822-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9822-157">RELATED LINKS</span></span>

[<span data-ttu-id="f9822-158">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9822-158">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f9822-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9822-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f9822-160">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9822-160">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

