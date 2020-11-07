---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 62c73fe60e147ca34083851db50c3830198dd60e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860870"
---
# <span data-ttu-id="d2747-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d2747-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="d2747-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2747-102">SYNOPSIS</span></span>
<span data-ttu-id="d2747-103">Ottiene un certificato SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2747-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="d2747-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2747-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2747-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2747-105">DESCRIPTION</span></span>
<span data-ttu-id="d2747-106">Il cmdlet **Get-AzApplicationGatewaySslCertificate** ottiene un certificato SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2747-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="d2747-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2747-107">EXAMPLES</span></span>

### <span data-ttu-id="d2747-108">Esempio 1: ottenere un certificato SSL specifico</span><span class="sxs-lookup"><span data-stu-id="d2747-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="d2747-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d2747-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d2747-110">Il secondo comando ottiene il certificato SSL denominato Cert01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d2747-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="d2747-111">Il comando Archivia il certificato nella variabile denominata $Cert.</span><span class="sxs-lookup"><span data-stu-id="d2747-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="d2747-112">Esempio 2: ottenere un elenco di certificati SSL</span><span class="sxs-lookup"><span data-stu-id="d2747-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="d2747-113">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d2747-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d2747-114">Questo secondo comando ottiene un elenco di certificati SSL dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d2747-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="d2747-115">Il comando Archivia quindi i risultati nella variabile denominata $Certs.</span><span class="sxs-lookup"><span data-stu-id="d2747-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="d2747-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2747-116">PARAMETERS</span></span>

### <span data-ttu-id="d2747-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2747-117">-ApplicationGateway</span></span>
<span data-ttu-id="d2747-118">Specifica l'oggetto gateway dell'applicazione che contiene il certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="d2747-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="d2747-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2747-119">-DefaultProfile</span></span>
<span data-ttu-id="d2747-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2747-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2747-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2747-121">-Name</span></span>
<span data-ttu-id="d2747-122">Specifica il nome del pool di certificati SSL ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2747-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d2747-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2747-123">CommonParameters</span></span>
<span data-ttu-id="d2747-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2747-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2747-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2747-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2747-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2747-126">INPUTS</span></span>

### <span data-ttu-id="d2747-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d2747-127">System.String</span></span>

## <span data-ttu-id="d2747-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2747-128">OUTPUTS</span></span>

### <span data-ttu-id="d2747-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d2747-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="d2747-130">Note</span><span class="sxs-lookup"><span data-stu-id="d2747-130">NOTES</span></span>

## <span data-ttu-id="d2747-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2747-131">RELATED LINKS</span></span>

[<span data-ttu-id="d2747-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d2747-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d2747-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d2747-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d2747-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d2747-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d2747-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d2747-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


