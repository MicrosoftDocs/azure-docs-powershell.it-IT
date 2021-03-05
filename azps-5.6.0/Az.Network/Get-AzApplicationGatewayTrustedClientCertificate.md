---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: b9522cf7bc29f01215cbac7473c58643b8d63b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993955"
---
# <span data-ttu-id="39abf-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39abf-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="39abf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39abf-102">SYNOPSIS</span></span>
<span data-ttu-id="39abf-103">Recupera la catena di certificati CA del client attendibile con un nome specifico dal Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="39abf-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="39abf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39abf-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39abf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39abf-105">DESCRIPTION</span></span>
<span data-ttu-id="39abf-106">Il cmdlet Get-AzApplicationGatewayTrustedClientCertificate recupera la catena di certificati CA del client attendibile con un nome specifico dal Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="39abf-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="39abf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39abf-107">EXAMPLES</span></span>

### <span data-ttu-id="39abf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39abf-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="39abf-109">Il primo comando recupera il Gateway applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="39abf-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="39abf-110">Il secondo comando recupera la catena di certificati CA del client attendibile con un nome specificato dal Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="39abf-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="39abf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39abf-111">PARAMETERS</span></span>

### <span data-ttu-id="39abf-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39abf-112">-ApplicationGateway</span></span>
<span data-ttu-id="39abf-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39abf-113">The applicationGateway</span></span>

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

### <span data-ttu-id="39abf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39abf-114">-DefaultProfile</span></span>
<span data-ttu-id="39abf-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39abf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39abf-116">-Name</span><span class="sxs-lookup"><span data-stu-id="39abf-116">-Name</span></span>
<span data-ttu-id="39abf-117">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="39abf-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39abf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39abf-118">CommonParameters</span></span>
<span data-ttu-id="39abf-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39abf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39abf-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39abf-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39abf-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="39abf-121">INPUTS</span></span>

### <span data-ttu-id="39abf-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39abf-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="39abf-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39abf-123">OUTPUTS</span></span>

### <span data-ttu-id="39abf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39abf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="39abf-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="39abf-125">NOTES</span></span>

## <span data-ttu-id="39abf-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39abf-126">RELATED LINKS</span></span>

[<span data-ttu-id="39abf-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39abf-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="39abf-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39abf-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="39abf-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39abf-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="39abf-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="39abf-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)