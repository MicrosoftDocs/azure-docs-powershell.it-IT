---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860386"
---
# <span data-ttu-id="789b8-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="789b8-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="789b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="789b8-102">SYNOPSIS</span></span>
<span data-ttu-id="789b8-103">Rimuove un certificato di autenticazione da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="789b8-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="789b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="789b8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="789b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="789b8-105">DESCRIPTION</span></span>
<span data-ttu-id="789b8-106">Il cmdlet **Remove-AzApplicationGatewayAuthenticationCertificate** rimuove un certificato di autenticazione da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="789b8-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="789b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="789b8-107">EXAMPLES</span></span>

### <span data-ttu-id="789b8-108">1:</span><span class="sxs-lookup"><span data-stu-id="789b8-108">1:</span></span>
```

```

## <span data-ttu-id="789b8-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="789b8-109">PARAMETERS</span></span>

### <span data-ttu-id="789b8-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="789b8-110">-ApplicationGateway</span></span>
<span data-ttu-id="789b8-111">Specifica il nome del gateway dell'applicazione da cui questo cmdlet rimuove un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="789b8-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="789b8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789b8-112">-DefaultProfile</span></span>
<span data-ttu-id="789b8-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="789b8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="789b8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="789b8-114">-Name</span></span>
<span data-ttu-id="789b8-115">Specifica il nome del certificato di autenticazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="789b8-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789b8-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="789b8-116">-Confirm</span></span>
<span data-ttu-id="789b8-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="789b8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789b8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789b8-118">-WhatIf</span></span>
<span data-ttu-id="789b8-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="789b8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="789b8-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="789b8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789b8-121">CommonParameters</span></span>
<span data-ttu-id="789b8-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789b8-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789b8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789b8-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="789b8-124">INPUTS</span></span>

### <span data-ttu-id="789b8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="789b8-125">System.String</span></span>

## <span data-ttu-id="789b8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="789b8-126">OUTPUTS</span></span>

### <span data-ttu-id="789b8-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="789b8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="789b8-128">Note</span><span class="sxs-lookup"><span data-stu-id="789b8-128">NOTES</span></span>
* <span data-ttu-id="789b8-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="789b8-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="789b8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="789b8-130">RELATED LINKS</span></span>

[<span data-ttu-id="789b8-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="789b8-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="789b8-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="789b8-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="789b8-133">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="789b8-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="789b8-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="789b8-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


