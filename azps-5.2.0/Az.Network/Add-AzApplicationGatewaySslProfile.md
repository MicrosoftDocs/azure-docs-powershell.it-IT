---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 8930041959712b7533651262a39409e884ffb177
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362946"
---
# <span data-ttu-id="5f65a-101">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5f65a-101">Add-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="5f65a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f65a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f65a-103">Aggiunge il profilo SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f65a-103">Adds SSL profile to an application gateway.</span></span>

## <span data-ttu-id="5f65a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f65a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f65a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f65a-105">DESCRIPTION</span></span>
<span data-ttu-id="5f65a-106">Il cmdlet **Add-AzApplicationGatewaySslProfile** aggiunge un profilo SSL a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f65a-106">The **Add-AzApplicationGatewaySslProfile** cmdlet adds a SSL profile to an application gateway.</span></span> <span data-ttu-id="5f65a-107">Il profilo SSL viene applicato ai listener HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5f65a-107">The SSL profile is applied to HTTPS Listeners.</span></span>

## <span data-ttu-id="5f65a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f65a-108">EXAMPLES</span></span>

### <span data-ttu-id="5f65a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5f65a-109">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
PS C:\> $trustedClient01 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert01" -CertificateFile "C:\clientCAChain1.cer"
PS C:\> $trustedClient02 = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert02" -CertificateFile "C:\clientCAChain2.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfile01Name -ApplicationGateway $AppGw -SslPolicy $sslPolicy -TrustedClientCertificates $trustedClient01,$trustedClient02
```

<span data-ttu-id="5f65a-110">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5f65a-110">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5f65a-111">Il secondo comando crea un nuovo criterio SSL e lo archivia nella variabile $sslPolicy.</span><span class="sxs-lookup"><span data-stu-id="5f65a-111">The second command creates a new SSL policy and stores it in the $sslPolicy variable.</span></span>
<span data-ttu-id="5f65a-112">Il terzo e il quarto comando crea due nuove catene di certificati CA client attendibili e le archivia nelle variabili $ClientCert 01 e $ClientCert 02.</span><span class="sxs-lookup"><span data-stu-id="5f65a-112">The third and fourth command creates two new trusted client CA certificate chains and stores them in the $ClientCert01 and $ClientCert02 variables.</span></span>
<span data-ttu-id="5f65a-113">Il quinto comando aggiunge il profilo SSL con il criterio SSL e le catene di certificati CA del client trusted per il gateway dell'applicazione $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5f65a-113">The fifth command adds the SSL profile with the the ssl policy and trusted client CA certificate chains to the application gateway $AppGw.</span></span>

## <span data-ttu-id="5f65a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f65a-114">PARAMETERS</span></span>

### <span data-ttu-id="5f65a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f65a-115">-ApplicationGateway</span></span>
<span data-ttu-id="5f65a-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f65a-116">The applicationGateway</span></span>

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

### <span data-ttu-id="5f65a-117">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f65a-117">-ClientAuthConfiguration</span></span>
<span data-ttu-id="5f65a-118">Impostazioni di configurazione dell'autenticazione client</span><span class="sxs-lookup"><span data-stu-id="5f65a-118">Client authentication configuration settings</span></span>

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

### <span data-ttu-id="5f65a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f65a-119">-DefaultProfile</span></span>
<span data-ttu-id="5f65a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f65a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f65a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f65a-121">-Name</span></span>
<span data-ttu-id="5f65a-122">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="5f65a-122">The name of the SSL profile</span></span>

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

### <span data-ttu-id="5f65a-123">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="5f65a-123">-SslPolicy</span></span>
<span data-ttu-id="5f65a-124">Criteri SSL</span><span class="sxs-lookup"><span data-stu-id="5f65a-124">SSL policy</span></span>

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

### <span data-ttu-id="5f65a-125">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="5f65a-125">-TrustedClientCertificates</span></span>
<span data-ttu-id="5f65a-126">Catene di certificati CA client attendibili</span><span class="sxs-lookup"><span data-stu-id="5f65a-126">The trusted client CA certificate chains</span></span>

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

### <span data-ttu-id="5f65a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f65a-127">CommonParameters</span></span>
<span data-ttu-id="5f65a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f65a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f65a-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f65a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f65a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f65a-130">INPUTS</span></span>

### <span data-ttu-id="5f65a-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f65a-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f65a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f65a-132">OUTPUTS</span></span>

### <span data-ttu-id="5f65a-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f65a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f65a-134">Note</span><span class="sxs-lookup"><span data-stu-id="5f65a-134">NOTES</span></span>

## <span data-ttu-id="5f65a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f65a-135">RELATED LINKS</span></span>

[<span data-ttu-id="5f65a-136">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5f65a-136">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="5f65a-137">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5f65a-137">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="5f65a-138">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5f65a-138">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="5f65a-139">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="5f65a-139">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)