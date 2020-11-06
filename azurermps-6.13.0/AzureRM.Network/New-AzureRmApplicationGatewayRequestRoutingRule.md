---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: e812d0cbe6bd587e02a88cf59f8d8df5bccd1766
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519261"
---
# <span data-ttu-id="3176e-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3176e-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3176e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3176e-102">SYNOPSIS</span></span>
<span data-ttu-id="3176e-103">Crea una regola di routing delle richieste per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3176e-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3176e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3176e-104">SYNTAX</span></span>

### <span data-ttu-id="3176e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3176e-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3176e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3176e-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3176e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3176e-107">DESCRIPTION</span></span>
<span data-ttu-id="3176e-108">**Il cmdlet Add-AzureRmApplicationGatewayRequestRoutingRule** crea una regola di routing delle richieste per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="3176e-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="3176e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3176e-109">EXAMPLES</span></span>

### <span data-ttu-id="3176e-110">Esempio 1: creare una regola di routing delle richieste per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3176e-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="3176e-111">Questo comando crea una regola di routing delle richieste di base denominata Rule01 e archivia il risultato nella variabile denominata $Rule.</span><span class="sxs-lookup"><span data-stu-id="3176e-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="3176e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3176e-112">PARAMETERS</span></span>

### <span data-ttu-id="3176e-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3176e-113">-BackendAddressPool</span></span>
<span data-ttu-id="3176e-114">Specifica il pool di indirizzi back-end, come oggetto, per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="3176e-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="3176e-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="3176e-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="3176e-116">Specifica l'ID del pool di indirizzi back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="3176e-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="3176e-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3176e-117">-BackendHttpSettings</span></span>
<span data-ttu-id="3176e-118">Specifica le impostazioni HTTP di back-end, come oggetto, per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="3176e-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="3176e-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="3176e-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="3176e-120">Specifica l'ID delle impostazioni HTTP back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="3176e-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="3176e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3176e-121">-DefaultProfile</span></span>
<span data-ttu-id="3176e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3176e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3176e-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="3176e-123">-HttpListener</span></span>
<span data-ttu-id="3176e-124">Specifica il listener HTTP back-end per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="3176e-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="3176e-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="3176e-125">-HttpListenerId</span></span>
<span data-ttu-id="3176e-126">Specifica l'ID del listener HTTP di backend per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="3176e-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="3176e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3176e-127">-Name</span></span>
<span data-ttu-id="3176e-128">Specifica il nome della regola di routing delle richieste creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3176e-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3176e-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3176e-129">-RedirectConfiguration</span></span>
<span data-ttu-id="3176e-130">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3176e-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="3176e-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3176e-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="3176e-132">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3176e-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="3176e-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="3176e-133">-RuleType</span></span>
<span data-ttu-id="3176e-134">Specifica il tipo della regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="3176e-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="3176e-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="3176e-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="3176e-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="3176e-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="3176e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3176e-137">CommonParameters</span></span>
<span data-ttu-id="3176e-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3176e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3176e-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3176e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3176e-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3176e-140">INPUTS</span></span>

### <span data-ttu-id="3176e-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3176e-141">None</span></span>

## <span data-ttu-id="3176e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3176e-142">OUTPUTS</span></span>

### <span data-ttu-id="3176e-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3176e-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3176e-144">Note</span><span class="sxs-lookup"><span data-stu-id="3176e-144">NOTES</span></span>

## <span data-ttu-id="3176e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3176e-145">RELATED LINKS</span></span>

[<span data-ttu-id="3176e-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3176e-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3176e-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3176e-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3176e-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3176e-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3176e-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3176e-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


