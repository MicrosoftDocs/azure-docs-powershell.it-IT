---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032366"
---
# <span data-ttu-id="596f3-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="596f3-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="596f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="596f3-102">SYNOPSIS</span></span>
<span data-ttu-id="596f3-103">Crea un criterio SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="596f3-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="596f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="596f3-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="596f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="596f3-105">DESCRIPTION</span></span>
<span data-ttu-id="596f3-106">Il cmdlet **New-AzApplicationGatewaySslPolicy** crea un criterio SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="596f3-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="596f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="596f3-107">EXAMPLES</span></span>

### <span data-ttu-id="596f3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="596f3-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="596f3-109">Questo comando crea un criterio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="596f3-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="596f3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="596f3-110">PARAMETERS</span></span>

### <span data-ttu-id="596f3-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="596f3-111">-CipherSuite</span></span>
<span data-ttu-id="596f3-112">Suite crittografiche SSL da abilitare nell'ordine specificato al gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="596f3-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="596f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596f3-113">-DefaultProfile</span></span>
<span data-ttu-id="596f3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="596f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="596f3-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="596f3-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="596f3-116">Specifica i protocolli disabilitati.</span><span class="sxs-lookup"><span data-stu-id="596f3-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="596f3-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="596f3-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="596f3-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="596f3-118">TLSv1_0</span></span> 
- <span data-ttu-id="596f3-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="596f3-119">TLSv1_1</span></span> 
- <span data-ttu-id="596f3-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="596f3-120">TLSv1_2</span></span>

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

### <span data-ttu-id="596f3-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="596f3-121">-MinProtocolVersion</span></span>
<span data-ttu-id="596f3-122">Versione minima del protocollo SSL da supportare nel gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="596f3-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="596f3-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="596f3-123">-PolicyName</span></span>
<span data-ttu-id="596f3-124">Nome dei criteri predefiniti SSL</span><span class="sxs-lookup"><span data-stu-id="596f3-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="596f3-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="596f3-125">-PolicyType</span></span>
<span data-ttu-id="596f3-126">Tipo di criteri SSL</span><span class="sxs-lookup"><span data-stu-id="596f3-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="596f3-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="596f3-127">-Confirm</span></span>
<span data-ttu-id="596f3-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="596f3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="596f3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596f3-129">-WhatIf</span></span>
<span data-ttu-id="596f3-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="596f3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="596f3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="596f3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="596f3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596f3-132">CommonParameters</span></span>
<span data-ttu-id="596f3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596f3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596f3-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="596f3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596f3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="596f3-135">INPUTS</span></span>

### <span data-ttu-id="596f3-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="596f3-136">None</span></span>

## <span data-ttu-id="596f3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="596f3-137">OUTPUTS</span></span>

### <span data-ttu-id="596f3-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="596f3-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="596f3-139">Note</span><span class="sxs-lookup"><span data-stu-id="596f3-139">NOTES</span></span>
* <span data-ttu-id="596f3-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="596f3-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="596f3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="596f3-141">RELATED LINKS</span></span>

[<span data-ttu-id="596f3-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="596f3-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="596f3-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="596f3-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


