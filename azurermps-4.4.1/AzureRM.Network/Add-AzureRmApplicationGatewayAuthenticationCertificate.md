---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 271eaf702165c3c1e80243efa080b3e4d981390d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519144"
---
# <span data-ttu-id="8d731-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d731-101">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="8d731-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d731-102">SYNOPSIS</span></span>
<span data-ttu-id="8d731-103">Aggiunge un certificato di autenticazione a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d731-103">Adds an authentication certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d731-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d731-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway>
 -Name <String> -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d731-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d731-105">DESCRIPTION</span></span>
<span data-ttu-id="8d731-106">Il cmdlet **Add-AzureRmApplicationGatewayAuthenticationCertificate** aggiunge un certificato di autenticazione a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="8d731-106">The **Add-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="8d731-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d731-107">EXAMPLES</span></span>

## <span data-ttu-id="8d731-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d731-108">PARAMETERS</span></span>

### <span data-ttu-id="8d731-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d731-109">-ApplicationGateway</span></span>
<span data-ttu-id="8d731-110">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiunge un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8d731-110">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d731-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="8d731-111">-CertificateFile</span></span>
<span data-ttu-id="8d731-112">Specifica il percorso del certificato di autenticazione aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d731-112">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d731-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d731-113">-Name</span></span>
<span data-ttu-id="8d731-114">Specifica il nome di un certificato aggiunto dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d731-114">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d731-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8d731-115">-Confirm</span></span>
<span data-ttu-id="8d731-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d731-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d731-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d731-117">-WhatIf</span></span>
<span data-ttu-id="8d731-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d731-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d731-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d731-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d731-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d731-120">-DefaultProfile</span></span>
<span data-ttu-id="8d731-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d731-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d731-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d731-122">CommonParameters</span></span>
<span data-ttu-id="8d731-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d731-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d731-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d731-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d731-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d731-125">INPUTS</span></span>

### <span data-ttu-id="8d731-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8d731-126">System.String</span></span>

## <span data-ttu-id="8d731-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d731-127">OUTPUTS</span></span>

### <span data-ttu-id="8d731-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d731-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d731-129">Note</span><span class="sxs-lookup"><span data-stu-id="8d731-129">NOTES</span></span>
* <span data-ttu-id="8d731-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="8d731-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8d731-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d731-131">RELATED LINKS</span></span>

[<span data-ttu-id="8d731-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d731-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d731-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d731-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d731-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d731-134">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="8d731-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8d731-135">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


