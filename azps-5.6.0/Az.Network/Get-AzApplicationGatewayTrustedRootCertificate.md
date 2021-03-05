---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f040110ea3e00e99b989c07e8757d3c3a0c4b976
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993942"
---
# <span data-ttu-id="56916-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56916-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="56916-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56916-102">SYNOPSIS</span></span>
<span data-ttu-id="56916-103">Recupera il certificato radice attendibile con un nome specifico dal Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="56916-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="56916-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56916-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56916-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56916-105">DESCRIPTION</span></span>
<span data-ttu-id="56916-106">Il cmdlet **Get-AzApplicationGatewayTrustedRootCertificate** ottiene il certificato radice attendibile con un nome specifico dal Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="56916-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="56916-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56916-107">EXAMPLES</span></span>

### <span data-ttu-id="56916-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56916-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="56916-109">Il primo comando recupera il Gateway applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="56916-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="56916-110">Il secondo comando recupera il certificato radice attendibile con un nome specificato dal Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="56916-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="56916-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56916-111">PARAMETERS</span></span>

### <span data-ttu-id="56916-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56916-112">-ApplicationGateway</span></span>
<span data-ttu-id="56916-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56916-113">The applicationGateway</span></span>

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

### <span data-ttu-id="56916-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56916-114">-DefaultProfile</span></span>
<span data-ttu-id="56916-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56916-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56916-116">-Name</span><span class="sxs-lookup"><span data-stu-id="56916-116">-Name</span></span>
<span data-ttu-id="56916-117">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="56916-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56916-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56916-118">CommonParameters</span></span>
<span data-ttu-id="56916-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56916-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56916-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56916-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56916-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="56916-121">INPUTS</span></span>

### <span data-ttu-id="56916-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56916-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="56916-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56916-123">OUTPUTS</span></span>

### <span data-ttu-id="56916-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56916-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="56916-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="56916-125">NOTES</span></span>

## <span data-ttu-id="56916-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56916-126">RELATED LINKS</span></span>

[<span data-ttu-id="56916-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56916-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="56916-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56916-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="56916-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56916-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="56916-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56916-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
