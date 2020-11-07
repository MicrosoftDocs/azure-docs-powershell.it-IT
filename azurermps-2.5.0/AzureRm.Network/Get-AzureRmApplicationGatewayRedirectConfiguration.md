---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 286afc05e9b7c825f183aabe7a78c965c790cb02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867057"
---
# <span data-ttu-id="d9764-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9764-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="d9764-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9764-102">SYNOPSIS</span></span>
<span data-ttu-id="d9764-103">Ottiene una configurazione di reindirizzamento esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9764-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9764-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9764-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9764-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9764-105">DESCRIPTION</span></span>
<span data-ttu-id="d9764-106">Il cmdlet **Get-AzureRmApplicationGatewayRedirectConfiguration** ottiene una configurazione di reindirizzamento esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9764-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="d9764-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9764-107">EXAMPLES</span></span>

### <span data-ttu-id="d9764-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9764-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="d9764-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d9764-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d9764-110">Il secondo comando consente di ottenere la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d9764-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="d9764-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9764-111">PARAMETERS</span></span>

### <span data-ttu-id="d9764-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9764-112">-ApplicationGateway</span></span>
<span data-ttu-id="d9764-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9764-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d9764-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9764-114">-DefaultProfile</span></span>
<span data-ttu-id="d9764-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9764-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9764-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9764-116">-Name</span></span>
<span data-ttu-id="d9764-117">Nome della regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="d9764-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="d9764-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9764-118">CommonParameters</span></span>
<span data-ttu-id="d9764-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9764-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9764-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9764-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9764-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9764-121">INPUTS</span></span>

### <span data-ttu-id="d9764-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9764-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9764-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9764-123">OUTPUTS</span></span>

### <span data-ttu-id="d9764-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9764-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="d9764-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d9764-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d9764-126">Note</span><span class="sxs-lookup"><span data-stu-id="d9764-126">NOTES</span></span>

## <span data-ttu-id="d9764-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9764-127">RELATED LINKS</span></span>

