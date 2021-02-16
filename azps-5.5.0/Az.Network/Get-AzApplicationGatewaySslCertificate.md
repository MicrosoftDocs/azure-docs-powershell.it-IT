---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 3e7010309c6aed367e3771971a8b1c2841548fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187254"
---
# <span data-ttu-id="3157f-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3157f-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3157f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3157f-102">SYNOPSIS</span></span>
<span data-ttu-id="3157f-103">Recupera un certificato SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="3157f-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="3157f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3157f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3157f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3157f-105">DESCRIPTION</span></span>
<span data-ttu-id="3157f-106">Il cmdlet **Get-AzApplicationGatewaySslCertificate** ottiene un certificato SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="3157f-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="3157f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3157f-107">EXAMPLES</span></span>

### <span data-ttu-id="3157f-108">Esempio 1: Ottenere un certificato SSL specifico</span><span class="sxs-lookup"><span data-stu-id="3157f-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="3157f-109">Il primo comando recupera il Gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3157f-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3157f-110">Il secondo comando recupera il certificato SSL denominato Cert01 dal gateway applicazione archiviato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3157f-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="3157f-111">Il comando archivia il certificato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="3157f-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="3157f-112">Esempio 2: Ottenere un elenco di certificati SSL</span><span class="sxs-lookup"><span data-stu-id="3157f-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="3157f-113">Il primo comando recupera il Gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3157f-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3157f-114">Questo secondo comando ottiene un elenco di certificati SSL dal gateway applicazione archiviato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3157f-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="3157f-115">Il comando archivia quindi i risultati nella variabile denominata $Certs.</span><span class="sxs-lookup"><span data-stu-id="3157f-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="3157f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3157f-116">PARAMETERS</span></span>

### <span data-ttu-id="3157f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3157f-117">-ApplicationGateway</span></span>
<span data-ttu-id="3157f-118">Specifica l'oggetto gateway applicazione che contiene il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="3157f-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="3157f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3157f-119">-DefaultProfile</span></span>
<span data-ttu-id="3157f-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3157f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3157f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3157f-121">-Name</span></span>
<span data-ttu-id="3157f-122">Specifica il nome del pool di certificati SSL che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3157f-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3157f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3157f-123">CommonParameters</span></span>
<span data-ttu-id="3157f-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3157f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3157f-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3157f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3157f-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="3157f-126">INPUTS</span></span>

### <span data-ttu-id="3157f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3157f-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3157f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3157f-128">OUTPUTS</span></span>

### <span data-ttu-id="3157f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3157f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3157f-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="3157f-130">NOTES</span></span>

## <span data-ttu-id="3157f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3157f-131">RELATED LINKS</span></span>

[<span data-ttu-id="3157f-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3157f-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3157f-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3157f-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3157f-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3157f-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3157f-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3157f-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


