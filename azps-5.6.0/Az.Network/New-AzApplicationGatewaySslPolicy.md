---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: b8b9eadd0beba6413b8b5919087a1c9081735ddf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015053"
---
# <span data-ttu-id="1b12d-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1b12d-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="1b12d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b12d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b12d-103">Crea un criterio SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b12d-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="1b12d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b12d-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b12d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b12d-105">DESCRIPTION</span></span>
<span data-ttu-id="1b12d-106">Il cmdlet **New-AzApplicationGatewaySslPolicy** crea un criterio SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b12d-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="1b12d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b12d-107">EXAMPLES</span></span>

### <span data-ttu-id="1b12d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b12d-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="1b12d-109">Questo comando crea un criterio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1b12d-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="1b12d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b12d-110">PARAMETERS</span></span>

### <span data-ttu-id="1b12d-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="1b12d-111">-CipherSuite</span></span>
<span data-ttu-id="1b12d-112">Pacchetti di crittografia Ssl da abilitato nell'ordine specificato al gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="1b12d-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="1b12d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b12d-113">-DefaultProfile</span></span>
<span data-ttu-id="1b12d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b12d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b12d-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="1b12d-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="1b12d-116">Specifica quali protocolli sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="1b12d-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="1b12d-117">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1b12d-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b12d-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="1b12d-118">TLSv1_0</span></span> 
- <span data-ttu-id="1b12d-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="1b12d-119">TLSv1_1</span></span> 
- <span data-ttu-id="1b12d-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="1b12d-120">TLSv1_2</span></span>

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

### <span data-ttu-id="1b12d-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="1b12d-121">-MinProtocolVersion</span></span>
<span data-ttu-id="1b12d-122">Versione minima del protocollo Ssl da supporto nel gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="1b12d-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="1b12d-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="1b12d-123">-PolicyName</span></span>
<span data-ttu-id="1b12d-124">Nome del criterio predefinito Ssl</span><span class="sxs-lookup"><span data-stu-id="1b12d-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="1b12d-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="1b12d-125">-PolicyType</span></span>
<span data-ttu-id="1b12d-126">Tipo di criterio Ssl</span><span class="sxs-lookup"><span data-stu-id="1b12d-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="1b12d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b12d-127">-Confirm</span></span>
<span data-ttu-id="1b12d-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b12d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b12d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b12d-129">-WhatIf</span></span>
<span data-ttu-id="1b12d-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b12d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b12d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b12d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b12d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b12d-132">CommonParameters</span></span>
<span data-ttu-id="1b12d-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b12d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b12d-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b12d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b12d-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b12d-135">INPUTS</span></span>

### <span data-ttu-id="1b12d-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b12d-136">None</span></span>

## <span data-ttu-id="1b12d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b12d-137">OUTPUTS</span></span>

### <span data-ttu-id="1b12d-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1b12d-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="1b12d-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b12d-139">NOTES</span></span>
* <span data-ttu-id="1b12d-140">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="1b12d-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1b12d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b12d-141">RELATED LINKS</span></span>

[<span data-ttu-id="1b12d-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1b12d-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="1b12d-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1b12d-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


