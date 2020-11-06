---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511096"
---
# <span data-ttu-id="0d3bf-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d3bf-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="0d3bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="0d3bf-103">Ottiene una rete virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d3bf-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d3bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d3bf-104">SYNTAX</span></span>

### <span data-ttu-id="0d3bf-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="0d3bf-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d3bf-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="0d3bf-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d3bf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d3bf-107">DESCRIPTION</span></span>
<span data-ttu-id="0d3bf-108">Il cmdlet **Get-AzureRmVirtualNetwork** ottiene uno o più reti virtuali n un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d3bf-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="0d3bf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d3bf-109">EXAMPLES</span></span>

### <span data-ttu-id="0d3bf-110">1: recuperare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0d3bf-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="0d3bf-111">Questo comando consente di ottenere la rete virtuale denominata MyVirtualNetwork nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0d3bf-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="0d3bf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d3bf-112">PARAMETERS</span></span>

### <span data-ttu-id="0d3bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d3bf-113">-DefaultProfile</span></span>
<span data-ttu-id="0d3bf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d3bf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d3bf-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0d3bf-115">-ExpandResource</span></span>
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

### <span data-ttu-id="0d3bf-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d3bf-116">-Name</span></span>
<span data-ttu-id="0d3bf-117">Specifica il nome della rete virtuale ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d3bf-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0d3bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d3bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d3bf-119">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d3bf-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="0d3bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3bf-120">CommonParameters</span></span>
<span data-ttu-id="0d3bf-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d3bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3bf-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d3bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3bf-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d3bf-123">INPUTS</span></span>

### <span data-ttu-id="0d3bf-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0d3bf-124">None</span></span>
<span data-ttu-id="0d3bf-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0d3bf-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d3bf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d3bf-126">OUTPUTS</span></span>

### <span data-ttu-id="0d3bf-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d3bf-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0d3bf-128">Note</span><span class="sxs-lookup"><span data-stu-id="0d3bf-128">NOTES</span></span>

## <span data-ttu-id="0d3bf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d3bf-129">RELATED LINKS</span></span>

[<span data-ttu-id="0d3bf-130">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d3bf-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0d3bf-131">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d3bf-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0d3bf-132">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0d3bf-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


