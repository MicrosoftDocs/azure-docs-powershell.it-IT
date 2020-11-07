---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861001"
---
# <span data-ttu-id="68800-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="68800-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="68800-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68800-102">SYNOPSIS</span></span>
<span data-ttu-id="68800-103">Aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="68800-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="68800-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68800-104">SYNTAX</span></span>

### <span data-ttu-id="68800-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="68800-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68800-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="68800-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68800-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68800-107">DESCRIPTION</span></span>
<span data-ttu-id="68800-108">Il cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="68800-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="68800-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68800-109">EXAMPLES</span></span>

### <span data-ttu-id="68800-110">1:</span><span class="sxs-lookup"><span data-stu-id="68800-110">1:</span></span>
```

```

## <span data-ttu-id="68800-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68800-111">PARAMETERS</span></span>

### <span data-ttu-id="68800-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68800-112">-ApplicationGateway</span></span>
<span data-ttu-id="68800-113">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="68800-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="68800-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="68800-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="68800-115">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="68800-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="68800-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="68800-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="68800-117">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="68800-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="68800-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="68800-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="68800-119">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="68800-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="68800-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="68800-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="68800-121">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="68800-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="68800-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68800-122">-DefaultProfile</span></span>
<span data-ttu-id="68800-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68800-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68800-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="68800-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="68800-125">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="68800-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="68800-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="68800-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="68800-127">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="68800-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="68800-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="68800-128">-Name</span></span>
<span data-ttu-id="68800-129">Specifica il nome della mappa percorso URL che questo cmdlet aggiunge al pool del server back-end.</span><span class="sxs-lookup"><span data-stu-id="68800-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="68800-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="68800-130">-PathRules</span></span>
<span data-ttu-id="68800-131">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="68800-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="68800-132">Le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="68800-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="68800-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68800-133">CommonParameters</span></span>
<span data-ttu-id="68800-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68800-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68800-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68800-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68800-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68800-136">INPUTS</span></span>

### <span data-ttu-id="68800-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68800-137">PSApplicationGateway</span></span>
<span data-ttu-id="68800-138">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="68800-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="68800-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68800-139">OUTPUTS</span></span>

### <span data-ttu-id="68800-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68800-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68800-141">Note</span><span class="sxs-lookup"><span data-stu-id="68800-141">NOTES</span></span>

## <span data-ttu-id="68800-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68800-142">RELATED LINKS</span></span>

[<span data-ttu-id="68800-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="68800-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="68800-144">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="68800-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="68800-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="68800-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="68800-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="68800-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


