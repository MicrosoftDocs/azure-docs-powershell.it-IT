---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 07958bcab5948280774ff3e056f7c34c9f6b0aac
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862817"
---
# <span data-ttu-id="502a5-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="502a5-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="502a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="502a5-102">SYNOPSIS</span></span>
<span data-ttu-id="502a5-103">Modifica i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="502a5-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="502a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="502a5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="502a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="502a5-105">DESCRIPTION</span></span>
<span data-ttu-id="502a5-106">Il cmdlet **set-AzApplicationGatewaySslPolicy** modifica i criteri SSL di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="502a5-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="502a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="502a5-107">EXAMPLES</span></span>

### <span data-ttu-id="502a5-108">1:</span><span class="sxs-lookup"><span data-stu-id="502a5-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="502a5-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="502a5-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="502a5-110">Questo secondo comando modifica i criteri SSL in un tipo di criterio predefinito e un nome di criterio AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="502a5-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="502a5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="502a5-111">PARAMETERS</span></span>

### <span data-ttu-id="502a5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="502a5-112">-ApplicationGateway</span></span>
<span data-ttu-id="502a5-113">Specifica il gateway dell'applicazione dei criteri SSL modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="502a5-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="502a5-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="502a5-114">-CipherSuite</span></span>
<span data-ttu-id="502a5-115">Suite crittografiche SSL da abilitare nell'ordine specificato al gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="502a5-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="502a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502a5-116">-DefaultProfile</span></span>
<span data-ttu-id="502a5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="502a5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="502a5-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="502a5-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="502a5-119">Specifica i protocolli disabilitati.</span><span class="sxs-lookup"><span data-stu-id="502a5-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="502a5-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="502a5-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="502a5-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="502a5-121">TLSv1_0</span></span> 
- <span data-ttu-id="502a5-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="502a5-122">TLSv1_1</span></span> 
- <span data-ttu-id="502a5-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="502a5-123">TLSv1_2</span></span>

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

### <span data-ttu-id="502a5-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="502a5-124">-MinProtocolVersion</span></span>
<span data-ttu-id="502a5-125">Versione minima del protocollo SSL da supportare nel gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="502a5-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="502a5-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="502a5-126">-PolicyName</span></span>
<span data-ttu-id="502a5-127">Nome dei criteri predefiniti SSL</span><span class="sxs-lookup"><span data-stu-id="502a5-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="502a5-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="502a5-128">-PolicyType</span></span>
<span data-ttu-id="502a5-129">Tipo di criteri SSL</span><span class="sxs-lookup"><span data-stu-id="502a5-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="502a5-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="502a5-130">-Confirm</span></span>
<span data-ttu-id="502a5-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="502a5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502a5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="502a5-132">-WhatIf</span></span>
<span data-ttu-id="502a5-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="502a5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="502a5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="502a5-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502a5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502a5-135">CommonParameters</span></span>
<span data-ttu-id="502a5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502a5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502a5-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502a5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502a5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="502a5-138">INPUTS</span></span>

### <span data-ttu-id="502a5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="502a5-139">System.String</span></span>

## <span data-ttu-id="502a5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="502a5-140">OUTPUTS</span></span>

### <span data-ttu-id="502a5-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="502a5-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="502a5-142">Note</span><span class="sxs-lookup"><span data-stu-id="502a5-142">NOTES</span></span>
* <span data-ttu-id="502a5-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="502a5-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="502a5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="502a5-144">RELATED LINKS</span></span>

[<span data-ttu-id="502a5-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="502a5-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="502a5-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="502a5-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


