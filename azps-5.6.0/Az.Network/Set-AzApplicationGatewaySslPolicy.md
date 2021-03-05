---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 689e678bf740590f3d5d749124b74a38742395b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986732"
---
# <span data-ttu-id="9d011-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9d011-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="9d011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d011-102">SYNOPSIS</span></span>
<span data-ttu-id="9d011-103">Modifica il criterio SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d011-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="9d011-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d011-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d011-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d011-105">DESCRIPTION</span></span>
<span data-ttu-id="9d011-106">Il cmdlet **Set-AzApplicationGatewaySslPolicy** modifica il criterio SSL di un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="9d011-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="9d011-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d011-107">EXAMPLES</span></span>

### <span data-ttu-id="9d011-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d011-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="9d011-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="9d011-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9d011-110">Questo secondo comando modifica il criterio SSL in un tipo di criterio Predefinito e con nome criterio AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="9d011-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="9d011-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d011-111">PARAMETERS</span></span>

### <span data-ttu-id="9d011-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d011-112">-ApplicationGateway</span></span>
<span data-ttu-id="9d011-113">Specifica il gateway applicazione del criterio SSL modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d011-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9d011-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="9d011-114">-CipherSuite</span></span>
<span data-ttu-id="9d011-115">Pacchetti di crittografia Ssl da abilitato nell'ordine specificato al gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="9d011-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d011-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d011-116">-DefaultProfile</span></span>
<span data-ttu-id="9d011-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d011-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d011-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="9d011-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="9d011-119">Specifica quali protocolli sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="9d011-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="9d011-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="9d011-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d011-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="9d011-121">TLSv1_0</span></span> 
- <span data-ttu-id="9d011-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="9d011-122">TLSv1_1</span></span> 
- <span data-ttu-id="9d011-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="9d011-123">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d011-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="9d011-124">-MinProtocolVersion</span></span>
<span data-ttu-id="9d011-125">Versione minima del protocollo Ssl da supportata nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="9d011-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="9d011-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="9d011-126">-PolicyName</span></span>
<span data-ttu-id="9d011-127">Nome del criterio predefinito Ssl</span><span class="sxs-lookup"><span data-stu-id="9d011-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="9d011-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="9d011-128">-PolicyType</span></span>
<span data-ttu-id="9d011-129">Tipo di criterio Ssl</span><span class="sxs-lookup"><span data-stu-id="9d011-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="9d011-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d011-130">-Confirm</span></span>
<span data-ttu-id="9d011-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d011-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d011-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d011-132">-WhatIf</span></span>
<span data-ttu-id="9d011-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d011-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d011-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d011-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d011-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d011-135">CommonParameters</span></span>
<span data-ttu-id="9d011-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d011-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d011-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d011-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d011-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d011-138">INPUTS</span></span>

### <span data-ttu-id="9d011-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d011-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d011-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d011-140">OUTPUTS</span></span>

### <span data-ttu-id="9d011-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d011-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d011-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d011-142">NOTES</span></span>
* <span data-ttu-id="9d011-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="9d011-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9d011-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d011-144">RELATED LINKS</span></span>

[<span data-ttu-id="9d011-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9d011-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="9d011-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="9d011-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


