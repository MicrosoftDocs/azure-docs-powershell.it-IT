---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3c70fcd0e04b566ff1cd3297525d3ed2c9ed95ba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866975"
---
# <span data-ttu-id="d881b-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d881b-101">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d881b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d881b-102">SYNOPSIS</span></span>
<span data-ttu-id="d881b-103">Aggiorna un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d881b-103">Updates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d881b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d881b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d881b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d881b-105">DESCRIPTION</span></span>
<span data-ttu-id="d881b-106">Il cmdlet **set-AzureRmApplicationGatewayAuthenticationCertificate** aggiorna un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="d881b-106">The **Set-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d881b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d881b-107">EXAMPLES</span></span>

### <span data-ttu-id="d881b-108">1:</span><span class="sxs-lookup"><span data-stu-id="d881b-108">1:</span></span>
```

```

## <span data-ttu-id="d881b-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d881b-109">PARAMETERS</span></span>

### <span data-ttu-id="d881b-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d881b-110">-ApplicationGateway</span></span>
<span data-ttu-id="d881b-111">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiorna un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d881b-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="d881b-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d881b-112">-CertificateFile</span></span>
<span data-ttu-id="d881b-113">Specifica il percorso del file del certificato di autenticazione con cui questo cmdlet aggiorna il certificato.</span><span class="sxs-lookup"><span data-stu-id="d881b-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="d881b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d881b-114">-DefaultProfile</span></span>
<span data-ttu-id="d881b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d881b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d881b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d881b-116">-Name</span></span>
<span data-ttu-id="d881b-117">Specifica il nome del certificato di autenticazione che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="d881b-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="d881b-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d881b-118">-Confirm</span></span>
<span data-ttu-id="d881b-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d881b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d881b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d881b-120">-WhatIf</span></span>
<span data-ttu-id="d881b-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d881b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d881b-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d881b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d881b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d881b-123">CommonParameters</span></span>
<span data-ttu-id="d881b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d881b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d881b-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d881b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d881b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d881b-126">INPUTS</span></span>

### <span data-ttu-id="d881b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d881b-127">System.String</span></span>

## <span data-ttu-id="d881b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d881b-128">OUTPUTS</span></span>

### <span data-ttu-id="d881b-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d881b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d881b-130">Note</span><span class="sxs-lookup"><span data-stu-id="d881b-130">NOTES</span></span>
* <span data-ttu-id="d881b-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="d881b-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d881b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d881b-132">RELATED LINKS</span></span>

[<span data-ttu-id="d881b-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d881b-133">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d881b-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d881b-134">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d881b-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d881b-135">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d881b-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d881b-136">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)


