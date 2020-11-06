---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 821f31ba8f42ff8a7b94839aad344a2f144353d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520042"
---
# <span data-ttu-id="5ec74-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec74-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5ec74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ec74-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec74-103">Aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="5ec74-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ec74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ec74-104">SYNTAX</span></span>

### <span data-ttu-id="5ec74-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ec74-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ec74-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5ec74-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ec74-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ec74-107">DESCRIPTION</span></span>
<span data-ttu-id="5ec74-108">Il cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** aggiunge una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="5ec74-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="5ec74-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ec74-109">EXAMPLES</span></span>

## <span data-ttu-id="5ec74-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ec74-110">PARAMETERS</span></span>

### <span data-ttu-id="5ec74-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ec74-111">-ApplicationGateway</span></span>
<span data-ttu-id="5ec74-112">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="5ec74-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="5ec74-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ec74-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5ec74-114">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="5ec74-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5ec74-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5ec74-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5ec74-116">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="5ec74-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5ec74-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5ec74-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5ec74-118">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="5ec74-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5ec74-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5ec74-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5ec74-120">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="5ec74-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5ec74-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ec74-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5ec74-122">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5ec74-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5ec74-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5ec74-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5ec74-124">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ec74-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5ec74-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ec74-125">-Name</span></span>
<span data-ttu-id="5ec74-126">Specifica il nome della mappa percorso URL che questo cmdlet aggiunge al pool del server back-end.</span><span class="sxs-lookup"><span data-stu-id="5ec74-126">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="5ec74-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5ec74-127">-PathRules</span></span>
<span data-ttu-id="5ec74-128">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="5ec74-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="5ec74-129">Le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="5ec74-129">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="5ec74-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec74-130">-DefaultProfile</span></span>
<span data-ttu-id="5ec74-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec74-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ec74-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec74-132">CommonParameters</span></span>
<span data-ttu-id="5ec74-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec74-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec74-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec74-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec74-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ec74-135">INPUTS</span></span>

### <span data-ttu-id="5ec74-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ec74-136">PSApplicationGateway</span></span>
<span data-ttu-id="5ec74-137">Il parametro ' ApplicationGateway ' accetta il valore di tipo ' PSApplicationGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5ec74-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5ec74-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ec74-138">OUTPUTS</span></span>

### <span data-ttu-id="5ec74-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ec74-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ec74-140">Note</span><span class="sxs-lookup"><span data-stu-id="5ec74-140">NOTES</span></span>

## <span data-ttu-id="5ec74-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ec74-141">RELATED LINKS</span></span>

[<span data-ttu-id="5ec74-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec74-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5ec74-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec74-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5ec74-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec74-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5ec74-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5ec74-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


