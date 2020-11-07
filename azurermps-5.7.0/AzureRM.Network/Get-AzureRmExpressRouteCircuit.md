---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 380a5f52a520f487e625663f7d84cbbc55564db5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686477"
---
# <span data-ttu-id="eceef-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eceef-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="eceef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eceef-102">SYNOPSIS</span></span>
<span data-ttu-id="eceef-103">Ottiene un circuito di Azure ExpressRoute da Azure.</span><span class="sxs-lookup"><span data-stu-id="eceef-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eceef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eceef-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eceef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eceef-105">DESCRIPTION</span></span>
<span data-ttu-id="eceef-106">Il cmdlet **Get-AzureRmExpressRouteCircuit** viene usato per recuperare un oggetto Circuit ExpressRoute dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eceef-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="eceef-107">L'oggetto Circuit restituito può essere usato come input per altri cmdlet che operano su circuiti ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eceef-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="eceef-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eceef-108">EXAMPLES</span></span>

### <span data-ttu-id="eceef-109">Esempio 1: ottenere il circuito ExpressRoute da eliminare</span><span class="sxs-lookup"><span data-stu-id="eceef-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="eceef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eceef-110">PARAMETERS</span></span>

### <span data-ttu-id="eceef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eceef-111">-DefaultProfile</span></span>
<span data-ttu-id="eceef-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eceef-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eceef-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="eceef-113">-Name</span></span>
<span data-ttu-id="eceef-114">Il nome del circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eceef-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eceef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eceef-115">-ResourceGroupName</span></span>
<span data-ttu-id="eceef-116">Nome del gruppo di risorse che contiene il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eceef-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eceef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eceef-117">CommonParameters</span></span>
<span data-ttu-id="eceef-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eceef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eceef-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eceef-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eceef-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eceef-120">INPUTS</span></span>

### <span data-ttu-id="eceef-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eceef-121">None</span></span>
<span data-ttu-id="eceef-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="eceef-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eceef-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eceef-123">OUTPUTS</span></span>

### <span data-ttu-id="eceef-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eceef-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="eceef-125">Note</span><span class="sxs-lookup"><span data-stu-id="eceef-125">NOTES</span></span>

## <span data-ttu-id="eceef-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eceef-126">RELATED LINKS</span></span>

[<span data-ttu-id="eceef-127">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eceef-127">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="eceef-128">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eceef-128">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="eceef-129">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eceef-129">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="eceef-130">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="eceef-130">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
