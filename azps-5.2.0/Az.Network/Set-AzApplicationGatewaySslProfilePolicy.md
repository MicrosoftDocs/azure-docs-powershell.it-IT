---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 344be8b71bc74f3620ca90dd60b61f9a59026ea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333892"
---
# <span data-ttu-id="ba95d-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ba95d-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="ba95d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba95d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba95d-103">Modifica i criteri SSL del profilo SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba95d-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="ba95d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba95d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba95d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba95d-105">DESCRIPTION</span></span>
<span data-ttu-id="ba95d-106">Il cmdlet **set-AzApplicationGatewaySslProfilePolicy** modifica i criteri SSL del profilo SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba95d-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="ba95d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba95d-107">EXAMPLES</span></span>

### <span data-ttu-id="ba95d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba95d-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="ba95d-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ba95d-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="ba95d-110">Il secondo comando ottiene il profilo SSL denominato SslProfile01 per $AppGw e archivia le impostazioni nella variabile $profile.</span><span class="sxs-lookup"><span data-stu-id="ba95d-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="ba95d-111">L'ultimo comando modifica i criteri SSL dell'oggetto profilo SSL archiviato in $profile.</span><span class="sxs-lookup"><span data-stu-id="ba95d-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="ba95d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba95d-112">PARAMETERS</span></span>

### <span data-ttu-id="ba95d-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="ba95d-113">-CipherSuite</span></span>
<span data-ttu-id="ba95d-114">Suite crittografiche SSL da abilitare nell'ordine specificato al gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ba95d-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba95d-115">-DefaultProfile</span></span>
<span data-ttu-id="ba95d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba95d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="ba95d-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="ba95d-118">Elenco dei protocolli SSL da disabilitare</span><span class="sxs-lookup"><span data-stu-id="ba95d-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="ba95d-119">-MinProtocolVersion</span></span>
<span data-ttu-id="ba95d-120">Versione minima del protocollo SSL da supportare nel gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="ba95d-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="ba95d-121">-PolicyName</span></span>
<span data-ttu-id="ba95d-122">Nome dei criteri predefiniti SSL</span><span class="sxs-lookup"><span data-stu-id="ba95d-122">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="ba95d-123">-PolicyType</span></span>
<span data-ttu-id="ba95d-124">Tipo di criteri SSL</span><span class="sxs-lookup"><span data-stu-id="ba95d-124">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="ba95d-125">-SslProfile</span></span>
<span data-ttu-id="ba95d-126">Profilo SSL del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ba95d-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba95d-127">-Confirm</span></span>
<span data-ttu-id="ba95d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba95d-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba95d-129">-WhatIf</span></span>
<span data-ttu-id="ba95d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba95d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba95d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba95d-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba95d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba95d-132">CommonParameters</span></span>
<span data-ttu-id="ba95d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba95d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba95d-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba95d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba95d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba95d-135">INPUTS</span></span>

### <span data-ttu-id="ba95d-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ba95d-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ba95d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba95d-137">OUTPUTS</span></span>

### <span data-ttu-id="ba95d-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="ba95d-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="ba95d-139">Note</span><span class="sxs-lookup"><span data-stu-id="ba95d-139">NOTES</span></span>

## <span data-ttu-id="ba95d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba95d-140">RELATED LINKS</span></span>

[<span data-ttu-id="ba95d-141">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ba95d-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="ba95d-142">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ba95d-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="ba95d-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ba95d-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="ba95d-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="ba95d-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)