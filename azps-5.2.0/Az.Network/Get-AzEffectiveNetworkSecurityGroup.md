---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369358"
---
# <span data-ttu-id="49cc4-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49cc4-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="49cc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="49cc4-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="49cc4-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="49cc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49cc4-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49cc4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="49cc4-106">Il cmdlet **Get-AzEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="49cc4-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="49cc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="49cc4-108">Esempio 1: ottenere il gruppo di sicurezza di rete effettivo in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="49cc4-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="49cc4-109">Questo comando consente di ottenere tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="49cc4-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="49cc4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49cc4-110">PARAMETERS</span></span>

### <span data-ttu-id="49cc4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cc4-111">-DefaultProfile</span></span>
<span data-ttu-id="49cc4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49cc4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49cc4-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="49cc4-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="49cc4-114">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="49cc4-114">Specified the name of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49cc4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49cc4-115">-ResourceGroupName</span></span>
<span data-ttu-id="49cc4-116">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="49cc4-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49cc4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cc4-117">CommonParameters</span></span>
<span data-ttu-id="49cc4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49cc4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cc4-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49cc4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cc4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49cc4-120">INPUTS</span></span>

### <span data-ttu-id="49cc4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="49cc4-121">System.String</span></span>

## <span data-ttu-id="49cc4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49cc4-122">OUTPUTS</span></span>

### <span data-ttu-id="49cc4-123">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49cc4-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="49cc4-124">Note</span><span class="sxs-lookup"><span data-stu-id="49cc4-124">NOTES</span></span>

## <span data-ttu-id="49cc4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49cc4-125">RELATED LINKS</span></span>

[<span data-ttu-id="49cc4-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="49cc4-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


