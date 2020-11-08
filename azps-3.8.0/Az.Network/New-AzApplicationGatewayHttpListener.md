---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022757"
---
# <span data-ttu-id="80ea2-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="80ea2-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="80ea2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80ea2-102">SYNOPSIS</span></span>
<span data-ttu-id="80ea2-103">Crea un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80ea2-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="80ea2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80ea2-104">SYNTAX</span></span>

### <span data-ttu-id="80ea2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="80ea2-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80ea2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="80ea2-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80ea2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80ea2-107">DESCRIPTION</span></span>
<span data-ttu-id="80ea2-108">Il cmdlet **New-AzApplicationGatewayHttpListener** crea un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="80ea2-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="80ea2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80ea2-109">EXAMPLES</span></span>

### <span data-ttu-id="80ea2-110">Esempio 1: creare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="80ea2-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="80ea2-111">Questo comando crea un listener HTTP denominato Listener01 e archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="80ea2-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="80ea2-112">Esempio 2: creare un listener HTTP con SSL</span><span class="sxs-lookup"><span data-stu-id="80ea2-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="80ea2-113">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="80ea2-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="80ea2-114">Il comando Archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="80ea2-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="80ea2-115">Esempio 3: creare un listener HTTP con Firewall-Policy</span><span class="sxs-lookup"><span data-stu-id="80ea2-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="80ea2-116">Questo comando crea un listener HTTP denominato Listener01, FirewallPolicy come $firewallPolicy e archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="80ea2-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="80ea2-117">Esempio 4: aggiungere un listener HTTPS con SSL e nomi host</span><span class="sxs-lookup"><span data-stu-id="80ea2-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="80ea2-118">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01 insieme a due nomi host.</span><span class="sxs-lookup"><span data-stu-id="80ea2-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="80ea2-119">Il comando Archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="80ea2-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="80ea2-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80ea2-120">PARAMETERS</span></span>

### <span data-ttu-id="80ea2-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="80ea2-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="80ea2-122">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="80ea2-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ea2-123">-DefaultProfile</span></span>
<span data-ttu-id="80ea2-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80ea2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ea2-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="80ea2-125">-FirewallPolicy</span></span>
<span data-ttu-id="80ea2-126">Specifica il riferimento all'oggetto a un criterio firewall di primo livello.</span><span class="sxs-lookup"><span data-stu-id="80ea2-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="80ea2-127">Il riferimento all'oggetto può essere creato usando il cmdlet New-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="80ea2-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="80ea2-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" un criterio firewall creato usando il unifiedgroup precedente può essere riferito a un livello di regola di percorso.</span><span class="sxs-lookup"><span data-stu-id="80ea2-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="80ea2-129">sopra il comando creerebbe le impostazioni dei criteri e le regole gestite predefinite.</span><span class="sxs-lookup"><span data-stu-id="80ea2-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="80ea2-130">Invece dei valori predefiniti, gli utenti possono specificare PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="80ea2-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="80ea2-131">-FirewallPolicyId</span></span>
<span data-ttu-id="80ea2-132">Specifica l'ID di una risorsa di firewall applicazione Web di primo livello esistente.</span><span class="sxs-lookup"><span data-stu-id="80ea2-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="80ea2-133">Gli ID dei criteri del firewall possono essere restituiti tramite il cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="80ea2-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="80ea2-134">Dopo aver ottenuto l'ID, puoi usare il parametro *FirewallPolicyId* invece del parametro *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="80ea2-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="80ea2-135">Ad esempio:-FirewallPolicyId/subscriptions/<Subscription-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="80ea2-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80ea2-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="80ea2-137">Specifica l'oggetto di configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="80ea2-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="80ea2-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="80ea2-139">Specifica l'ID della configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="80ea2-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="80ea2-140">-FrontendPort</span></span>
<span data-ttu-id="80ea2-141">Specifica la porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="80ea2-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="80ea2-142">-FrontendPortId</span></span>
<span data-ttu-id="80ea2-143">Specifica l'ID dell'oggetto porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="80ea2-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="80ea2-144">-HostName</span></span>
<span data-ttu-id="80ea2-145">Specifica il nome host del listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80ea2-145">Specifies the host name of the application gateway HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-146">-HostName</span><span class="sxs-lookup"><span data-stu-id="80ea2-146">-HostNames</span></span>
<span data-ttu-id="80ea2-147">Nomi host</span><span class="sxs-lookup"><span data-stu-id="80ea2-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="80ea2-148">-Name</span></span>
<span data-ttu-id="80ea2-149">Specifica il nome del listener HTTP creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80ea2-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-150">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="80ea2-150">-Protocol</span></span>
<span data-ttu-id="80ea2-151">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="80ea2-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="80ea2-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="80ea2-153">-SslCertificate</span></span>
<span data-ttu-id="80ea2-154">Specifica l'oggetto certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="80ea2-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="80ea2-155">-SslCertificateId</span></span>
<span data-ttu-id="80ea2-156">Specifica l'ID del certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="80ea2-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ea2-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ea2-157">CommonParameters</span></span>
<span data-ttu-id="80ea2-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ea2-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ea2-159">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ea2-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ea2-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80ea2-160">INPUTS</span></span>

### <span data-ttu-id="80ea2-161">Nessuno</span><span class="sxs-lookup"><span data-stu-id="80ea2-161">None</span></span>

## <span data-ttu-id="80ea2-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80ea2-162">OUTPUTS</span></span>

### <span data-ttu-id="80ea2-163">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="80ea2-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="80ea2-164">Note</span><span class="sxs-lookup"><span data-stu-id="80ea2-164">NOTES</span></span>

## <span data-ttu-id="80ea2-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80ea2-165">RELATED LINKS</span></span>

[<span data-ttu-id="80ea2-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="80ea2-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="80ea2-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="80ea2-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="80ea2-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="80ea2-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="80ea2-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="80ea2-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


