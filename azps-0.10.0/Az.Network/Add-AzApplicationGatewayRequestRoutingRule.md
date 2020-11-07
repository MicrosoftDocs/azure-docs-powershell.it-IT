---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 32695204a153d04643063f4d991b577e619edcea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861006"
---
# <span data-ttu-id="afe75-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="afe75-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="afe75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afe75-102">SYNOPSIS</span></span>
<span data-ttu-id="afe75-103">Aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="afe75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afe75-104">SYNTAX</span></span>

### <span data-ttu-id="afe75-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="afe75-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afe75-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="afe75-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afe75-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afe75-107">DESCRIPTION</span></span>
<span data-ttu-id="afe75-108">Il cmdlet **Add-AzApplicationGatewayRequestRoutingRule** aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="afe75-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afe75-109">EXAMPLES</span></span>

### <span data-ttu-id="afe75-110">Esempio 1: aggiungere una regola di routing delle richieste a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="afe75-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="afe75-111">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="afe75-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="afe75-112">Il secondo comando aggiunge la regola di routing delle richieste al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="afe75-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afe75-113">PARAMETERS</span></span>

### <span data-ttu-id="afe75-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afe75-114">-ApplicationGateway</span></span>
<span data-ttu-id="afe75-115">Specifica un gateway dell'applicazione a cui questo cmdlet aggiunge una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="afe75-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="afe75-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="afe75-116">-BackendAddressPool</span></span>
<span data-ttu-id="afe75-117">Specifica un oggetto pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="afe75-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="afe75-119">Specifica un ID del pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="afe75-120">-BackendHttpSettings</span></span>
<span data-ttu-id="afe75-121">Specifica un oggetto impostazioni HTTP back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="afe75-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="afe75-123">Specifica un ID di impostazioni HTTP di backend per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe75-124">-DefaultProfile</span></span>
<span data-ttu-id="afe75-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afe75-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afe75-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="afe75-126">-HttpListener</span></span>
<span data-ttu-id="afe75-127">Specifica l'oggetto listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="afe75-128">-HttpListenerId</span></span>
<span data-ttu-id="afe75-129">Specifica l'ID listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afe75-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="afe75-130">-Name</span></span>
<span data-ttu-id="afe75-131">Specifica il nome della regola di routing della richiesta aggiunta dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afe75-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="afe75-132">-RedirectConfiguration</span></span>
<span data-ttu-id="afe75-133">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="afe75-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="afe75-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="afe75-135">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="afe75-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="afe75-136">-RuleType</span></span>
<span data-ttu-id="afe75-137">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="afe75-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="afe75-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="afe75-139">-UrlPathMapId</span></span>
<span data-ttu-id="afe75-140">Specifica l'ID Mappa percorso URL per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="afe75-140">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afe75-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe75-141">CommonParameters</span></span>
<span data-ttu-id="afe75-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afe75-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe75-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afe75-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe75-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afe75-144">INPUTS</span></span>

### <span data-ttu-id="afe75-145">System. String</span><span class="sxs-lookup"><span data-stu-id="afe75-145">System.String</span></span>

## <span data-ttu-id="afe75-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afe75-146">OUTPUTS</span></span>

### <span data-ttu-id="afe75-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afe75-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="afe75-148">Note</span><span class="sxs-lookup"><span data-stu-id="afe75-148">NOTES</span></span>

## <span data-ttu-id="afe75-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afe75-149">RELATED LINKS</span></span>

[<span data-ttu-id="afe75-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="afe75-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="afe75-151">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="afe75-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="afe75-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="afe75-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="afe75-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="afe75-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


