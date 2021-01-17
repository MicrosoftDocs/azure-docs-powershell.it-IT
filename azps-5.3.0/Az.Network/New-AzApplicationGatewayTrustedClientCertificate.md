---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474543"
---
# <span data-ttu-id="6c2a6-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6c2a6-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="6c2a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c2a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2a6-103">Crea una catena di certificati CA client attendibile per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="6c2a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c2a6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c2a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c2a6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c2a6-106">Il cmdlet New-AzApplicationGatewayTrustedClientCertificate crea una catena di certificati CA client attendibile per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="6c2a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c2a6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c2a6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c2a6-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="6c2a6-109">Il comando crea un nuovo oggetto della catena di certificati CA del client attendibile che sta prendendo il percorso del certificato della CA client come input.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="6c2a6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c2a6-110">PARAMETERS</span></span>

### <span data-ttu-id="6c2a6-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6c2a6-111">-CertificateFile</span></span>
<span data-ttu-id="6c2a6-112">Percorso del file della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="6c2a6-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="6c2a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2a6-113">-DefaultProfile</span></span>
<span data-ttu-id="6c2a6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2a6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c2a6-115">-Name</span></span>
<span data-ttu-id="6c2a6-116">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="6c2a6-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="6c2a6-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c2a6-117">-Confirm</span></span>
<span data-ttu-id="6c2a6-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c2a6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c2a6-119">-WhatIf</span></span>
<span data-ttu-id="6c2a6-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c2a6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c2a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2a6-122">CommonParameters</span></span>
<span data-ttu-id="6c2a6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2a6-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c2a6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2a6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c2a6-125">INPUTS</span></span>

### <span data-ttu-id="6c2a6-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6c2a6-126">None</span></span>

## <span data-ttu-id="6c2a6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c2a6-127">OUTPUTS</span></span>

### <span data-ttu-id="6c2a6-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6c2a6-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="6c2a6-129">Note</span><span class="sxs-lookup"><span data-stu-id="6c2a6-129">NOTES</span></span>

## <span data-ttu-id="6c2a6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c2a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="6c2a6-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6c2a6-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="6c2a6-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6c2a6-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="6c2a6-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6c2a6-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="6c2a6-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="6c2a6-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)