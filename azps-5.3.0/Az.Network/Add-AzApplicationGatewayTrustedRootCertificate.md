---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380222"
---
# <span data-ttu-id="9b048-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9b048-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="9b048-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b048-102">SYNOPSIS</span></span>
<span data-ttu-id="9b048-103">Aggiunge un certificato radice attendibile a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b048-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="9b048-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b048-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b048-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b048-105">DESCRIPTION</span></span>
<span data-ttu-id="9b048-106">Il cmdlet **Add-AzApplicationGatewayTrustedRootCertificate** aggiunge un certificato radice attendibile a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="9b048-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="9b048-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b048-107">EXAMPLES</span></span>

### <span data-ttu-id="9b048-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b048-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="9b048-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="9b048-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="9b048-110">Il secondo comando aggiunge un nuovo certificato radice attendibile al gateway dell'applicazione che prende il percorso del certificato radice come input.</span><span class="sxs-lookup"><span data-stu-id="9b048-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="9b048-111">Il terzo comando crea una nuova impostazione http backend usando il certificato radice attendibile per la convalida del certificato del server back-end.</span><span class="sxs-lookup"><span data-stu-id="9b048-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="9b048-112">Il quarto comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b048-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="9b048-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b048-113">PARAMETERS</span></span>

### <span data-ttu-id="9b048-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b048-114">-ApplicationGateway</span></span>
<span data-ttu-id="9b048-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b048-115">The applicationGateway</span></span>

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

### <span data-ttu-id="9b048-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9b048-116">-CertificateFile</span></span>
<span data-ttu-id="9b048-117">Percorso del file CER certificato</span><span class="sxs-lookup"><span data-stu-id="9b048-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="9b048-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b048-118">-DefaultProfile</span></span>
<span data-ttu-id="9b048-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b048-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b048-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b048-120">-Name</span></span>
<span data-ttu-id="9b048-121">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="9b048-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="9b048-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b048-122">-Confirm</span></span>
<span data-ttu-id="9b048-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b048-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b048-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b048-124">-WhatIf</span></span>
<span data-ttu-id="9b048-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b048-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b048-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b048-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b048-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b048-127">CommonParameters</span></span>
<span data-ttu-id="9b048-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b048-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b048-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b048-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b048-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b048-130">INPUTS</span></span>

### <span data-ttu-id="9b048-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b048-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b048-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b048-132">OUTPUTS</span></span>

### <span data-ttu-id="9b048-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b048-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b048-134">Note</span><span class="sxs-lookup"><span data-stu-id="9b048-134">NOTES</span></span>

## <span data-ttu-id="9b048-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b048-135">RELATED LINKS</span></span>

[<span data-ttu-id="9b048-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9b048-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="9b048-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9b048-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="9b048-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9b048-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="9b048-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9b048-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
