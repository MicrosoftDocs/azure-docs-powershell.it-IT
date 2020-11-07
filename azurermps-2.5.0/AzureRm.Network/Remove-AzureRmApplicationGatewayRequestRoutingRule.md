---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 859ef684424069bb5fc4c5b45de3e722f0921705
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866059"
---
# <span data-ttu-id="71c39-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c39-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="71c39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71c39-102">SYNOPSIS</span></span>
<span data-ttu-id="71c39-103">Rimuove una regola di routing delle richieste da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="71c39-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71c39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71c39-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71c39-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71c39-105">DESCRIPTION</span></span>
<span data-ttu-id="71c39-106">Il cmdlet **Remove-AzureRmApplicationGatewayRequestRoutingRule** rimuove una regola di routing delle richieste da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="71c39-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="71c39-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71c39-107">EXAMPLES</span></span>

### <span data-ttu-id="71c39-108">Esempio 1: rimuovere una regola di routing delle richieste da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="71c39-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="71c39-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="71c39-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="71c39-110">Il secondo comando rimuove la regola di routing delle richieste denominata Rule02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="71c39-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="71c39-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71c39-111">PARAMETERS</span></span>

### <span data-ttu-id="71c39-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71c39-112">-ApplicationGateway</span></span>
<span data-ttu-id="71c39-113">Specifica il gateway dell'applicazione da cui rimuovere una regola di routing delle richieste.</span><span class="sxs-lookup"><span data-stu-id="71c39-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="71c39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c39-114">-DefaultProfile</span></span>
<span data-ttu-id="71c39-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71c39-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71c39-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="71c39-116">-Name</span></span>
<span data-ttu-id="71c39-117">Specifica il nome della regola di routing delle richieste per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71c39-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="71c39-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c39-118">CommonParameters</span></span>
<span data-ttu-id="71c39-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c39-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c39-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c39-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c39-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71c39-121">INPUTS</span></span>

### <span data-ttu-id="71c39-122">System. String</span><span class="sxs-lookup"><span data-stu-id="71c39-122">System.String</span></span>

## <span data-ttu-id="71c39-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71c39-123">OUTPUTS</span></span>

### <span data-ttu-id="71c39-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c39-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="71c39-125">Note</span><span class="sxs-lookup"><span data-stu-id="71c39-125">NOTES</span></span>

## <span data-ttu-id="71c39-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71c39-126">RELATED LINKS</span></span>

[<span data-ttu-id="71c39-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c39-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="71c39-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c39-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="71c39-129">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c39-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="71c39-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c39-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


