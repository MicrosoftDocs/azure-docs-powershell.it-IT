---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866317"
---
# <span data-ttu-id="18544-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="18544-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="18544-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18544-102">SYNOPSIS</span></span>
<span data-ttu-id="18544-103">Aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="18544-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18544-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18544-104">SYNTAX</span></span>

### <span data-ttu-id="18544-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="18544-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18544-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="18544-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18544-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18544-107">DESCRIPTION</span></span>
<span data-ttu-id="18544-108">Il cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="18544-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="18544-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18544-109">EXAMPLES</span></span>

### <span data-ttu-id="18544-110">1:</span><span class="sxs-lookup"><span data-stu-id="18544-110">1:</span></span>
```

```

## <span data-ttu-id="18544-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18544-111">PARAMETERS</span></span>

### <span data-ttu-id="18544-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18544-112">-ApplicationGateway</span></span>
<span data-ttu-id="18544-113">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="18544-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="18544-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18544-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="18544-115">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="18544-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="18544-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="18544-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="18544-117">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="18544-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="18544-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="18544-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="18544-119">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="18544-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="18544-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="18544-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="18544-121">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="18544-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="18544-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18544-122">-DefaultProfile</span></span>
<span data-ttu-id="18544-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18544-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18544-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="18544-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="18544-125">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="18544-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="18544-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="18544-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="18544-127">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="18544-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="18544-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="18544-128">-Name</span></span>
<span data-ttu-id="18544-129">Specifica il nome della mappa percorso URL che questo cmdlet aggiunge al pool del server back-end.</span><span class="sxs-lookup"><span data-stu-id="18544-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="18544-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="18544-130">-PathRules</span></span>
<span data-ttu-id="18544-131">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="18544-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="18544-132">Le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="18544-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18544-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18544-133">CommonParameters</span></span>
<span data-ttu-id="18544-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18544-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18544-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18544-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18544-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18544-136">INPUTS</span></span>

### <span data-ttu-id="18544-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18544-137">PSApplicationGateway</span></span>
<span data-ttu-id="18544-138">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="18544-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="18544-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18544-139">OUTPUTS</span></span>

### <span data-ttu-id="18544-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18544-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18544-141">Note</span><span class="sxs-lookup"><span data-stu-id="18544-141">NOTES</span></span>

## <span data-ttu-id="18544-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18544-142">RELATED LINKS</span></span>

[<span data-ttu-id="18544-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="18544-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="18544-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="18544-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="18544-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="18544-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="18544-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="18544-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


