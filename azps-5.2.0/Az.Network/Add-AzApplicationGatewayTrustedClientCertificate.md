---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346648"
---
# <span data-ttu-id="1a7ed-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1a7ed-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="1a7ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a7ed-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7ed-103">Aggiunge una catena di certificati CA client attendibile a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="1a7ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a7ed-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a7ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a7ed-105">DESCRIPTION</span></span>
<span data-ttu-id="1a7ed-106">Il cmdlet **Add-AzApplicationGatewayTrustedClientCertificate** aggiunge una catena di certificati CA client attendibile a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="1a7ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a7ed-107">EXAMPLES</span></span>

### <span data-ttu-id="1a7ed-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a7ed-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="1a7ed-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="1a7ed-110">Il secondo comando crea una nuova catena di certificati CA del client attendibile che prende il percorso del certificato della CA client come input.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="1a7ed-111">Il terzo comando crea un profilo SSL usando un certificato client attendibile.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="1a7ed-112">Il quarto comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="1a7ed-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a7ed-113">PARAMETERS</span></span>

### <span data-ttu-id="1a7ed-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a7ed-114">-ApplicationGateway</span></span>
<span data-ttu-id="1a7ed-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a7ed-115">The applicationGateway</span></span>

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

### <span data-ttu-id="1a7ed-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1a7ed-116">-CertificateFile</span></span>
<span data-ttu-id="1a7ed-117">Percorso del file della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="1a7ed-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="1a7ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a7ed-118">-DefaultProfile</span></span>
<span data-ttu-id="1a7ed-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7ed-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a7ed-120">-Name</span></span>
<span data-ttu-id="1a7ed-121">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="1a7ed-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="1a7ed-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1a7ed-122">-Confirm</span></span>
<span data-ttu-id="1a7ed-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a7ed-124">-WhatIf</span></span>
<span data-ttu-id="1a7ed-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a7ed-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7ed-127">CommonParameters</span></span>
<span data-ttu-id="1a7ed-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a7ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7ed-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a7ed-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7ed-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a7ed-130">INPUTS</span></span>

### <span data-ttu-id="1a7ed-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a7ed-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a7ed-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a7ed-132">OUTPUTS</span></span>

### <span data-ttu-id="1a7ed-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a7ed-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a7ed-134">Note</span><span class="sxs-lookup"><span data-stu-id="1a7ed-134">NOTES</span></span>

## <span data-ttu-id="1a7ed-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a7ed-135">RELATED LINKS</span></span>

[<span data-ttu-id="1a7ed-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1a7ed-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1a7ed-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1a7ed-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1a7ed-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1a7ed-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1a7ed-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1a7ed-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)