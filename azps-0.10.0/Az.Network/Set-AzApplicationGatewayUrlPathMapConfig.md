---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5eb4fb0f036331fe68755a3a8ebddcd7e1b6e424
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862813"
---
# <span data-ttu-id="210c4-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="210c4-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="210c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="210c4-102">SYNOPSIS</span></span>
<span data-ttu-id="210c4-103">Imposta la configurazione per una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="210c4-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="210c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="210c4-104">SYNTAX</span></span>

### <span data-ttu-id="210c4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="210c4-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210c4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="210c4-106">SetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="210c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="210c4-107">DESCRIPTION</span></span>
<span data-ttu-id="210c4-108">Il cmdlet **set-AzApplicationGatewayUrlPathMapConfig** imposta la configurazione per una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="210c4-108">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="210c4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="210c4-109">EXAMPLES</span></span>

### <span data-ttu-id="210c4-110">1:</span><span class="sxs-lookup"><span data-stu-id="210c4-110">1:</span></span>
```

```

## <span data-ttu-id="210c4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="210c4-111">PARAMETERS</span></span>

### <span data-ttu-id="210c4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="210c4-112">-ApplicationGateway</span></span>
<span data-ttu-id="210c4-113">Specifica il gateway dell'applicazione a cui questo cmdlet imposta una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="210c4-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="210c4-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="210c4-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="210c4-115">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="210c4-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="210c4-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="210c4-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="210c4-117">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="210c4-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="210c4-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="210c4-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="210c4-119">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="210c4-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="210c4-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="210c4-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="210c4-121">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="210c4-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="210c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210c4-122">-DefaultProfile</span></span>
<span data-ttu-id="210c4-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="210c4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="210c4-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="210c4-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="210c4-125">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="210c4-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="210c4-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="210c4-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="210c4-127">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="210c4-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="210c4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="210c4-128">-Name</span></span>
<span data-ttu-id="210c4-129">Specifica il nome della mappa percorso URL in cui questo cmdlet imposta la configurazione.</span><span class="sxs-lookup"><span data-stu-id="210c4-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="210c4-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="210c4-130">-PathRules</span></span>
<span data-ttu-id="210c4-131">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="210c4-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="210c4-132">Tieni presente che le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="210c4-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="210c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210c4-133">CommonParameters</span></span>
<span data-ttu-id="210c4-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="210c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210c4-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="210c4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210c4-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="210c4-136">INPUTS</span></span>

### <span data-ttu-id="210c4-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="210c4-137">PSApplicationGateway</span></span>
<span data-ttu-id="210c4-138">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="210c4-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="210c4-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="210c4-139">OUTPUTS</span></span>

### <span data-ttu-id="210c4-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="210c4-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="210c4-141">Note</span><span class="sxs-lookup"><span data-stu-id="210c4-141">NOTES</span></span>

## <span data-ttu-id="210c4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="210c4-142">RELATED LINKS</span></span>

[<span data-ttu-id="210c4-143">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="210c4-143">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="210c4-144">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="210c4-144">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="210c4-145">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="210c4-145">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="210c4-146">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="210c4-146">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


