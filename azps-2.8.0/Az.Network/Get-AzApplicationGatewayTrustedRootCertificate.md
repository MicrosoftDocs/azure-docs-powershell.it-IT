---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 1e617ef1283937116bd97c24a968f247fa7552de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853801"
---
# <span data-ttu-id="7f575-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f575-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7f575-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f575-102">SYNOPSIS</span></span>
<span data-ttu-id="7f575-103">Ottiene il certificato radice attendibile con un nome specifico dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f575-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="7f575-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f575-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f575-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f575-105">DESCRIPTION</span></span>
<span data-ttu-id="7f575-106">Il cmdlet **Get-AzApplicationGatewayTrustedRootCertificate** ottiene un certificato radice attendibile con un nome specifico dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f575-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="7f575-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f575-107">EXAMPLES</span></span>

### <span data-ttu-id="7f575-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7f575-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="7f575-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="7f575-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="7f575-110">Il secondo comando ottiene il certificato radice attendibile con un nome specificato dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f575-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="7f575-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f575-111">PARAMETERS</span></span>

### <span data-ttu-id="7f575-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f575-112">-ApplicationGateway</span></span>
<span data-ttu-id="7f575-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f575-113">The applicationGateway</span></span>

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

### <span data-ttu-id="7f575-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f575-114">-DefaultProfile</span></span>
<span data-ttu-id="7f575-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f575-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f575-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f575-116">-Name</span></span>
<span data-ttu-id="7f575-117">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="7f575-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="7f575-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f575-118">CommonParameters</span></span>
<span data-ttu-id="7f575-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f575-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f575-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f575-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f575-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f575-121">INPUTS</span></span>

### <span data-ttu-id="7f575-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f575-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f575-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f575-123">OUTPUTS</span></span>

### <span data-ttu-id="7f575-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f575-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7f575-125">Note</span><span class="sxs-lookup"><span data-stu-id="7f575-125">NOTES</span></span>

## <span data-ttu-id="7f575-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f575-126">RELATED LINKS</span></span>

[<span data-ttu-id="7f575-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f575-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7f575-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f575-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7f575-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f575-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="7f575-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f575-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
