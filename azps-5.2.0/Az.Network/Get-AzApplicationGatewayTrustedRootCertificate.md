---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337999"
---
# <span data-ttu-id="82b4e-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="82b4e-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="82b4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="82b4e-103">Ottiene il certificato radice attendibile con un nome specifico dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82b4e-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="82b4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82b4e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b4e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="82b4e-106">Il cmdlet **Get-AzApplicationGatewayTrustedRootCertificate** ottiene un certificato radice attendibile con un nome specifico dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82b4e-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="82b4e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82b4e-107">EXAMPLES</span></span>

### <span data-ttu-id="82b4e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82b4e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="82b4e-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="82b4e-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="82b4e-110">Il secondo comando ottiene il certificato radice attendibile con un nome specificato dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="82b4e-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="82b4e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82b4e-111">PARAMETERS</span></span>

### <span data-ttu-id="82b4e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82b4e-112">-ApplicationGateway</span></span>
<span data-ttu-id="82b4e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82b4e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="82b4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b4e-114">-DefaultProfile</span></span>
<span data-ttu-id="82b4e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82b4e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b4e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="82b4e-116">-Name</span></span>
<span data-ttu-id="82b4e-117">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="82b4e-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="82b4e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b4e-118">CommonParameters</span></span>
<span data-ttu-id="82b4e-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b4e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b4e-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82b4e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b4e-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82b4e-121">INPUTS</span></span>

### <span data-ttu-id="82b4e-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82b4e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82b4e-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82b4e-123">OUTPUTS</span></span>

### <span data-ttu-id="82b4e-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="82b4e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="82b4e-125">Note</span><span class="sxs-lookup"><span data-stu-id="82b4e-125">NOTES</span></span>

## <span data-ttu-id="82b4e-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82b4e-126">RELATED LINKS</span></span>

[<span data-ttu-id="82b4e-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="82b4e-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="82b4e-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="82b4e-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="82b4e-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="82b4e-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="82b4e-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="82b4e-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
