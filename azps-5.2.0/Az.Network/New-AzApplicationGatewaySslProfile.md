---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: a9b0d41ad700d0591e38fa339c38efb85cb00859
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369344"
---
# <span data-ttu-id="46a3d-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="46a3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="46a3d-103">Crea il profilo SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46a3d-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="46a3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46a3d-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46a3d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="46a3d-106">Il cmdlet **New-AzApplicationGatewaySslProfile** crea il profilo SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46a3d-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="46a3d-107">Il profilo SSL è configurato nei listener HTTPS.</span><span class="sxs-lookup"><span data-stu-id="46a3d-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="46a3d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46a3d-108">EXAMPLES</span></span>

### <span data-ttu-id="46a3d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46a3d-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="46a3d-110">Il primo comando crea un nuovo criterio SSL e lo archivia nella variabile $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="46a3d-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="46a3d-111">Il secondo comando crea una catena di certificati CA del client attendibile e li archivia nella variabile $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="46a3d-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="46a3d-112">Il terzo comando crea un nuovo profilo SSL con i criteri SSL e la catena di certificati CA del client attendibile.</span><span class="sxs-lookup"><span data-stu-id="46a3d-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="46a3d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46a3d-113">PARAMETERS</span></span>

### <span data-ttu-id="46a3d-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="46a3d-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="46a3d-115">Impostazioni di configurazione dell'autenticazione client</span><span class="sxs-lookup"><span data-stu-id="46a3d-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-116">-DefaultProfile</span></span>
<span data-ttu-id="46a3d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46a3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a3d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="46a3d-118">-Name</span></span>
<span data-ttu-id="46a3d-119">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="46a3d-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="46a3d-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="46a3d-120">-SslPolicy</span></span>
<span data-ttu-id="46a3d-121">Criteri SSL</span><span class="sxs-lookup"><span data-stu-id="46a3d-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a3d-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="46a3d-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="46a3d-123">Catene di certificati CA client attendibili</span><span class="sxs-lookup"><span data-stu-id="46a3d-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a3d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a3d-124">CommonParameters</span></span>
<span data-ttu-id="46a3d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a3d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a3d-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46a3d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a3d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46a3d-127">INPUTS</span></span>

### <span data-ttu-id="46a3d-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="46a3d-128">None</span></span>

## <span data-ttu-id="46a3d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46a3d-129">OUTPUTS</span></span>

### <span data-ttu-id="46a3d-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="46a3d-131">Note</span><span class="sxs-lookup"><span data-stu-id="46a3d-131">NOTES</span></span>

## <span data-ttu-id="46a3d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46a3d-132">RELATED LINKS</span></span>

[<span data-ttu-id="46a3d-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="46a3d-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="46a3d-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="46a3d-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="46a3d-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)