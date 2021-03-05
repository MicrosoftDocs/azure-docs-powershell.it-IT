---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: aa6dbacb85263d8f0169f913c07e56a9dbd1c7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994054"
---
# <span data-ttu-id="62ac6-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62ac6-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="62ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="62ac6-103">Ottiene un certificato SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="62ac6-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="62ac6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62ac6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62ac6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62ac6-105">DESCRIPTION</span></span>
<span data-ttu-id="62ac6-106">Il cmdlet **Get-AzApplicationGatewaySslCertificate** ottiene un certificato SSL per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="62ac6-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="62ac6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62ac6-107">EXAMPLES</span></span>

### <span data-ttu-id="62ac6-108">Esempio 1: Ottenere un certificato SSL specifico</span><span class="sxs-lookup"><span data-stu-id="62ac6-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="62ac6-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="62ac6-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="62ac6-110">Il secondo comando recupera il certificato SSL denominato Cert01 dal gateway applicazione archiviato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="62ac6-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="62ac6-111">Il comando archivia il certificato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="62ac6-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="62ac6-112">Esempio 2: Ottenere un elenco di certificati SSL</span><span class="sxs-lookup"><span data-stu-id="62ac6-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="62ac6-113">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="62ac6-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="62ac6-114">Questo secondo comando ottiene un elenco di certificati SSL dal gateway applicazione archiviato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="62ac6-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="62ac6-115">Il comando archivia quindi i risultati nella variabile denominata $Certs.</span><span class="sxs-lookup"><span data-stu-id="62ac6-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="62ac6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62ac6-116">PARAMETERS</span></span>

### <span data-ttu-id="62ac6-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62ac6-117">-ApplicationGateway</span></span>
<span data-ttu-id="62ac6-118">Specifica l'oggetto gateway applicazione che contiene il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="62ac6-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="62ac6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ac6-119">-DefaultProfile</span></span>
<span data-ttu-id="62ac6-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62ac6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ac6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="62ac6-121">-Name</span></span>
<span data-ttu-id="62ac6-122">Specifica il nome del pool di certificati SSL che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ac6-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62ac6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ac6-123">CommonParameters</span></span>
<span data-ttu-id="62ac6-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ac6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ac6-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62ac6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ac6-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="62ac6-126">INPUTS</span></span>

### <span data-ttu-id="62ac6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62ac6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62ac6-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62ac6-128">OUTPUTS</span></span>

### <span data-ttu-id="62ac6-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62ac6-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="62ac6-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="62ac6-130">NOTES</span></span>

## <span data-ttu-id="62ac6-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62ac6-131">RELATED LINKS</span></span>

[<span data-ttu-id="62ac6-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62ac6-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="62ac6-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62ac6-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="62ac6-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62ac6-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="62ac6-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="62ac6-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


