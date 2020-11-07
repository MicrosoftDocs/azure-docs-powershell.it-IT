---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: fdbbb28d69d5094b52d8ac7340839fa570bce55d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865921"
---
# <span data-ttu-id="bad19-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bad19-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="bad19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bad19-102">SYNOPSIS</span></span>
<span data-ttu-id="bad19-103">Aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bad19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bad19-104">SYNTAX</span></span>

### <span data-ttu-id="bad19-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bad19-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bad19-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bad19-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bad19-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bad19-107">DESCRIPTION</span></span>
<span data-ttu-id="bad19-108">Il cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** aggiunge una regola di routing delle richieste a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="bad19-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bad19-109">EXAMPLES</span></span>

### <span data-ttu-id="bad19-110">Esempio 1: aggiungere una regola di routing delle richieste a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="bad19-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="bad19-111">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bad19-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bad19-112">Il secondo comando aggiunge la regola di routing delle richieste al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="bad19-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bad19-113">PARAMETERS</span></span>

### <span data-ttu-id="bad19-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bad19-114">-ApplicationGateway</span></span>
<span data-ttu-id="bad19-115">Specifica un gateway dell'applicazione a cui questo cmdlet aggiunge una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="bad19-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="bad19-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bad19-116">-BackendAddressPool</span></span>
<span data-ttu-id="bad19-117">Specifica un oggetto pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="bad19-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bad19-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="bad19-119">Specifica un ID del pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="bad19-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bad19-120">-BackendHttpSettings</span></span>
<span data-ttu-id="bad19-121">Specifica un oggetto impostazioni HTTP back-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="bad19-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="bad19-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="bad19-123">Specifica un ID di impostazioni HTTP di backend per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="bad19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad19-124">-DefaultProfile</span></span>
<span data-ttu-id="bad19-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bad19-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bad19-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="bad19-126">-HttpListener</span></span>
<span data-ttu-id="bad19-127">Specifica l'oggetto listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="bad19-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="bad19-128">-HttpListenerId</span></span>
<span data-ttu-id="bad19-129">Specifica l'ID listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bad19-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="bad19-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="bad19-130">-Name</span></span>
<span data-ttu-id="bad19-131">Specifica il nome della regola di routing della richiesta aggiunta dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bad19-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="bad19-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bad19-132">-RedirectConfiguration</span></span>
<span data-ttu-id="bad19-133">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bad19-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="bad19-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bad19-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="bad19-135">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bad19-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="bad19-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="bad19-136">-RuleType</span></span>
<span data-ttu-id="bad19-137">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="bad19-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="bad19-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="bad19-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="bad19-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="bad19-139">-UrlPathMapId</span></span>
<span data-ttu-id="bad19-140">Specifica l'ID Mappa percorso URL per la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="bad19-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="bad19-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad19-141">CommonParameters</span></span>
<span data-ttu-id="bad19-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bad19-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad19-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad19-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad19-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bad19-144">INPUTS</span></span>

### <span data-ttu-id="bad19-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bad19-145">System.String</span></span>

## <span data-ttu-id="bad19-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bad19-146">OUTPUTS</span></span>

### <span data-ttu-id="bad19-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bad19-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bad19-148">Note</span><span class="sxs-lookup"><span data-stu-id="bad19-148">NOTES</span></span>

## <span data-ttu-id="bad19-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bad19-149">RELATED LINKS</span></span>

[<span data-ttu-id="bad19-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bad19-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bad19-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bad19-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bad19-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bad19-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bad19-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bad19-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


