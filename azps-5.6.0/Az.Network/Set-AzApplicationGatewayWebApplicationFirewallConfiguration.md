---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 95d0e82609c2cb8bfcbbfcf57d1354d219da9f9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995300"
---
# <span data-ttu-id="79251-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="79251-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="79251-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79251-102">SYNOPSIS</span></span>
<span data-ttu-id="79251-103">Modifica la configurazione WAF di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="79251-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="79251-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79251-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79251-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79251-105">DESCRIPTION</span></span>
<span data-ttu-id="79251-106">Il cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione del firewall dell'applicazione Web (WAF) di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="79251-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="79251-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79251-107">EXAMPLES</span></span>

### <span data-ttu-id="79251-108">Esempio 1: Aggiornare la configurazione firewall dell'applicazione Web del Gateway applicazioni Web</span><span class="sxs-lookup"><span data-stu-id="79251-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="79251-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e quindi lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="79251-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="79251-110">Il secondo comando abilita la configurazione del firewall per il gateway applicazione archiviato in $AppGw e imposta la modalità del firewall su "Rilevamento", RuleSetType su "OWASP" e RuleSetVersion su "3.0".</span><span class="sxs-lookup"><span data-stu-id="79251-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="79251-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79251-111">PARAMETERS</span></span>

### <span data-ttu-id="79251-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79251-112">-ApplicationGateway</span></span>
<span data-ttu-id="79251-113">Specifica un oggetto gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="79251-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="79251-114">È possibile usare il cmdlet Get-AzApplicationGateway per ottenere un oggetto gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="79251-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="79251-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79251-115">-DefaultProfile</span></span>
<span data-ttu-id="79251-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79251-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79251-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="79251-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="79251-118">Gruppi di regole disabilitati.</span><span class="sxs-lookup"><span data-stu-id="79251-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="79251-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="79251-119">-Enabled</span></span>
<span data-ttu-id="79251-120">Indica se il firewall dell'applicazione Web è abilitato.</span><span class="sxs-lookup"><span data-stu-id="79251-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="79251-121">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="79251-121">-Exclusion</span></span>
<span data-ttu-id="79251-122">Elenchi di esclusione.</span><span class="sxs-lookup"><span data-stu-id="79251-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="79251-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="79251-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="79251-124">Limite massimo di caricamento dei file in MB.</span><span class="sxs-lookup"><span data-stu-id="79251-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="79251-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="79251-125">-FirewallMode</span></span>
<span data-ttu-id="79251-126">Specifica la modalità firewall dell'applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="79251-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="79251-127">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="79251-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79251-128">Rilevamento</span><span class="sxs-lookup"><span data-stu-id="79251-128">Detection</span></span>
- <span data-ttu-id="79251-129">Prevenzione</span><span class="sxs-lookup"><span data-stu-id="79251-129">Prevention</span></span>

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

### <span data-ttu-id="79251-130">-MaxRequest UnaRidimensionaInKb</span><span class="sxs-lookup"><span data-stu-id="79251-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="79251-131">Dimensioni massime del corpo della richiesta in KB.</span><span class="sxs-lookup"><span data-stu-id="79251-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="79251-132">-RequestCheckCheck</span><span class="sxs-lookup"><span data-stu-id="79251-132">-RequestBodyCheck</span></span>
<span data-ttu-id="79251-133">Se il corpo della richiesta è selezionato o meno.</span><span class="sxs-lookup"><span data-stu-id="79251-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="79251-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="79251-134">-RuleSetType</span></span>
<span data-ttu-id="79251-135">Il tipo di set di regole firewall dell'applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="79251-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="79251-136">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="79251-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="79251-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="79251-137">OWASP</span></span>

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

### <span data-ttu-id="79251-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="79251-138">-RuleSetVersion</span></span>
<span data-ttu-id="79251-139">Versione del tipo di set di regole.</span><span class="sxs-lookup"><span data-stu-id="79251-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="79251-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79251-140">-Confirm</span></span>
<span data-ttu-id="79251-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79251-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79251-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79251-142">-WhatIf</span></span>
<span data-ttu-id="79251-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79251-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79251-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79251-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79251-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79251-145">CommonParameters</span></span>
<span data-ttu-id="79251-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79251-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79251-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79251-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79251-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="79251-148">INPUTS</span></span>

### <span data-ttu-id="79251-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79251-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79251-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79251-150">OUTPUTS</span></span>

### <span data-ttu-id="79251-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79251-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="79251-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="79251-152">NOTES</span></span>

## <span data-ttu-id="79251-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79251-153">RELATED LINKS</span></span>

[<span data-ttu-id="79251-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="79251-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="79251-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="79251-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="79251-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="79251-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


