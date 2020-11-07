---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678366"
---
# <span data-ttu-id="4f6c5-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f6c5-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4f6c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="4f6c5-103">Crea una porta front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="4f6c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f6c5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f6c5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="4f6c5-106">Il cmdlet **New-AzApplicationGatewayFrontendPort** crea una porta front-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="4f6c5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="4f6c5-108">Esempio1: creare una porta front-end</span><span class="sxs-lookup"><span data-stu-id="4f6c5-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="4f6c5-109">Questo comando crea una porta front-end denominata FrontEndPort01 sulla porta 80 e archivia il risultato nella variabile denominata $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="4f6c5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f6c5-110">PARAMETERS</span></span>

### <span data-ttu-id="4f6c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f6c5-111">-DefaultProfile</span></span>
<span data-ttu-id="4f6c5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f6c5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f6c5-113">-Name</span></span>
<span data-ttu-id="4f6c5-114">Specifica il nome della porta front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4f6c5-115">-Porta</span><span class="sxs-lookup"><span data-stu-id="4f6c5-115">-Port</span></span>
<span data-ttu-id="4f6c5-116">Specifica il numero di porta della porta front-end.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f6c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f6c5-117">CommonParameters</span></span>
<span data-ttu-id="4f6c5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f6c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f6c5-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f6c5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f6c5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f6c5-120">INPUTS</span></span>

### <span data-ttu-id="4f6c5-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4f6c5-121">None</span></span>

## <span data-ttu-id="4f6c5-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f6c5-122">OUTPUTS</span></span>

### <span data-ttu-id="4f6c5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f6c5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4f6c5-124">Note</span><span class="sxs-lookup"><span data-stu-id="4f6c5-124">NOTES</span></span>

## <span data-ttu-id="4f6c5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f6c5-125">RELATED LINKS</span></span>

[<span data-ttu-id="4f6c5-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f6c5-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4f6c5-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f6c5-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4f6c5-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f6c5-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4f6c5-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4f6c5-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


