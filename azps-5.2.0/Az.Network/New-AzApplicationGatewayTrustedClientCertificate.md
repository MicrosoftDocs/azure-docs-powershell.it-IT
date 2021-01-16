---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360989"
---
# <span data-ttu-id="62d85-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62d85-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="62d85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62d85-102">SYNOPSIS</span></span>
<span data-ttu-id="62d85-103">Crea una catena di certificati CA client attendibile per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62d85-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="62d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62d85-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62d85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62d85-105">DESCRIPTION</span></span>
<span data-ttu-id="62d85-106">Il cmdlet New-AzApplicationGatewayTrustedClientCertificate crea una catena di certificati CA client attendibile per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62d85-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="62d85-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62d85-107">EXAMPLES</span></span>

### <span data-ttu-id="62d85-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62d85-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="62d85-109">Il comando crea un nuovo oggetto della catena di certificati CA del client attendibile che sta prendendo il percorso del certificato della CA client come input.</span><span class="sxs-lookup"><span data-stu-id="62d85-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="62d85-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62d85-110">PARAMETERS</span></span>

### <span data-ttu-id="62d85-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="62d85-111">-CertificateFile</span></span>
<span data-ttu-id="62d85-112">Percorso del file della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="62d85-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="62d85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d85-113">-DefaultProfile</span></span>
<span data-ttu-id="62d85-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62d85-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d85-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="62d85-115">-Name</span></span>
<span data-ttu-id="62d85-116">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="62d85-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="62d85-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62d85-117">-Confirm</span></span>
<span data-ttu-id="62d85-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62d85-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62d85-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d85-119">-WhatIf</span></span>
<span data-ttu-id="62d85-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62d85-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d85-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62d85-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62d85-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d85-122">CommonParameters</span></span>
<span data-ttu-id="62d85-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62d85-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d85-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62d85-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d85-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62d85-125">INPUTS</span></span>

### <span data-ttu-id="62d85-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="62d85-126">None</span></span>

## <span data-ttu-id="62d85-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62d85-127">OUTPUTS</span></span>

### <span data-ttu-id="62d85-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62d85-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="62d85-129">Note</span><span class="sxs-lookup"><span data-stu-id="62d85-129">NOTES</span></span>

## <span data-ttu-id="62d85-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62d85-130">RELATED LINKS</span></span>

[<span data-ttu-id="62d85-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62d85-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="62d85-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62d85-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="62d85-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62d85-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="62d85-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="62d85-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)