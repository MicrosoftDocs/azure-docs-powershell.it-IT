---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 71a6ec46cea6cc9d2ba6e6537797657b2124fe01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512523"
---
# <span data-ttu-id="e4e20-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="e4e20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4e20-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e20-103">Modifica un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e4e20-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4e20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4e20-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e20-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4e20-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e20-106">Il cmdlet **set-AzureRmExpressRouteCircuit** Salva il circuito ExpressRoute modificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e20-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="e4e20-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4e20-107">EXAMPLES</span></span>

### <span data-ttu-id="e4e20-108">Esempio 1: cambiare la ServiceKey di un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e4e20-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="e4e20-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4e20-109">PARAMETERS</span></span>

### <span data-ttu-id="e4e20-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4e20-110">-AsJob</span></span>
<span data-ttu-id="e4e20-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e4e20-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e20-112">-DefaultProfile</span></span>
<span data-ttu-id="e4e20-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e20-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4e20-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e4e20-115">Specifica l'oggetto **ExpressRouteCircuit** che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e4e20-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e20-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e20-116">CommonParameters</span></span>
<span data-ttu-id="e4e20-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e20-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e20-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e20-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e20-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4e20-119">INPUTS</span></span>

### <span data-ttu-id="e4e20-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="e4e20-121">Il parametro ' ExpressRouteCircuit ' accetta il valore di tipo ' PSExpressRouteCircuit ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e4e20-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="e4e20-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4e20-122">OUTPUTS</span></span>

### <span data-ttu-id="e4e20-123">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e4e20-124">Note</span><span class="sxs-lookup"><span data-stu-id="e4e20-124">NOTES</span></span>

## <span data-ttu-id="e4e20-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4e20-125">RELATED LINKS</span></span>

[<span data-ttu-id="e4e20-126">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e4e20-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e4e20-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="e4e20-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e4e20-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
