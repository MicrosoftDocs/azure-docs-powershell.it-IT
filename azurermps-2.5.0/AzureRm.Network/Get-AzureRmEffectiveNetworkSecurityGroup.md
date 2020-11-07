---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 214ab7f91791fa05453e2f4ef4238440d9c78a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866094"
---
# <span data-ttu-id="1536c-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1536c-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="1536c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1536c-102">SYNOPSIS</span></span>
<span data-ttu-id="1536c-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1536c-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1536c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1536c-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1536c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1536c-105">DESCRIPTION</span></span>
<span data-ttu-id="1536c-106">Il cmdlet **Get-AzureRmEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1536c-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="1536c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1536c-107">EXAMPLES</span></span>

### <span data-ttu-id="1536c-108">Esempio 1: ottenere il gruppo di sicurezza di rete effettivo in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="1536c-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="1536c-109">Questo comando consente di ottenere tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1536c-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="1536c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1536c-110">PARAMETERS</span></span>

### <span data-ttu-id="1536c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1536c-111">-DefaultProfile</span></span>
<span data-ttu-id="1536c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1536c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1536c-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="1536c-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="1536c-114">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1536c-114">Specified the name of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1536c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1536c-115">-ResourceGroupName</span></span>
<span data-ttu-id="1536c-116">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1536c-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="1536c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1536c-117">CommonParameters</span></span>
<span data-ttu-id="1536c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1536c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1536c-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1536c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1536c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1536c-120">INPUTS</span></span>

## <span data-ttu-id="1536c-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1536c-121">OUTPUTS</span></span>

### <span data-ttu-id="1536c-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1536c-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="1536c-123">Note</span><span class="sxs-lookup"><span data-stu-id="1536c-123">NOTES</span></span>

## <span data-ttu-id="1536c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1536c-124">RELATED LINKS</span></span>

[<span data-ttu-id="1536c-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="1536c-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


