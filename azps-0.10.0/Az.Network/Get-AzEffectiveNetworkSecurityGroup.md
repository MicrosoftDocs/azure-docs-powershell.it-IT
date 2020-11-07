---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a960d5b2f6daf19fc4e46eb253b596eb88e6bd71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860837"
---
# <span data-ttu-id="88583-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88583-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="88583-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88583-102">SYNOPSIS</span></span>
<span data-ttu-id="88583-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="88583-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="88583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88583-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88583-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88583-105">DESCRIPTION</span></span>
<span data-ttu-id="88583-106">Il cmdlet **Get-AzEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="88583-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="88583-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88583-107">EXAMPLES</span></span>

### <span data-ttu-id="88583-108">Esempio 1: ottenere il gruppo di sicurezza di rete effettivo in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="88583-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="88583-109">Questo comando consente di ottenere tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="88583-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="88583-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88583-110">PARAMETERS</span></span>

### <span data-ttu-id="88583-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88583-111">-DefaultProfile</span></span>
<span data-ttu-id="88583-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88583-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88583-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="88583-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="88583-114">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="88583-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="88583-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88583-115">-ResourceGroupName</span></span>
<span data-ttu-id="88583-116">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="88583-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="88583-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88583-117">CommonParameters</span></span>
<span data-ttu-id="88583-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88583-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88583-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88583-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88583-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88583-120">INPUTS</span></span>

## <span data-ttu-id="88583-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88583-121">OUTPUTS</span></span>

### <span data-ttu-id="88583-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88583-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="88583-123">Note</span><span class="sxs-lookup"><span data-stu-id="88583-123">NOTES</span></span>

## <span data-ttu-id="88583-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88583-124">RELATED LINKS</span></span>

[<span data-ttu-id="88583-125">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="88583-125">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


