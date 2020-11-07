---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d254008ef4d6d4fc6e16f9a543a38518a6537a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688452"
---
# <span data-ttu-id="6683c-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6683c-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6683c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6683c-102">SYNOPSIS</span></span>
<span data-ttu-id="6683c-103">Ottiene la regola di routing delle richieste di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6683c-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6683c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6683c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6683c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6683c-105">DESCRIPTION</span></span>
<span data-ttu-id="6683c-106">Il cmdlet **Get-AzureRmApplicationGatewayRequestRoutingRule** ottiene la regola di routing delle richieste di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6683c-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="6683c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6683c-107">EXAMPLES</span></span>

### <span data-ttu-id="6683c-108">Esempio 1: ottenere una specifica regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="6683c-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="6683c-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6683c-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6683c-110">Il secondo comando consente di ottenere la regola di routing delle richieste denominata Rule01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6683c-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="6683c-111">Esempio 2: ottenere un elenco delle regole di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="6683c-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="6683c-112">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6683c-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6683c-113">Il secondo comando ottiene un elenco delle regole di routing delle richieste dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6683c-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="6683c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6683c-114">PARAMETERS</span></span>

### <span data-ttu-id="6683c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6683c-115">-ApplicationGateway</span></span>
<span data-ttu-id="6683c-116">Specifica l'oggetto gateway dell'applicazione che contiene la regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="6683c-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="6683c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6683c-117">-DefaultProfile</span></span>
<span data-ttu-id="6683c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6683c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6683c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6683c-119">-Name</span></span>
<span data-ttu-id="6683c-120">Specifica il nome della regola di routing delle richieste ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6683c-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="6683c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6683c-121">CommonParameters</span></span>
<span data-ttu-id="6683c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6683c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6683c-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6683c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6683c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6683c-124">INPUTS</span></span>

### <span data-ttu-id="6683c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6683c-125">System.String</span></span>

## <span data-ttu-id="6683c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6683c-126">OUTPUTS</span></span>

### <span data-ttu-id="6683c-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6683c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6683c-128">Note</span><span class="sxs-lookup"><span data-stu-id="6683c-128">NOTES</span></span>

## <span data-ttu-id="6683c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6683c-129">RELATED LINKS</span></span>

[<span data-ttu-id="6683c-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6683c-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6683c-131">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6683c-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6683c-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6683c-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6683c-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6683c-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


