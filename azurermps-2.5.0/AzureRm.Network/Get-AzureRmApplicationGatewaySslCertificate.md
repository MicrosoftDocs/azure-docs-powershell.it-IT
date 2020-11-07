---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 6e2dceadf11323eb1798435df426c063f4d58858
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867053"
---
# <span data-ttu-id="3ef8d-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef8d-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3ef8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ef8d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef8d-103">Ottiene un certificato SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ef8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ef8d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ef8d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ef8d-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef8d-106">Il cmdlet **Get-AzureRmApplicationGatewaySslCertificate** ottiene un certificato SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="3ef8d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ef8d-107">EXAMPLES</span></span>

### <span data-ttu-id="3ef8d-108">Esempio 1: ottenere un certificato SSL specifico</span><span class="sxs-lookup"><span data-stu-id="3ef8d-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="3ef8d-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3ef8d-110">Il secondo comando ottiene il certificato SSL denominato Cert01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="3ef8d-111">Il comando Archivia il certificato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="3ef8d-112">Esempio 2: ottenere un elenco di certificati SSL</span><span class="sxs-lookup"><span data-stu-id="3ef8d-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="3ef8d-113">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3ef8d-114">Questo secondo comando ottiene un elenco di certificati SSL dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="3ef8d-115">Il comando Archivia quindi i risultati nella variabile denominata $Certs.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="3ef8d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ef8d-116">PARAMETERS</span></span>

### <span data-ttu-id="3ef8d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ef8d-117">-ApplicationGateway</span></span>
<span data-ttu-id="3ef8d-118">Specifica l'oggetto gateway dell'applicazione che contiene il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="3ef8d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef8d-119">-DefaultProfile</span></span>
<span data-ttu-id="3ef8d-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ef8d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ef8d-121">-Name</span></span>
<span data-ttu-id="3ef8d-122">Specifica il nome del pool di certificati SSL ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3ef8d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef8d-123">CommonParameters</span></span>
<span data-ttu-id="3ef8d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ef8d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef8d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef8d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef8d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ef8d-126">INPUTS</span></span>

### <span data-ttu-id="3ef8d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3ef8d-127">System.String</span></span>

## <span data-ttu-id="3ef8d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ef8d-128">OUTPUTS</span></span>

### <span data-ttu-id="3ef8d-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef8d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3ef8d-130">Note</span><span class="sxs-lookup"><span data-stu-id="3ef8d-130">NOTES</span></span>

## <span data-ttu-id="3ef8d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ef8d-131">RELATED LINKS</span></span>

[<span data-ttu-id="3ef8d-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef8d-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3ef8d-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef8d-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3ef8d-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef8d-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3ef8d-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3ef8d-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


