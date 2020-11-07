---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 6652da4491bc503ecc2d0c8ee016416cefbff172
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861045"
---
# <span data-ttu-id="40d7a-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="40d7a-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="40d7a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="40d7a-103">Aggiunge un certificato di autenticazione a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40d7a-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="40d7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40d7a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40d7a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40d7a-105">DESCRIPTION</span></span>
<span data-ttu-id="40d7a-106">Il cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** aggiunge un certificato di autenticazione a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="40d7a-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="40d7a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40d7a-107">EXAMPLES</span></span>

### <span data-ttu-id="40d7a-108">1:</span><span class="sxs-lookup"><span data-stu-id="40d7a-108">1:</span></span>
```

```

## <span data-ttu-id="40d7a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40d7a-109">PARAMETERS</span></span>

### <span data-ttu-id="40d7a-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d7a-110">-ApplicationGateway</span></span>
<span data-ttu-id="40d7a-111">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiunge un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="40d7a-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="40d7a-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="40d7a-112">-CertificateFile</span></span>
<span data-ttu-id="40d7a-113">Specifica il percorso del certificato di autenticazione aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d7a-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="40d7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d7a-114">-DefaultProfile</span></span>
<span data-ttu-id="40d7a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40d7a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d7a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="40d7a-116">-Name</span></span>
<span data-ttu-id="40d7a-117">Specifica il nome di un certificato aggiunto dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="40d7a-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="40d7a-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40d7a-118">-Confirm</span></span>
<span data-ttu-id="40d7a-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d7a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d7a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d7a-120">-WhatIf</span></span>
<span data-ttu-id="40d7a-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40d7a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d7a-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40d7a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d7a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d7a-123">CommonParameters</span></span>
<span data-ttu-id="40d7a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d7a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d7a-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d7a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d7a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40d7a-126">INPUTS</span></span>

### <span data-ttu-id="40d7a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="40d7a-127">System.String</span></span>

## <span data-ttu-id="40d7a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40d7a-128">OUTPUTS</span></span>

### <span data-ttu-id="40d7a-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d7a-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="40d7a-130">Note</span><span class="sxs-lookup"><span data-stu-id="40d7a-130">NOTES</span></span>
* <span data-ttu-id="40d7a-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="40d7a-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="40d7a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40d7a-132">RELATED LINKS</span></span>

[<span data-ttu-id="40d7a-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="40d7a-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="40d7a-134">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="40d7a-134">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="40d7a-135">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="40d7a-135">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="40d7a-136">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="40d7a-136">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


