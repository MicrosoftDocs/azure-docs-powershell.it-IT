---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 317fd5bf8306416ad4cbef3d1fb64d56d556ed1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515635"
---
# <span data-ttu-id="7e1d2-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e1d2-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7e1d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7e1d2-103">Aggiunge un certificato di autenticazione a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e1d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e1d2-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e1d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e1d2-105">DESCRIPTION</span></span>
<span data-ttu-id="7e1d2-106">Il cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** aggiunge un certificato di autenticazione a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="7e1d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e1d2-107">EXAMPLES</span></span>

## <span data-ttu-id="7e1d2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e1d2-108">PARAMETERS</span></span>

### <span data-ttu-id="7e1d2-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e1d2-109">-ApplicationGateway</span></span>
<span data-ttu-id="7e1d2-110">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiunge un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="7e1d2-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7e1d2-111">-CertificateFile</span></span>
<span data-ttu-id="7e1d2-112">Specifica il percorso del certificato di autenticazione aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="7e1d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e1d2-113">-DefaultProfile</span></span>
<span data-ttu-id="7e1d2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e1d2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e1d2-115">-Name</span></span>
<span data-ttu-id="7e1d2-116">Specifica il nome di un certificato aggiunto dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-116">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="7e1d2-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7e1d2-117">-Confirm</span></span>
<span data-ttu-id="7e1d2-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e1d2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e1d2-119">-WhatIf</span></span>
<span data-ttu-id="7e1d2-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e1d2-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e1d2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e1d2-122">CommonParameters</span></span>
<span data-ttu-id="7e1d2-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e1d2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e1d2-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e1d2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e1d2-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e1d2-125">INPUTS</span></span>

### <span data-ttu-id="7e1d2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7e1d2-126">System.String</span></span>

## <span data-ttu-id="7e1d2-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e1d2-127">OUTPUTS</span></span>

### <span data-ttu-id="7e1d2-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e1d2-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e1d2-129">Note</span><span class="sxs-lookup"><span data-stu-id="7e1d2-129">NOTES</span></span>
* <span data-ttu-id="7e1d2-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="7e1d2-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7e1d2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e1d2-131">RELATED LINKS</span></span>

[<span data-ttu-id="7e1d2-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e1d2-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7e1d2-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e1d2-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7e1d2-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e1d2-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7e1d2-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7e1d2-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


