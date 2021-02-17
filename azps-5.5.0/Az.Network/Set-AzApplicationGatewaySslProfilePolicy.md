---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 7d04d73905bde7ab008c6910cab708e209125316
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407999"
---
# <span data-ttu-id="305f7-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="305f7-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="305f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305f7-102">SYNOPSIS</span></span>
<span data-ttu-id="305f7-103">Modifica il criterio SSL di un profilo SSL del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="305f7-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="305f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="305f7-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="305f7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="305f7-105">DESCRIPTION</span></span>
<span data-ttu-id="305f7-106">Il cmdlet **Set-AzApplicationGatewaySslProfilePolicy** modifica il criterio SSL di un profilo SSL del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="305f7-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="305f7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="305f7-107">EXAMPLES</span></span>

### <span data-ttu-id="305f7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="305f7-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="305f7-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="305f7-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="305f7-110">Il secondo comando recupera il profilo SSL denominato SslProfile01 per $AppGw e archivia le impostazioni nella $profile variabile.</span><span class="sxs-lookup"><span data-stu-id="305f7-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="305f7-111">L'ultimo comando modifica il criterio SSL dell'oggetto profilo SSL archiviato nel $profile.</span><span class="sxs-lookup"><span data-stu-id="305f7-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="305f7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="305f7-112">PARAMETERS</span></span>

### <span data-ttu-id="305f7-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="305f7-113">-CipherSuite</span></span>
<span data-ttu-id="305f7-114">Pacchetti di crittografia Ssl da abilitato nell'ordine specificato al gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="305f7-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="305f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305f7-115">-DefaultProfile</span></span>
<span data-ttu-id="305f7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="305f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="305f7-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="305f7-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="305f7-118">Elenco dei protocolli SSL da disabilitare</span><span class="sxs-lookup"><span data-stu-id="305f7-118">List of SSL protocols to be disabled</span></span>

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

### <span data-ttu-id="305f7-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="305f7-119">-MinProtocolVersion</span></span>
<span data-ttu-id="305f7-120">Versione minima del protocollo Ssl da supporto nel gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="305f7-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="305f7-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="305f7-121">-PolicyName</span></span>
<span data-ttu-id="305f7-122">Nome del criterio predefinito Ssl</span><span class="sxs-lookup"><span data-stu-id="305f7-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="305f7-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="305f7-123">-PolicyType</span></span>
<span data-ttu-id="305f7-124">Tipo di criterio Ssl</span><span class="sxs-lookup"><span data-stu-id="305f7-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="305f7-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="305f7-125">-SslProfile</span></span>
<span data-ttu-id="305f7-126">Profilo SSL del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="305f7-126">The application gateway SSL profile</span></span>

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

### <span data-ttu-id="305f7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="305f7-127">-Confirm</span></span>
<span data-ttu-id="305f7-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="305f7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="305f7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="305f7-129">-WhatIf</span></span>
<span data-ttu-id="305f7-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="305f7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="305f7-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="305f7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="305f7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305f7-132">CommonParameters</span></span>
<span data-ttu-id="305f7-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="305f7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305f7-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="305f7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305f7-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="305f7-135">INPUTS</span></span>

### <span data-ttu-id="305f7-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="305f7-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="305f7-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="305f7-137">OUTPUTS</span></span>

### <span data-ttu-id="305f7-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="305f7-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="305f7-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="305f7-139">NOTES</span></span>

## <span data-ttu-id="305f7-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="305f7-140">RELATED LINKS</span></span>



[<span data-ttu-id="305f7-141">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="305f7-141">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="305f7-142">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="305f7-142">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)
