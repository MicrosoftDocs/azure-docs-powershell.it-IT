---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 4d664018592f05203c684a896f0a0701940301a6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866505"
---
# <span data-ttu-id="f4331-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4331-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="f4331-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4331-102">SYNOPSIS</span></span>
<span data-ttu-id="f4331-103">Aggiunge un certificato di autenticazione a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4331-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4331-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4331-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4331-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4331-105">DESCRIPTION</span></span>
<span data-ttu-id="f4331-106">Il cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** aggiunge un certificato di autenticazione a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="f4331-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="f4331-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4331-107">EXAMPLES</span></span>

### <span data-ttu-id="f4331-108">1:</span><span class="sxs-lookup"><span data-stu-id="f4331-108">1:</span></span>
```

```

## <span data-ttu-id="f4331-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4331-109">PARAMETERS</span></span>

### <span data-ttu-id="f4331-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4331-110">-ApplicationGateway</span></span>
<span data-ttu-id="f4331-111">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiunge un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f4331-111">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="f4331-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f4331-112">-CertificateFile</span></span>
<span data-ttu-id="f4331-113">Specifica il percorso del certificato di autenticazione aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4331-113">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f4331-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4331-114">-DefaultProfile</span></span>
<span data-ttu-id="f4331-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4331-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4331-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4331-116">-Name</span></span>
<span data-ttu-id="f4331-117">Specifica il nome di un certificato aggiunto dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4331-117">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="f4331-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4331-118">-Confirm</span></span>
<span data-ttu-id="f4331-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4331-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4331-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4331-120">-WhatIf</span></span>
<span data-ttu-id="f4331-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4331-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4331-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4331-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4331-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4331-123">CommonParameters</span></span>
<span data-ttu-id="f4331-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4331-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4331-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4331-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4331-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4331-126">INPUTS</span></span>

### <span data-ttu-id="f4331-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f4331-127">System.String</span></span>

## <span data-ttu-id="f4331-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4331-128">OUTPUTS</span></span>

### <span data-ttu-id="f4331-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f4331-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f4331-130">Note</span><span class="sxs-lookup"><span data-stu-id="f4331-130">NOTES</span></span>
* <span data-ttu-id="f4331-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="f4331-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f4331-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4331-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4331-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4331-133">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f4331-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4331-134">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f4331-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4331-135">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="f4331-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="f4331-136">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


