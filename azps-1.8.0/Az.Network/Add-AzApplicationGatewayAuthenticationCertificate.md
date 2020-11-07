---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1a1d484d3b8d23633393c0f300f84091b06c1d0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678714"
---
# <span data-ttu-id="47afd-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47afd-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="47afd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47afd-102">SYNOPSIS</span></span>
<span data-ttu-id="47afd-103">Aggiunge un certificato di autenticazione a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47afd-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="47afd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47afd-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47afd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47afd-105">DESCRIPTION</span></span>
<span data-ttu-id="47afd-106">Il cmdlet **Add-AzApplicationGatewayAuthenticationCertificate** aggiunge un certificato di autenticazione a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="47afd-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="47afd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47afd-107">EXAMPLES</span></span>

### <span data-ttu-id="47afd-108">Esempio 1: aggiungere un certificato di autenticazione a un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="47afd-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="47afd-109">Il primo comando ottiene un gateway dell'applicazione denominato appGwName e lo archivia in $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="47afd-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="47afd-110">Il secondo comando aggiunge il certificato di autenticazione denominato cert01 al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47afd-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="47afd-111">Il terzo comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47afd-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="47afd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47afd-112">PARAMETERS</span></span>

### <span data-ttu-id="47afd-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47afd-113">-ApplicationGateway</span></span>
<span data-ttu-id="47afd-114">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiunge un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="47afd-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="47afd-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="47afd-115">-CertificateFile</span></span>
<span data-ttu-id="47afd-116">Specifica il percorso del certificato di autenticazione aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47afd-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="47afd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47afd-117">-DefaultProfile</span></span>
<span data-ttu-id="47afd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47afd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47afd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="47afd-119">-Name</span></span>
<span data-ttu-id="47afd-120">Specifica il nome di un certificato aggiunto dal cmdlet al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="47afd-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="47afd-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47afd-121">-Confirm</span></span>
<span data-ttu-id="47afd-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47afd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47afd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47afd-123">-WhatIf</span></span>
<span data-ttu-id="47afd-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47afd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47afd-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47afd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47afd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47afd-126">CommonParameters</span></span>
<span data-ttu-id="47afd-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47afd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47afd-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47afd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47afd-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47afd-129">INPUTS</span></span>

### <span data-ttu-id="47afd-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47afd-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47afd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47afd-131">OUTPUTS</span></span>

### <span data-ttu-id="47afd-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47afd-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47afd-133">Note</span><span class="sxs-lookup"><span data-stu-id="47afd-133">NOTES</span></span>
* <span data-ttu-id="47afd-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="47afd-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="47afd-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47afd-135">RELATED LINKS</span></span>

[<span data-ttu-id="47afd-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47afd-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47afd-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47afd-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47afd-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47afd-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="47afd-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47afd-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)

