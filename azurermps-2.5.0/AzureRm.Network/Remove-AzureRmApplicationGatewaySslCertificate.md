---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866055"
---
# <span data-ttu-id="5cb13-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb13-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5cb13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cb13-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb13-103">Rimuove un certificato SSL da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb13-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cb13-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cb13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cb13-105">DESCRIPTION</span></span>
<span data-ttu-id="5cb13-106">Il cmdlet **Remove-AzureRmApplicationGatewaySslCertificate** rimuove un certificato SSL (Secure Sockets Layer) da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb13-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="5cb13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cb13-107">EXAMPLES</span></span>

### <span data-ttu-id="5cb13-108">Esempio 1: rimuovere un certificato SSL da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5cb13-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="5cb13-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5cb13-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="5cb13-110">Il secondo comando rimuove il certificato SSL denominato Cert02 dal gateway dell'applicazione archiviato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5cb13-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="5cb13-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cb13-111">PARAMETERS</span></span>

### <span data-ttu-id="5cb13-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cb13-112">-ApplicationGateway</span></span>
<span data-ttu-id="5cb13-113">Specifica il gateway dell'applicazione da cui questo cmdlet rimuove un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="5cb13-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="5cb13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb13-114">-DefaultProfile</span></span>
<span data-ttu-id="5cb13-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cb13-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb13-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cb13-116">-Name</span></span>
<span data-ttu-id="5cb13-117">Specifica il nome di un certificato SSL rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cb13-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5cb13-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb13-118">CommonParameters</span></span>
<span data-ttu-id="5cb13-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb13-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb13-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb13-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb13-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cb13-121">INPUTS</span></span>

### <span data-ttu-id="5cb13-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5cb13-122">System.String</span></span>

## <span data-ttu-id="5cb13-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cb13-123">OUTPUTS</span></span>

### <span data-ttu-id="5cb13-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5cb13-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5cb13-125">Note</span><span class="sxs-lookup"><span data-stu-id="5cb13-125">NOTES</span></span>

## <span data-ttu-id="5cb13-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cb13-126">RELATED LINKS</span></span>

[<span data-ttu-id="5cb13-127">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb13-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5cb13-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb13-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5cb13-129">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb13-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5cb13-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb13-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


