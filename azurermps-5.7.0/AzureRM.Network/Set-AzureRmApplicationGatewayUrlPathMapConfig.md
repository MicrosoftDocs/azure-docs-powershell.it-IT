---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 949de1a2016ffbecb96a8f10a34435cedd284ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520687"
---
# <span data-ttu-id="5e63e-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e63e-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5e63e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e63e-102">SYNOPSIS</span></span>
<span data-ttu-id="5e63e-103">Imposta la configurazione per una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="5e63e-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e63e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e63e-104">SYNTAX</span></span>

### <span data-ttu-id="5e63e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e63e-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e63e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5e63e-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e63e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e63e-107">DESCRIPTION</span></span>
<span data-ttu-id="5e63e-108">Il cmdlet **set-AzureRmApplicationGatewayUrlPathMapConfig** imposta la configurazione per una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="5e63e-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5e63e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e63e-109">EXAMPLES</span></span>

## <span data-ttu-id="5e63e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e63e-110">PARAMETERS</span></span>

### <span data-ttu-id="5e63e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e63e-111">-ApplicationGateway</span></span>
<span data-ttu-id="5e63e-112">Specifica il gateway dell'applicazione a cui questo cmdlet imposta una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="5e63e-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="5e63e-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5e63e-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5e63e-114">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="5e63e-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5e63e-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5e63e-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5e63e-116">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="5e63e-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5e63e-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5e63e-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5e63e-118">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="5e63e-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5e63e-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5e63e-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5e63e-120">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="5e63e-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5e63e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e63e-121">-DefaultProfile</span></span>
<span data-ttu-id="5e63e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e63e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e63e-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e63e-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5e63e-124">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5e63e-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5e63e-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5e63e-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5e63e-126">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e63e-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5e63e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e63e-127">-Name</span></span>
<span data-ttu-id="5e63e-128">Specifica il nome della mappa percorso URL in cui questo cmdlet imposta la configurazione.</span><span class="sxs-lookup"><span data-stu-id="5e63e-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="5e63e-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5e63e-129">-PathRules</span></span>
<span data-ttu-id="5e63e-130">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="5e63e-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="5e63e-131">Tieni presente che le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="5e63e-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="5e63e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e63e-132">CommonParameters</span></span>
<span data-ttu-id="5e63e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e63e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e63e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e63e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e63e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e63e-135">INPUTS</span></span>

### <span data-ttu-id="5e63e-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e63e-136">PSApplicationGateway</span></span>
<span data-ttu-id="5e63e-137">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5e63e-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5e63e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e63e-138">OUTPUTS</span></span>

### <span data-ttu-id="5e63e-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e63e-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e63e-140">Note</span><span class="sxs-lookup"><span data-stu-id="5e63e-140">NOTES</span></span>

## <span data-ttu-id="5e63e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e63e-141">RELATED LINKS</span></span>

[<span data-ttu-id="5e63e-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e63e-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5e63e-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e63e-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5e63e-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e63e-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5e63e-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5e63e-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


