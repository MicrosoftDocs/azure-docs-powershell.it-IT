---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: dc6dc0c201ebb8298805064e06af5bb6c63ceda8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514692"
---
# <span data-ttu-id="c81ef-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c81ef-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c81ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c81ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c81ef-103">Crea un criterio SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c81ef-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c81ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c81ef-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c81ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c81ef-105">DESCRIPTION</span></span>
<span data-ttu-id="c81ef-106">Il cmdlet **New-AzureRmApplicationGatewaySslPolicy** crea un criterio SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c81ef-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="c81ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c81ef-107">EXAMPLES</span></span>

### <span data-ttu-id="c81ef-108">1:</span><span class="sxs-lookup"><span data-stu-id="c81ef-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="c81ef-109">Questo comando crea un criterio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c81ef-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="c81ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c81ef-110">PARAMETERS</span></span>

### <span data-ttu-id="c81ef-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="c81ef-111">-CipherSuite</span></span>
<span data-ttu-id="c81ef-112">Suite crittografiche SSL da abilitare nell'ordine specificato al gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c81ef-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="c81ef-113">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="c81ef-113">-DisabledSslProtocols</span></span>
<span data-ttu-id="c81ef-114">Specifica i protocolli disabilitati.</span><span class="sxs-lookup"><span data-stu-id="c81ef-114">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="c81ef-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c81ef-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c81ef-116">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="c81ef-116">TLSv1_0</span></span> 
- <span data-ttu-id="c81ef-117">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="c81ef-117">TLSv1_1</span></span> 
- <span data-ttu-id="c81ef-118">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="c81ef-118">TLSv1_2</span></span>

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

### <span data-ttu-id="c81ef-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="c81ef-119">-MinProtocolVersion</span></span>
<span data-ttu-id="c81ef-120">Versione minima del protocollo SSL da supportare nel gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="c81ef-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="c81ef-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="c81ef-121">-PolicyName</span></span>
<span data-ttu-id="c81ef-122">Nome dei criteri predefiniti SSL</span><span class="sxs-lookup"><span data-stu-id="c81ef-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="c81ef-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="c81ef-123">-PolicyType</span></span>
<span data-ttu-id="c81ef-124">Tipo di criteri SSL</span><span class="sxs-lookup"><span data-stu-id="c81ef-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="c81ef-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c81ef-125">-Confirm</span></span>
<span data-ttu-id="c81ef-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c81ef-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81ef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81ef-127">-WhatIf</span></span>
<span data-ttu-id="c81ef-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c81ef-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81ef-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c81ef-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81ef-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81ef-130">-DefaultProfile</span></span>
<span data-ttu-id="c81ef-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c81ef-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c81ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81ef-132">CommonParameters</span></span>
<span data-ttu-id="c81ef-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81ef-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c81ef-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81ef-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c81ef-135">INPUTS</span></span>

### <span data-ttu-id="c81ef-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c81ef-136">System.String</span></span>

## <span data-ttu-id="c81ef-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c81ef-137">OUTPUTS</span></span>

### <span data-ttu-id="c81ef-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c81ef-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c81ef-139">Note</span><span class="sxs-lookup"><span data-stu-id="c81ef-139">NOTES</span></span>
* <span data-ttu-id="c81ef-140">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="c81ef-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c81ef-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c81ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="c81ef-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c81ef-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c81ef-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c81ef-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


