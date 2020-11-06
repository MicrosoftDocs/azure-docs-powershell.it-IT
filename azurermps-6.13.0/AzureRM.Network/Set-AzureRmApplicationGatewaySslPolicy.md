---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: c482f3e4e7882f32db3415a36aab0a0313c0085a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507420"
---
# <span data-ttu-id="726bd-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="726bd-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="726bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="726bd-102">SYNOPSIS</span></span>
<span data-ttu-id="726bd-103">Modifica i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="726bd-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="726bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="726bd-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="726bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="726bd-105">DESCRIPTION</span></span>
<span data-ttu-id="726bd-106">Il cmdlet **set-AzureRmApplicationGatewaySslPolicy** modifica i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="726bd-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="726bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="726bd-107">EXAMPLES</span></span>

### <span data-ttu-id="726bd-108">1:</span><span class="sxs-lookup"><span data-stu-id="726bd-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="726bd-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="726bd-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="726bd-110">Questo secondo comando modifica i criteri SSL in un tipo di criterio predefinito e un nome di criterio AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="726bd-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="726bd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="726bd-111">PARAMETERS</span></span>

### <span data-ttu-id="726bd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="726bd-112">-ApplicationGateway</span></span>
<span data-ttu-id="726bd-113">Specifica il gateway dell'applicazione dei criteri SSL modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726bd-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="726bd-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="726bd-114">-CipherSuite</span></span>
<span data-ttu-id="726bd-115">Suite crittografiche SSL da abilitare nell'ordine specificato al gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="726bd-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726bd-116">-DefaultProfile</span></span>
<span data-ttu-id="726bd-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="726bd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="726bd-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="726bd-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="726bd-119">Specifica i protocolli disabilitati.</span><span class="sxs-lookup"><span data-stu-id="726bd-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="726bd-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="726bd-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="726bd-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="726bd-121">TLSv1_0</span></span> 
- <span data-ttu-id="726bd-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="726bd-122">TLSv1_1</span></span> 
- <span data-ttu-id="726bd-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="726bd-123">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bd-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="726bd-124">-MinProtocolVersion</span></span>
<span data-ttu-id="726bd-125">Versione minima del protocollo SSL da supportare nel gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="726bd-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bd-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="726bd-126">-PolicyName</span></span>
<span data-ttu-id="726bd-127">Nome dei criteri predefiniti SSL</span><span class="sxs-lookup"><span data-stu-id="726bd-127">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bd-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="726bd-128">-PolicyType</span></span>
<span data-ttu-id="726bd-129">Tipo di criteri SSL</span><span class="sxs-lookup"><span data-stu-id="726bd-129">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bd-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="726bd-130">-Confirm</span></span>
<span data-ttu-id="726bd-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="726bd-132">-WhatIf</span></span>
<span data-ttu-id="726bd-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="726bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="726bd-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="726bd-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726bd-135">CommonParameters</span></span>
<span data-ttu-id="726bd-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="726bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726bd-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726bd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726bd-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="726bd-138">INPUTS</span></span>

### <span data-ttu-id="726bd-139">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="726bd-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="726bd-140">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="726bd-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="726bd-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="726bd-141">OUTPUTS</span></span>

### <span data-ttu-id="726bd-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="726bd-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="726bd-143">Note</span><span class="sxs-lookup"><span data-stu-id="726bd-143">NOTES</span></span>
* <span data-ttu-id="726bd-144">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="726bd-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="726bd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="726bd-145">RELATED LINKS</span></span>

[<span data-ttu-id="726bd-146">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="726bd-146">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="726bd-147">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="726bd-147">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


