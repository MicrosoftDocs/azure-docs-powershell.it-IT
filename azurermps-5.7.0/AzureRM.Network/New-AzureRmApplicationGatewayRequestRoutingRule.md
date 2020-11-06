---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ab053235c928f109321cdf9adf3429e589958ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516695"
---
# <span data-ttu-id="bbe2f-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbe2f-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="bbe2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbe2f-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe2f-103">Crea una regola di routing delle richieste per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbe2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbe2f-104">SYNTAX</span></span>

### <span data-ttu-id="bbe2f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe2f-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbe2f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bbe2f-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbe2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbe2f-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe2f-108">**Il cmdlet Add-AzureRmApplicationGatewayRequestRoutingRule** crea una regola di routing delle richieste per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="bbe2f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbe2f-109">EXAMPLES</span></span>

### <span data-ttu-id="bbe2f-110">Esempio 1: creare una regola di routing delle richieste per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="bbe2f-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="bbe2f-111">Questo comando crea una regola di routing delle richieste di base denominata Rule01 e archivia il risultato nella variabile denominata $Rule.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="bbe2f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbe2f-112">PARAMETERS</span></span>

### <span data-ttu-id="bbe2f-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbe2f-113">-BackendAddressPool</span></span>
<span data-ttu-id="bbe2f-114">Specifica il pool di indirizzi back-end, come oggetto, per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bbe2f-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bbe2f-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="bbe2f-116">Specifica l'ID del pool di indirizzi back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="bbe2f-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bbe2f-117">-BackendHttpSettings</span></span>
<span data-ttu-id="bbe2f-118">Specifica le impostazioni HTTP di back-end, come oggetto, per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bbe2f-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="bbe2f-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="bbe2f-120">Specifica l'ID delle impostazioni HTTP back-end della regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="bbe2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe2f-121">-DefaultProfile</span></span>
<span data-ttu-id="bbe2f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbe2f-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="bbe2f-123">-HttpListener</span></span>
<span data-ttu-id="bbe2f-124">Specifica il listener HTTP back-end per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bbe2f-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="bbe2f-125">-HttpListenerId</span></span>
<span data-ttu-id="bbe2f-126">Specifica l'ID del listener HTTP di backend per la regola di routing delle richieste da creare.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="bbe2f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbe2f-127">-Name</span></span>
<span data-ttu-id="bbe2f-128">Specifica il nome della regola di routing delle richieste creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bbe2f-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbe2f-129">-RedirectConfiguration</span></span>
<span data-ttu-id="bbe2f-130">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbe2f-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="bbe2f-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bbe2f-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="bbe2f-132">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbe2f-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="bbe2f-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="bbe2f-133">-RuleType</span></span>
<span data-ttu-id="bbe2f-134">Specifica il tipo della regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="bbe2f-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="bbe2f-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="bbe2f-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="bbe2f-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="bbe2f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe2f-137">CommonParameters</span></span>
<span data-ttu-id="bbe2f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe2f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe2f-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe2f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe2f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbe2f-140">INPUTS</span></span>

### <span data-ttu-id="bbe2f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bbe2f-141">System.String</span></span>

## <span data-ttu-id="bbe2f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbe2f-142">OUTPUTS</span></span>

### <span data-ttu-id="bbe2f-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbe2f-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="bbe2f-144">Note</span><span class="sxs-lookup"><span data-stu-id="bbe2f-144">NOTES</span></span>

## <span data-ttu-id="bbe2f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbe2f-145">RELATED LINKS</span></span>

[<span data-ttu-id="bbe2f-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbe2f-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bbe2f-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbe2f-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bbe2f-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbe2f-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="bbe2f-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbe2f-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


