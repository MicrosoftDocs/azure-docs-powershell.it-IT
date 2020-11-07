---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: ddfe8b1736ef6c037522815dc81019fadc5b6c1f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860569"
---
# <span data-ttu-id="80285-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="80285-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="80285-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80285-102">SYNOPSIS</span></span>
<span data-ttu-id="80285-103">Crea una porta front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80285-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="80285-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80285-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80285-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80285-105">DESCRIPTION</span></span>
<span data-ttu-id="80285-106">Il cmdlet **New-AzApplicationGatewayFrontendPort** crea una porta front-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="80285-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="80285-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80285-107">EXAMPLES</span></span>

### <span data-ttu-id="80285-108">Esempio1: creare una porta front-end</span><span class="sxs-lookup"><span data-stu-id="80285-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="80285-109">Questo comando crea una porta front-end denominata FrontEndPort01 sulla porta 80 e archivia il risultato nella variabile denominata $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="80285-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="80285-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80285-110">PARAMETERS</span></span>

### <span data-ttu-id="80285-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80285-111">-DefaultProfile</span></span>
<span data-ttu-id="80285-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80285-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80285-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="80285-113">-Name</span></span>
<span data-ttu-id="80285-114">Specifica il nome della porta front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80285-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="80285-115">-Porta</span><span class="sxs-lookup"><span data-stu-id="80285-115">-Port</span></span>
<span data-ttu-id="80285-116">Specifica il numero di porta della porta front-end.</span><span class="sxs-lookup"><span data-stu-id="80285-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80285-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80285-117">CommonParameters</span></span>
<span data-ttu-id="80285-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80285-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80285-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80285-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80285-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80285-120">INPUTS</span></span>

### <span data-ttu-id="80285-121">System. String</span><span class="sxs-lookup"><span data-stu-id="80285-121">System.String</span></span>

## <span data-ttu-id="80285-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80285-122">OUTPUTS</span></span>

### <span data-ttu-id="80285-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="80285-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="80285-124">Note</span><span class="sxs-lookup"><span data-stu-id="80285-124">NOTES</span></span>

## <span data-ttu-id="80285-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80285-125">RELATED LINKS</span></span>

[<span data-ttu-id="80285-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="80285-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="80285-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="80285-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="80285-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="80285-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="80285-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="80285-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


