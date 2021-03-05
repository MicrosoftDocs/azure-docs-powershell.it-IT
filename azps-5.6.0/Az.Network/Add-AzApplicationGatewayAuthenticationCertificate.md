---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38855E74-F30C-43DF-8D94-ABD7872BCE11
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: ba0d82ab04f8e0c990c7bbf15facb3ee725f7609
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968061"
---
# <span data-ttu-id="bd58b-101">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd58b-101">Add-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="bd58b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd58b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd58b-103">Aggiunge un certificato di autenticazione a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd58b-103">Adds an authentication certificate to an application gateway.</span></span>

## <span data-ttu-id="bd58b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd58b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd58b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd58b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd58b-106">Il cmdlet **Add-AzApplicationGatewayAuthenticationCertificate aggiunge** un certificato di autenticazione a un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bd58b-106">The **Add-AzApplicationGatewayAuthenticationCertificate** cmdlet adds an authentication certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="bd58b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd58b-107">EXAMPLES</span></span>

### <span data-ttu-id="bd58b-108">Esempio 1: Aggiungere il certificato di autenticazione a un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="bd58b-108">Example 1: Add authentication certificate to an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Add-AzApplicationGatewayAuthenticationCertificate -ApplicationGateway $appgw -Name "cert01" -CertificateFile "C:\cert.cer"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="bd58b-109">Il primo comando ottiene un gateway applicazione denominato appGwName e lo archivia in $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="bd58b-109">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="bd58b-110">Il secondo comando aggiunge il certificato di autenticazione denominato cert01 al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd58b-110">The second command adds authentication certificate named cert01 to the application gateway.</span></span>
<span data-ttu-id="bd58b-111">Il terzo comando aggiorna il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd58b-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="bd58b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd58b-112">PARAMETERS</span></span>

### <span data-ttu-id="bd58b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd58b-113">-ApplicationGateway</span></span>
<span data-ttu-id="bd58b-114">Specifica il nome del gateway applicazione per cui questo cmdlet aggiunge un certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="bd58b-114">Specifies the name of application gateway for which this cmdlet adds an authentication certificate.</span></span>

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

### <span data-ttu-id="bd58b-115">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="bd58b-115">-CertificateFile</span></span>
<span data-ttu-id="bd58b-116">Specifica il percorso del certificato di autenticazione aggiunto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd58b-116">Specifies the path of the authentication certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="bd58b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd58b-117">-DefaultProfile</span></span>
<span data-ttu-id="bd58b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd58b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd58b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bd58b-119">-Name</span></span>
<span data-ttu-id="bd58b-120">Specifica il nome di un certificato che questo cmdlet aggiunge al gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bd58b-120">Specifies the name of a certificate that this cmdlet adds to the application gateway.</span></span>

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

### <span data-ttu-id="bd58b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd58b-121">-Confirm</span></span>
<span data-ttu-id="bd58b-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd58b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd58b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd58b-123">-WhatIf</span></span>
<span data-ttu-id="bd58b-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd58b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd58b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd58b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd58b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd58b-126">CommonParameters</span></span>
<span data-ttu-id="bd58b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd58b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd58b-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd58b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd58b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd58b-129">INPUTS</span></span>

### <span data-ttu-id="bd58b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd58b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bd58b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd58b-131">OUTPUTS</span></span>

### <span data-ttu-id="bd58b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd58b-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bd58b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd58b-133">NOTES</span></span>
* <span data-ttu-id="bd58b-134">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="bd58b-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bd58b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd58b-135">RELATED LINKS</span></span>

[<span data-ttu-id="bd58b-136">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd58b-136">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd58b-137">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd58b-137">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd58b-138">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd58b-138">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="bd58b-139">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="bd58b-139">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


