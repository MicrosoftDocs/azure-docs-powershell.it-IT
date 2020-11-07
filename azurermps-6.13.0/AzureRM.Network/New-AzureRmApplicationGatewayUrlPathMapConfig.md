---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 6752526e5c6f035d6446c4e6e3ed31724bdbd337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688395"
---
# <span data-ttu-id="1a6d2-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1a6d2-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="1a6d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6d2-103">Crea una matrice di mapping dei percorsi URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a6d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a6d2-104">SYNTAX</span></span>

### <span data-ttu-id="1a6d2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a6d2-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a6d2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1a6d2-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a6d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a6d2-107">DESCRIPTION</span></span>
<span data-ttu-id="1a6d2-108">Il cmdlet **New-AzureRmApplicationGatewayUrlPathMapConfig** crea una matrice di mapping dei percorsi URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1a6d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a6d2-109">EXAMPLES</span></span>

### <span data-ttu-id="1a6d2-110">Esempio 1: creare una matrice di mapping dei percorsi URL in un pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="1a6d2-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="1a6d2-111">Questo comando crea una matrice di mapping dei percorsi URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="1a6d2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a6d2-112">PARAMETERS</span></span>

### <span data-ttu-id="1a6d2-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1a6d2-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="1a6d2-114">Specifica il pool di indirizzi di backend predefinito da instradare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1a6d2-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1a6d2-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="1a6d2-116">Specifica l'ID del pool di indirizzi backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="1a6d2-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1a6d2-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="1a6d2-118">Specifica le impostazioni HTTP di backend predefinite da usare nel caso in cui nessuna delle regole specificate nel parametro *pathRules* corrisponda.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="1a6d2-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="1a6d2-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="1a6d2-120">Specifica l'ID impostazioni HTTP backend predefinito.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="1a6d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6d2-121">-DefaultProfile</span></span>
<span data-ttu-id="1a6d2-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a6d2-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a6d2-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="1a6d2-124">RedirectConfiguration predefinito del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="1a6d2-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1a6d2-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1a6d2-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="1a6d2-126">ID del gateway applicazione predefinito RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a6d2-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="1a6d2-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a6d2-127">-Name</span></span>
<span data-ttu-id="1a6d2-128">Specifica il nome della mappa percorso URL creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1a6d2-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="1a6d2-129">-PathRules</span></span>
<span data-ttu-id="1a6d2-130">Specifica un elenco di regole di percorso.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="1a6d2-131">Tieni presente che le regole del percorso sono riservate agli ordini, che vengono applicate in modo che siano specificate.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="1a6d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6d2-132">CommonParameters</span></span>
<span data-ttu-id="1a6d2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a6d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6d2-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a6d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6d2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a6d2-135">INPUTS</span></span>

### <span data-ttu-id="1a6d2-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1a6d2-136">None</span></span>

## <span data-ttu-id="1a6d2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a6d2-137">OUTPUTS</span></span>

### <span data-ttu-id="1a6d2-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="1a6d2-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="1a6d2-139">Note</span><span class="sxs-lookup"><span data-stu-id="1a6d2-139">NOTES</span></span>

## <span data-ttu-id="1a6d2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a6d2-140">RELATED LINKS</span></span>

[<span data-ttu-id="1a6d2-141">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1a6d2-141">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1a6d2-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1a6d2-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1a6d2-143">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1a6d2-143">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="1a6d2-144">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1a6d2-144">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


