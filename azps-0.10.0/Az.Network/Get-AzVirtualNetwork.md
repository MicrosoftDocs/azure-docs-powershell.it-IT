---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860674"
---
# <span data-ttu-id="51eb0-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51eb0-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="51eb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="51eb0-103">Ottiene una rete virtuale in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51eb0-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="51eb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51eb0-104">SYNTAX</span></span>

### <span data-ttu-id="51eb0-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="51eb0-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51eb0-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="51eb0-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51eb0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51eb0-107">DESCRIPTION</span></span>
<span data-ttu-id="51eb0-108">Il cmdlet **Get-AzVirtualNetwork** ottiene uno o più reti virtuali n un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51eb0-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="51eb0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51eb0-109">EXAMPLES</span></span>

### <span data-ttu-id="51eb0-110">1: recuperare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="51eb0-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="51eb0-111">Questo comando consente di ottenere la rete virtuale denominata MyVirtualNetwork nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51eb0-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="51eb0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51eb0-112">PARAMETERS</span></span>

### <span data-ttu-id="51eb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51eb0-113">-DefaultProfile</span></span>
<span data-ttu-id="51eb0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51eb0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51eb0-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="51eb0-115">-ExpandResource</span></span>
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

### <span data-ttu-id="51eb0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="51eb0-116">-Name</span></span>
<span data-ttu-id="51eb0-117">Specifica il nome della rete virtuale ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51eb0-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="51eb0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51eb0-118">-ResourceGroupName</span></span>
<span data-ttu-id="51eb0-119">Specifica il nome del gruppo di risorse a cui appartiene la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="51eb0-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="51eb0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51eb0-120">CommonParameters</span></span>
<span data-ttu-id="51eb0-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51eb0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51eb0-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51eb0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51eb0-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51eb0-123">INPUTS</span></span>

## <span data-ttu-id="51eb0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51eb0-124">OUTPUTS</span></span>

### <span data-ttu-id="51eb0-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51eb0-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="51eb0-126">Note</span><span class="sxs-lookup"><span data-stu-id="51eb0-126">NOTES</span></span>

## <span data-ttu-id="51eb0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51eb0-127">RELATED LINKS</span></span>

[<span data-ttu-id="51eb0-128">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51eb0-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="51eb0-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51eb0-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="51eb0-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="51eb0-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


