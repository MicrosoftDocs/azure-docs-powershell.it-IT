---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: c4c2c2041c6bf21aa6bf8b13055d0dac5ffbc64a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010414"
---
# <span data-ttu-id="5388e-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5388e-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5388e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5388e-102">SYNOPSIS</span></span>
<span data-ttu-id="5388e-103">Crea un certificato di autenticazione per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="5388e-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="5388e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5388e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5388e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5388e-105">DESCRIPTION</span></span>
<span data-ttu-id="5388e-106">Il cmdlet **New-AzApplicationGatewayAuthenticationCertificate crea** un certificato di autenticazione per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5388e-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="5388e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5388e-107">EXAMPLES</span></span>

### <span data-ttu-id="5388e-108">Esempio 1: Creare un certificato di autenticazione</span><span class="sxs-lookup"><span data-stu-id="5388e-108">Example 1: Create an authentication certificate</span></span>
```
PS C:\> $cert = New-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -CertificateFile "C:\cert.cer"
```

<span data-ttu-id="5388e-109">Il primo comando crea il certificato di autenticazione denominato cert01.</span><span class="sxs-lookup"><span data-stu-id="5388e-109">The first command creates authentication certificate named cert01.</span></span>

## <span data-ttu-id="5388e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5388e-110">PARAMETERS</span></span>

### <span data-ttu-id="5388e-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="5388e-111">-CertificateFile</span></span>
<span data-ttu-id="5388e-112">Specifica il percorso del certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5388e-112">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="5388e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5388e-113">-DefaultProfile</span></span>
<span data-ttu-id="5388e-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5388e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5388e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5388e-115">-Name</span></span>
<span data-ttu-id="5388e-116">Specifica un nome per il certificato di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5388e-116">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="5388e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5388e-117">-Confirm</span></span>
<span data-ttu-id="5388e-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5388e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5388e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5388e-119">-WhatIf</span></span>
<span data-ttu-id="5388e-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5388e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5388e-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5388e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5388e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5388e-122">CommonParameters</span></span>
<span data-ttu-id="5388e-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5388e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5388e-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5388e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5388e-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="5388e-125">INPUTS</span></span>

### <span data-ttu-id="5388e-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5388e-126">None</span></span>

## <span data-ttu-id="5388e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5388e-127">OUTPUTS</span></span>

### <span data-ttu-id="5388e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5388e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="5388e-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="5388e-129">NOTES</span></span>
* <span data-ttu-id="5388e-130">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="5388e-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5388e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5388e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5388e-132">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5388e-132">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5388e-133">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5388e-133">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5388e-134">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5388e-134">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="5388e-135">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="5388e-135">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


