---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686913"
---
# <span data-ttu-id="fc1ee-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fc1ee-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fc1ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1ee-103">Ottiene il certificato radice attendibile con un nome specifico dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc1ee-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc1ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc1ee-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc1ee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc1ee-105">DESCRIPTION</span></span>
<span data-ttu-id="fc1ee-106">Il cmdlet **Get-AzureRmApplicationGatewayTrustedRootCertificate** ottiene un certificato radice attendibile con un nome specifico dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc1ee-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="fc1ee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc1ee-107">EXAMPLES</span></span>

### <span data-ttu-id="fc1ee-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc1ee-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="fc1ee-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="fc1ee-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="fc1ee-110">Il secondo comando ottiene il certificato radice attendibile con un nome specificato dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc1ee-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="fc1ee-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc1ee-111">PARAMETERS</span></span>

### <span data-ttu-id="fc1ee-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc1ee-112">-ApplicationGateway</span></span>
<span data-ttu-id="fc1ee-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc1ee-113">The applicationGateway</span></span>

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

### <span data-ttu-id="fc1ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1ee-114">-DefaultProfile</span></span>
<span data-ttu-id="fc1ee-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc1ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1ee-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc1ee-116">-Name</span></span>
<span data-ttu-id="fc1ee-117">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="fc1ee-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="fc1ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1ee-118">CommonParameters</span></span>
<span data-ttu-id="fc1ee-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc1ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1ee-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1ee-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1ee-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc1ee-121">INPUTS</span></span>

### <span data-ttu-id="fc1ee-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc1ee-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc1ee-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc1ee-123">OUTPUTS</span></span>

### <span data-ttu-id="fc1ee-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fc1ee-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="fc1ee-125">Note</span><span class="sxs-lookup"><span data-stu-id="fc1ee-125">NOTES</span></span>

## <span data-ttu-id="fc1ee-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc1ee-126">RELATED LINKS</span></span>
