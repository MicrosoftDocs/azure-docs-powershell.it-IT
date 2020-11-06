---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9da7a3d77c0a5f9b9dec44ee1224a66be79a1772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512531"
---
# <span data-ttu-id="e2326-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2326-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e2326-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2326-102">SYNOPSIS</span></span>
<span data-ttu-id="e2326-103">Modifica la configurazione WAF di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e2326-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2326-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2326-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2326-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2326-105">DESCRIPTION</span></span>
<span data-ttu-id="e2326-106">Il cmdlet **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modifica la configurazione WAF (Web Application Firewall) di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e2326-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="e2326-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2326-107">EXAMPLES</span></span>

### <span data-ttu-id="e2326-108">Esempio 1: aggiornare la configurazione del firewall applicazione Web gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="e2326-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="e2326-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e2326-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e2326-110">Il secondo comando Abilita la configurazione del firewall per il gateway dell'applicazione archiviata in $AppGw e imposta la modalità firewall su "Detection", RuleSetType su "OWASP" e RuleSetVersion su "3,0".</span><span class="sxs-lookup"><span data-stu-id="e2326-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="e2326-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2326-111">PARAMETERS</span></span>

### <span data-ttu-id="e2326-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2326-112">-ApplicationGateway</span></span>
<span data-ttu-id="e2326-113">Specifica un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e2326-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="e2326-114">Puoi usare il cmdlet Get-AzureRmApplicationGateway per ottenere un oggetto gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e2326-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2326-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2326-115">-DefaultProfile</span></span>
<span data-ttu-id="e2326-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2326-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2326-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="e2326-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="e2326-118">Gruppi di regole disabilitati.</span><span class="sxs-lookup"><span data-stu-id="e2326-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="e2326-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e2326-119">-Enabled</span></span>
<span data-ttu-id="e2326-120">Indica se il firewall applicazione Web è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e2326-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="e2326-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="e2326-121">-FirewallMode</span></span>
<span data-ttu-id="e2326-122">Specifica la modalità firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="e2326-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="e2326-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2326-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2326-124">Rilevamento</span><span class="sxs-lookup"><span data-stu-id="e2326-124">Detection</span></span>
- <span data-ttu-id="e2326-125">Prevenzione</span><span class="sxs-lookup"><span data-stu-id="e2326-125">Prevention</span></span>

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

### <span data-ttu-id="e2326-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="e2326-126">-RuleSetType</span></span>
<span data-ttu-id="e2326-127">Tipo del set di regole del firewall applicazione Web.</span><span class="sxs-lookup"><span data-stu-id="e2326-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="e2326-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2326-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="e2326-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="e2326-129">OWASP</span></span>

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

### <span data-ttu-id="e2326-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="e2326-130">-RuleSetVersion</span></span>
<span data-ttu-id="e2326-131">Versione del tipo di set di regole.</span><span class="sxs-lookup"><span data-stu-id="e2326-131">The version of the rule set type.</span></span>
<span data-ttu-id="e2326-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2326-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="e2326-133">3,0</span><span class="sxs-lookup"><span data-stu-id="e2326-133">3.0</span></span>
- <span data-ttu-id="e2326-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="e2326-134">2.2.9</span></span>

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

### <span data-ttu-id="e2326-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2326-135">-Confirm</span></span>
<span data-ttu-id="e2326-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2326-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2326-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2326-137">-WhatIf</span></span>
<span data-ttu-id="e2326-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2326-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2326-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2326-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2326-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2326-140">CommonParameters</span></span>
<span data-ttu-id="e2326-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2326-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2326-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2326-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2326-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2326-143">INPUTS</span></span>

### <span data-ttu-id="e2326-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2326-144">PSApplicationGateway</span></span>
<span data-ttu-id="e2326-145">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e2326-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e2326-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2326-146">OUTPUTS</span></span>

### <span data-ttu-id="e2326-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2326-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2326-148">Note</span><span class="sxs-lookup"><span data-stu-id="e2326-148">NOTES</span></span>

## <span data-ttu-id="e2326-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2326-149">RELATED LINKS</span></span>

[<span data-ttu-id="e2326-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2326-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e2326-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2326-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e2326-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2326-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

