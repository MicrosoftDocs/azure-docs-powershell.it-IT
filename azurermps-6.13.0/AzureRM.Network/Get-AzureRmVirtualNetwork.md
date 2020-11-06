---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 3a5cd755718536170c3e6fb1f6dd5410e1acffc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522035"
---
# <span data-ttu-id="48aa2-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48aa2-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="48aa2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="48aa2-103">Ottiene una rete virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="48aa2-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48aa2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48aa2-104">SYNTAX</span></span>

### <span data-ttu-id="48aa2-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="48aa2-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48aa2-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="48aa2-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48aa2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48aa2-107">DESCRIPTION</span></span>
<span data-ttu-id="48aa2-108">Il cmdlet **Get-AzureRmVirtualNetwork** ottiene uno o più reti virtuali n un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="48aa2-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="48aa2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48aa2-109">EXAMPLES</span></span>

### <span data-ttu-id="48aa2-110">1: recuperare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="48aa2-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="48aa2-111">Questo comando consente di ottenere la rete virtuale denominata MyVirtualNetwork nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="48aa2-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="48aa2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48aa2-112">PARAMETERS</span></span>

### <span data-ttu-id="48aa2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48aa2-113">-DefaultProfile</span></span>
<span data-ttu-id="48aa2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48aa2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48aa2-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="48aa2-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48aa2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="48aa2-116">-Name</span></span>
<span data-ttu-id="48aa2-117">Specifica il nome della rete virtuale ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48aa2-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48aa2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48aa2-118">-ResourceGroupName</span></span>
<span data-ttu-id="48aa2-119">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="48aa2-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48aa2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48aa2-120">CommonParameters</span></span>
<span data-ttu-id="48aa2-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48aa2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48aa2-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48aa2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48aa2-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48aa2-123">INPUTS</span></span>

### <span data-ttu-id="48aa2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="48aa2-124">System.String</span></span>

## <span data-ttu-id="48aa2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48aa2-125">OUTPUTS</span></span>

### <span data-ttu-id="48aa2-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48aa2-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="48aa2-127">Note</span><span class="sxs-lookup"><span data-stu-id="48aa2-127">NOTES</span></span>

## <span data-ttu-id="48aa2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48aa2-128">RELATED LINKS</span></span>

[<span data-ttu-id="48aa2-129">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48aa2-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="48aa2-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48aa2-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="48aa2-131">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="48aa2-131">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


