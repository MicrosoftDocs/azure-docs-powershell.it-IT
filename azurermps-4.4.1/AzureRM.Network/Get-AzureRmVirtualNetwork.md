---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516955"
---
# <span data-ttu-id="668d5-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="668d5-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="668d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="668d5-102">SYNOPSIS</span></span>
<span data-ttu-id="668d5-103">Ottiene una rete virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="668d5-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="668d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="668d5-104">SYNTAX</span></span>

### <span data-ttu-id="668d5-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="668d5-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="668d5-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="668d5-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="668d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="668d5-107">DESCRIPTION</span></span>
<span data-ttu-id="668d5-108">Il cmdlet **Get-AzureRmVirtualNetwork** ottiene uno o più reti virtuali n un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="668d5-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="668d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="668d5-109">EXAMPLES</span></span>

### <span data-ttu-id="668d5-110">1: recuperare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="668d5-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="668d5-111">Questo comando consente di ottenere la rete virtuale denominata MyVirtualNetwork nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="668d5-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="668d5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="668d5-112">PARAMETERS</span></span>

### <span data-ttu-id="668d5-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="668d5-113">-ExpandResource</span></span>
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

### <span data-ttu-id="668d5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="668d5-114">-Name</span></span>
<span data-ttu-id="668d5-115">Specifica il nome della rete virtuale ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="668d5-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="668d5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668d5-116">-ResourceGroupName</span></span>
<span data-ttu-id="668d5-117">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="668d5-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="668d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668d5-118">-DefaultProfile</span></span>
<span data-ttu-id="668d5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="668d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="668d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668d5-120">CommonParameters</span></span>
<span data-ttu-id="668d5-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="668d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668d5-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="668d5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668d5-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="668d5-123">INPUTS</span></span>

## <span data-ttu-id="668d5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="668d5-124">OUTPUTS</span></span>

### <span data-ttu-id="668d5-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="668d5-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="668d5-126">Note</span><span class="sxs-lookup"><span data-stu-id="668d5-126">NOTES</span></span>

## <span data-ttu-id="668d5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="668d5-127">RELATED LINKS</span></span>

[<span data-ttu-id="668d5-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="668d5-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="668d5-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="668d5-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="668d5-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="668d5-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


