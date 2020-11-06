---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 656067c89adbcead5dd24e08d45147eb7f019e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519270"
---
# <span data-ttu-id="42eef-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42eef-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="42eef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42eef-102">SYNOPSIS</span></span>
<span data-ttu-id="42eef-103">Crea una porta front-end per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="42eef-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42eef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42eef-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42eef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42eef-105">DESCRIPTION</span></span>
<span data-ttu-id="42eef-106">Il cmdlet **New-AzureRmApplicationGatewayFrontendPort** crea una porta front-end per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="42eef-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="42eef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42eef-107">EXAMPLES</span></span>

### <span data-ttu-id="42eef-108">Esempio1: creare una porta front-end</span><span class="sxs-lookup"><span data-stu-id="42eef-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="42eef-109">Questo comando crea una porta front-end denominata FrontEndPort01 sulla porta 80 e archivia il risultato nella variabile denominata $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="42eef-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="42eef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42eef-110">PARAMETERS</span></span>

### <span data-ttu-id="42eef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42eef-111">-DefaultProfile</span></span>
<span data-ttu-id="42eef-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42eef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42eef-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="42eef-113">-Name</span></span>
<span data-ttu-id="42eef-114">Specifica il nome della porta front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42eef-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="42eef-115">-Porta</span><span class="sxs-lookup"><span data-stu-id="42eef-115">-Port</span></span>
<span data-ttu-id="42eef-116">Specifica il numero di porta della porta front-end.</span><span class="sxs-lookup"><span data-stu-id="42eef-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="42eef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42eef-117">CommonParameters</span></span>
<span data-ttu-id="42eef-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42eef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42eef-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42eef-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42eef-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42eef-120">INPUTS</span></span>

### <span data-ttu-id="42eef-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="42eef-121">None</span></span>

## <span data-ttu-id="42eef-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42eef-122">OUTPUTS</span></span>

### <span data-ttu-id="42eef-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42eef-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="42eef-124">Note</span><span class="sxs-lookup"><span data-stu-id="42eef-124">NOTES</span></span>

## <span data-ttu-id="42eef-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42eef-125">RELATED LINKS</span></span>

[<span data-ttu-id="42eef-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42eef-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="42eef-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42eef-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="42eef-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42eef-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="42eef-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="42eef-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


