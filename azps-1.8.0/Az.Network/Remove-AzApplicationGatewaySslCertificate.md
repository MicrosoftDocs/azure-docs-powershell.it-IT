---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7b5f37cb42d128cbf44294520419c8f4d09124fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678155"
---
# <span data-ttu-id="97f40-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97f40-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="97f40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97f40-102">SYNOPSIS</span></span>
<span data-ttu-id="97f40-103">Rimuove un certificato SSL da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="97f40-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="97f40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97f40-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97f40-105">DESCRIPTION</span></span>
<span data-ttu-id="97f40-106">Il cmdlet **Remove-AzApplicationGatewaySslCertificate** rimuove un certificato SSL (Secure Sockets Layer) da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="97f40-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="97f40-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97f40-107">EXAMPLES</span></span>

### <span data-ttu-id="97f40-108">Esempio 1: rimuovere un certificato SSL da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="97f40-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="97f40-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="97f40-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="97f40-110">Il secondo comando rimuove il certificato SSL denominato Cert02 dal gateway dell'applicazione archiviato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="97f40-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="97f40-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97f40-111">PARAMETERS</span></span>

### <span data-ttu-id="97f40-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97f40-112">-ApplicationGateway</span></span>
<span data-ttu-id="97f40-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="97f40-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="97f40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f40-114">-DefaultProfile</span></span>
<span data-ttu-id="97f40-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97f40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97f40-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="97f40-116">-Name</span></span>
<span data-ttu-id="97f40-117">Specifica il nome di un certificato SSL rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97f40-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97f40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f40-118">CommonParameters</span></span>
<span data-ttu-id="97f40-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f40-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f40-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f40-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97f40-121">INPUTS</span></span>

### <span data-ttu-id="97f40-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97f40-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97f40-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97f40-123">OUTPUTS</span></span>

### <span data-ttu-id="97f40-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97f40-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97f40-125">Note</span><span class="sxs-lookup"><span data-stu-id="97f40-125">NOTES</span></span>

## <span data-ttu-id="97f40-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97f40-126">RELATED LINKS</span></span>

[<span data-ttu-id="97f40-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97f40-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="97f40-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97f40-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="97f40-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97f40-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="97f40-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="97f40-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)

