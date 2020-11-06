---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: a6cf6c4918dcaacb49ca9257acb436cec0556767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510420"
---
# <span data-ttu-id="ba09e-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ba09e-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="ba09e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba09e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba09e-103">Modifica una regola di routing delle richieste per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba09e-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba09e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba09e-104">SYNTAX</span></span>

### <span data-ttu-id="ba09e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba09e-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba09e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ba09e-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba09e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba09e-107">DESCRIPTION</span></span>
<span data-ttu-id="ba09e-108">Il cmdlet **set-AzureRmApplicationGatewayRequestRoutingRule** modifica una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="ba09e-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="ba09e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba09e-109">EXAMPLES</span></span>

### <span data-ttu-id="ba09e-110">Esempio 1: aggiornare una regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="ba09e-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="ba09e-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ba09e-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ba09e-112">Il secondo comando modifica la regola di routing delle richieste per il gateway dell'applicazione per l'uso delle impostazioni HTTP di back-end specificate nella variabile $Setting, un listener HTTP specificato nella variabile $Listener e un pool di indirizzi back-end specificato nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="ba09e-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="ba09e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba09e-113">PARAMETERS</span></span>

### <span data-ttu-id="ba09e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba09e-114">-ApplicationGateway</span></span>
<span data-ttu-id="ba09e-115">Specifica l'oggetto gateway dell'applicazione con cui questo cmdlet associa una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="ba09e-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="ba09e-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ba09e-116">-BackendAddressPool</span></span>
<span data-ttu-id="ba09e-117">Specifica il pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba09e-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba09e-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ba09e-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="ba09e-119">Specifica l'ID del pool di indirizzi back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba09e-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="ba09e-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ba09e-120">-BackendHttpSettings</span></span>
<span data-ttu-id="ba09e-121">Specifica le impostazioni HTTP di backend del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba09e-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba09e-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ba09e-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="ba09e-123">Specifica l'ID delle impostazioni HTTP di back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba09e-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="ba09e-124">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="ba09e-124">-HttpListener</span></span>
<span data-ttu-id="ba09e-125">Specifica il listener HTTP del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba09e-125">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba09e-126">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="ba09e-126">-HttpListenerId</span></span>
<span data-ttu-id="ba09e-127">Specifica l'ID del listener HTTP gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba09e-127">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="ba09e-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba09e-128">-Name</span></span>
<span data-ttu-id="ba09e-129">Specifica il nome della regola di routing delle richieste modificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba09e-129">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ba09e-130">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba09e-130">-RedirectConfiguration</span></span>
<span data-ttu-id="ba09e-131">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba09e-131">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba09e-132">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ba09e-132">-RedirectConfigurationId</span></span>
<span data-ttu-id="ba09e-133">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba09e-133">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="ba09e-134">-RuleType</span><span class="sxs-lookup"><span data-stu-id="ba09e-134">-RuleType</span></span>
<span data-ttu-id="ba09e-135">Specifica il tipo di regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="ba09e-135">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba09e-136">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="ba09e-136">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba09e-137">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="ba09e-137">-UrlPathMapId</span></span>
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

### <span data-ttu-id="ba09e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba09e-138">-DefaultProfile</span></span>
<span data-ttu-id="ba09e-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba09e-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba09e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba09e-140">CommonParameters</span></span>
<span data-ttu-id="ba09e-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba09e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba09e-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba09e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba09e-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba09e-143">INPUTS</span></span>

### <span data-ttu-id="ba09e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ba09e-144">System.String</span></span>

## <span data-ttu-id="ba09e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba09e-145">OUTPUTS</span></span>

### <span data-ttu-id="ba09e-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ba09e-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ba09e-147">Note</span><span class="sxs-lookup"><span data-stu-id="ba09e-147">NOTES</span></span>

## <span data-ttu-id="ba09e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba09e-148">RELATED LINKS</span></span>

[<span data-ttu-id="ba09e-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ba09e-149">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ba09e-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ba09e-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ba09e-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ba09e-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ba09e-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ba09e-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


