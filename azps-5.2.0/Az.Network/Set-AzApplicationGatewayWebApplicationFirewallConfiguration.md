---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9b5e618fc4b4be02614d872bfa5bcdabd2b0fec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343552"
---
# <span data-ttu-id="ca09b-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca09b-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ca09b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca09b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca09b-103">Modifica la configurazione WAF di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca09b-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="ca09b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca09b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca09b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca09b-105">DESCRIPTION</span></span>
<span data-ttu-id="ca09b-106">Il cmdlet **set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione WAF (Web Application Firewall) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca09b-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="ca09b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca09b-107">EXAMPLES</span></span>

### <span data-ttu-id="ca09b-108">Esempio 1: aggiornare la configurazione del firewall applicazione Web gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ca09b-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="ca09b-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ca09b-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ca09b-110">Il secondo comando Abilita la configurazione del firewall per il gateway dell'applicazione archiviata in $AppGw e imposta la modalità firewall su "Detection", RuleSetType su "OWASP" e RuleSetVersion su "3,0".</span><span class="sxs-lookup"><span data-stu-id="ca09b-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="ca09b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca09b-111">PARAMETERS</span></span>

### <span data-ttu-id="ca09b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca09b-112">-ApplicationGateway</span></span>
<span data-ttu-id="ca09b-113">Specifica un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca09b-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="ca09b-114">Puoi usare il cmdlet Get-AzApplicationGateway per ottenere un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca09b-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="ca09b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca09b-115">-DefaultProfile</span></span>
<span data-ttu-id="ca09b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca09b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca09b-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="ca09b-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="ca09b-118">Gruppi di regole disabilitati.</span><span class="sxs-lookup"><span data-stu-id="ca09b-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="ca09b-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="ca09b-119">-Enabled</span></span>
<span data-ttu-id="ca09b-120">Indica se il firewall applicazione Web è abilitato.</span><span class="sxs-lookup"><span data-stu-id="ca09b-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="ca09b-121">-Esclusione</span><span class="sxs-lookup"><span data-stu-id="ca09b-121">-Exclusion</span></span>
<span data-ttu-id="ca09b-122">Elenchi di esclusione.</span><span class="sxs-lookup"><span data-stu-id="ca09b-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="ca09b-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="ca09b-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="ca09b-124">Limite massimo per il caricamento di file in MB.</span><span class="sxs-lookup"><span data-stu-id="ca09b-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="ca09b-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="ca09b-125">-FirewallMode</span></span>
<span data-ttu-id="ca09b-126">Specifica la modalità firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="ca09b-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="ca09b-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca09b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca09b-128">Rilevamento</span><span class="sxs-lookup"><span data-stu-id="ca09b-128">Detection</span></span>
- <span data-ttu-id="ca09b-129">Prevenzione</span><span class="sxs-lookup"><span data-stu-id="ca09b-129">Prevention</span></span>

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

### <span data-ttu-id="ca09b-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="ca09b-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="ca09b-131">Dimensioni massime della richiesta in KB.</span><span class="sxs-lookup"><span data-stu-id="ca09b-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="ca09b-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="ca09b-132">-RequestBodyCheck</span></span>
<span data-ttu-id="ca09b-133">Se il corpo della richiesta è selezionato o meno.</span><span class="sxs-lookup"><span data-stu-id="ca09b-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="ca09b-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="ca09b-134">-RuleSetType</span></span>
<span data-ttu-id="ca09b-135">Tipo del set di regole del firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="ca09b-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="ca09b-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca09b-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="ca09b-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="ca09b-137">OWASP</span></span>

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

### <span data-ttu-id="ca09b-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="ca09b-138">-RuleSetVersion</span></span>
<span data-ttu-id="ca09b-139">Versione del tipo di set di regole.</span><span class="sxs-lookup"><span data-stu-id="ca09b-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="ca09b-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca09b-140">-Confirm</span></span>
<span data-ttu-id="ca09b-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca09b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca09b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca09b-142">-WhatIf</span></span>
<span data-ttu-id="ca09b-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca09b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca09b-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca09b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca09b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca09b-145">CommonParameters</span></span>
<span data-ttu-id="ca09b-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca09b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca09b-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca09b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca09b-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca09b-148">INPUTS</span></span>

### <span data-ttu-id="ca09b-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca09b-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ca09b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca09b-150">OUTPUTS</span></span>

### <span data-ttu-id="ca09b-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca09b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ca09b-152">Note</span><span class="sxs-lookup"><span data-stu-id="ca09b-152">NOTES</span></span>

## <span data-ttu-id="ca09b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca09b-153">RELATED LINKS</span></span>

[<span data-ttu-id="ca09b-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca09b-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ca09b-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca09b-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ca09b-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca09b-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


