---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 983c23111486a964275a7efb85031b013fb365d2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866886"
---
# <span data-ttu-id="12d3e-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="12d3e-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="12d3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="12d3e-103">Ottiene una rete virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12d3e-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12d3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12d3e-104">SYNTAX</span></span>

### <span data-ttu-id="12d3e-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="12d3e-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d3e-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="12d3e-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12d3e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12d3e-107">DESCRIPTION</span></span>
<span data-ttu-id="12d3e-108">Il cmdlet **Get-AzureRmVirtualNetwork** ottiene uno o più reti virtuali n un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12d3e-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="12d3e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12d3e-109">EXAMPLES</span></span>

### <span data-ttu-id="12d3e-110">1: recuperare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="12d3e-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="12d3e-111">Questo comando consente di ottenere la rete virtuale denominata MyVirtualNetwork nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12d3e-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="12d3e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12d3e-112">PARAMETERS</span></span>

### <span data-ttu-id="12d3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d3e-113">-DefaultProfile</span></span>
<span data-ttu-id="12d3e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12d3e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12d3e-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="12d3e-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d3e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="12d3e-116">-Name</span></span>
<span data-ttu-id="12d3e-117">Specifica il nome della rete virtuale ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d3e-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d3e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d3e-118">-ResourceGroupName</span></span>
<span data-ttu-id="12d3e-119">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="12d3e-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d3e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d3e-120">CommonParameters</span></span>
<span data-ttu-id="12d3e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d3e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d3e-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d3e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d3e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12d3e-123">INPUTS</span></span>

## <span data-ttu-id="12d3e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12d3e-124">OUTPUTS</span></span>

### <span data-ttu-id="12d3e-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="12d3e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="12d3e-126">Note</span><span class="sxs-lookup"><span data-stu-id="12d3e-126">NOTES</span></span>

## <span data-ttu-id="12d3e-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12d3e-127">RELATED LINKS</span></span>

[<span data-ttu-id="12d3e-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="12d3e-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="12d3e-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="12d3e-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="12d3e-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="12d3e-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


