---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192031"
---
# <span data-ttu-id="73a77-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73a77-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="73a77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73a77-102">SYNOPSIS</span></span>
<span data-ttu-id="73a77-103">Aggiunge un certificato radice attendibile a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="73a77-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="73a77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73a77-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a77-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="73a77-105">DESCRIPTION</span></span>
<span data-ttu-id="73a77-106">Il cmdlet **Add-AzApplicationGatewayTrustedRootCertificate aggiunge** un certificato radice attendibile a un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="73a77-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="73a77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73a77-107">EXAMPLES</span></span>

### <span data-ttu-id="73a77-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="73a77-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="73a77-109">Il primo comando recupera il gateway applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="73a77-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="73a77-110">Il secondo comando aggiunge un nuovo certificato radice attendibile al Gateway applicazione, prendendo come input il percorso del certificato radice.</span><span class="sxs-lookup"><span data-stu-id="73a77-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="73a77-111">Il terzo comando crea una nuova impostazione HTTP back-end usando il certificato radice attendibile per convalidare il certificato del server back-end.</span><span class="sxs-lookup"><span data-stu-id="73a77-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="73a77-112">Il quarto comando aggiorna il Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="73a77-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="73a77-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73a77-113">PARAMETERS</span></span>

### <span data-ttu-id="73a77-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73a77-114">-ApplicationGateway</span></span>
<span data-ttu-id="73a77-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73a77-115">The applicationGateway</span></span>

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

### <span data-ttu-id="73a77-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="73a77-116">-CertificateFile</span></span>
<span data-ttu-id="73a77-117">Percorso del file CER del certificato</span><span class="sxs-lookup"><span data-stu-id="73a77-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="73a77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a77-118">-DefaultProfile</span></span>
<span data-ttu-id="73a77-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73a77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73a77-120">-Name</span><span class="sxs-lookup"><span data-stu-id="73a77-120">-Name</span></span>
<span data-ttu-id="73a77-121">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="73a77-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="73a77-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73a77-122">-Confirm</span></span>
<span data-ttu-id="73a77-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73a77-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a77-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a77-124">-WhatIf</span></span>
<span data-ttu-id="73a77-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73a77-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a77-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="73a77-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a77-127">CommonParameters</span></span>
<span data-ttu-id="73a77-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a77-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a77-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a77-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="73a77-130">INPUTS</span></span>

### <span data-ttu-id="73a77-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73a77-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73a77-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73a77-132">OUTPUTS</span></span>

### <span data-ttu-id="73a77-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73a77-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73a77-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="73a77-134">NOTES</span></span>

## <span data-ttu-id="73a77-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73a77-135">RELATED LINKS</span></span>

[<span data-ttu-id="73a77-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73a77-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="73a77-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73a77-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="73a77-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73a77-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="73a77-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="73a77-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
