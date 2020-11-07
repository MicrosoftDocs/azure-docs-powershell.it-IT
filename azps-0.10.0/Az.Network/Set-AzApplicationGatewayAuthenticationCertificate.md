---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0108A65B-E322-4783-AB6A-6AF1E1A58AC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 23b337779da46169be29e3dd6fef55fc70f4f035
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862874"
---
# <span data-ttu-id="b9c9e-101">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9c9e-101">Set-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b9c9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c9e-103">Aggiorna un certificato di autenticazione per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-103">Updates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="b9c9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9c9e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9c9e-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c9e-106">Il cmdlet **set-AzApplicationGatewayAuthenticationCertificate** aggiorna un certificato di autenticazione per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-106">The **Set-AzApplicationGatewayAuthenticationCertificate** cmdlet updates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b9c9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9c9e-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c9e-108">1:</span><span class="sxs-lookup"><span data-stu-id="b9c9e-108">1:</span></span>
```

```

## <span data-ttu-id="b9c9e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9c9e-109">PARAMETERS</span></span>

### <span data-ttu-id="b9c9e-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c9e-110">-ApplicationGateway</span></span>
<span data-ttu-id="b9c9e-111">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiorna un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-111">Specifies the name of application gateway for which this cmdlet updates an authentication certificate.</span></span>

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

### <span data-ttu-id="b9c9e-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b9c9e-112">-CertificateFile</span></span>
<span data-ttu-id="b9c9e-113">Specifica il percorso del file del certificato di autenticazione con cui questo cmdlet aggiorna il certificato.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-113">Specifies the path of the authentication certificate file with which this cmdlet updates the certificate.</span></span>

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

### <span data-ttu-id="b9c9e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c9e-114">-DefaultProfile</span></span>
<span data-ttu-id="b9c9e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c9e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9c9e-116">-Name</span></span>
<span data-ttu-id="b9c9e-117">Specifica il nome del certificato di autenticazione che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-117">Specifies the name of the authentication certificate that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b9c9e-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9c9e-118">-Confirm</span></span>
<span data-ttu-id="b9c9e-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c9e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c9e-120">-WhatIf</span></span>
<span data-ttu-id="b9c9e-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c9e-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c9e-123">CommonParameters</span></span>
<span data-ttu-id="b9c9e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c9e-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c9e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c9e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9c9e-126">INPUTS</span></span>

### <span data-ttu-id="b9c9e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c9e-127">System.String</span></span>

## <span data-ttu-id="b9c9e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9c9e-128">OUTPUTS</span></span>

### <span data-ttu-id="b9c9e-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c9e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9c9e-130">Note</span><span class="sxs-lookup"><span data-stu-id="b9c9e-130">NOTES</span></span>
* <span data-ttu-id="b9c9e-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="b9c9e-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b9c9e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9c9e-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9c9e-133">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9c9e-133">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9c9e-134">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9c9e-134">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9c9e-135">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9c9e-135">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b9c9e-136">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b9c9e-136">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)


