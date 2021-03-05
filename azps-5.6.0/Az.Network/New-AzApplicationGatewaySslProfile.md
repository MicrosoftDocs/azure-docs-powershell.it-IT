---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 4e58ee2c2f9b7854234913f0cf6ce7c6923f3345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970509"
---
# <span data-ttu-id="c3376-101">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-101">New-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c3376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3376-102">SYNOPSIS</span></span>
<span data-ttu-id="c3376-103">Crea un profilo SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3376-103">Creates SSL profile for an application gateway.</span></span>

## <span data-ttu-id="c3376-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3376-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslProfile -Name <String> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3376-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3376-105">DESCRIPTION</span></span>
<span data-ttu-id="c3376-106">Il cmdlet **New-AzApplicationGatewaySslProfile** crea un profilo SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="c3376-106">The **New-AzApplicationGatewaySslProfile** cmdlet creates SSL profile for an application gateway.</span></span> <span data-ttu-id="c3376-107">Il profilo SSL è configurato nei listener HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c3376-107">The ssl profile is configured on the HTTPS listeners.</span></span>

## <span data-ttu-id="c3376-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3376-108">EXAMPLES</span></span>

### <span data-ttu-id="c3376-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c3376-109">Example 1</span></span>
```powershell
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $profile = New-AzApplicationGatewaySslProfile -Name $sslProfile01Name -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01
```
<span data-ttu-id="c3376-110">Il primo comando crea un nuovo criterio SSL e lo archivia nella $sslPolicy variabile.</span><span class="sxs-lookup"><span data-stu-id="c3376-110">The first command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="c3376-111">Il secondo comando crea catene di certificati CA attendibili del client e le archivia nella variabile $ClientCert 01.</span><span class="sxs-lookup"><span data-stu-id="c3376-111">The second command creates a trusted client CA certificate chains and stores them in the $ClientCert01 variable.</span></span>
<span data-ttu-id="c3376-112">Il terzo comando crea un nuovo profilo SSL con il criterio SSL e la catena di certificati CA del client attendibile.</span><span class="sxs-lookup"><span data-stu-id="c3376-112">The third command create a new SSL profile with the the ssl policy and trusted client CA certificate chain.</span></span>

## <span data-ttu-id="c3376-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3376-113">PARAMETERS</span></span>

### <span data-ttu-id="c3376-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3376-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="c3376-115">Impostazioni di configurazione dell'autenticazione client</span><span class="sxs-lookup"><span data-stu-id="c3376-115">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="c3376-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-116">-DefaultProfile</span></span>
<span data-ttu-id="c3376-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3376-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3376-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c3376-118">-Name</span></span>
<span data-ttu-id="c3376-119">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="c3376-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="c3376-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3376-120">-SslPolicy</span></span>
<span data-ttu-id="c3376-121">Criterio SSL</span><span class="sxs-lookup"><span data-stu-id="c3376-121">SSL policy</span></span>

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

### <span data-ttu-id="c3376-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="c3376-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="c3376-123">Catene di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="c3376-123">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="c3376-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3376-124">CommonParameters</span></span>
<span data-ttu-id="c3376-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3376-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3376-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3376-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3376-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3376-127">INPUTS</span></span>

### <span data-ttu-id="c3376-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3376-128">None</span></span>

## <span data-ttu-id="c3376-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3376-129">OUTPUTS</span></span>

### <span data-ttu-id="c3376-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="c3376-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3376-131">NOTES</span></span>

## <span data-ttu-id="c3376-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3376-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3376-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="c3376-134">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-134">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="c3376-135">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-135">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="c3376-136">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="c3376-136">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)