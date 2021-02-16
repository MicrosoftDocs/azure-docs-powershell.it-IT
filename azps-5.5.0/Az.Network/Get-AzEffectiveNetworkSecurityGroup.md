---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191967"
---
# <span data-ttu-id="5d63f-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d63f-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5d63f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d63f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d63f-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="5d63f-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="5d63f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d63f-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d63f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d63f-105">DESCRIPTION</span></span>
<span data-ttu-id="5d63f-106">Il cmdlet **Get-AzEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="5d63f-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="5d63f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d63f-107">EXAMPLES</span></span>

### <span data-ttu-id="5d63f-108">Esempio 1: Ottenere il gruppo di sicurezza di rete effettivo su un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="5d63f-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="5d63f-109">Questo comando recupera tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5d63f-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="5d63f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d63f-110">PARAMETERS</span></span>

### <span data-ttu-id="5d63f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d63f-111">-DefaultProfile</span></span>
<span data-ttu-id="5d63f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d63f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d63f-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5d63f-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="5d63f-114">È stato specificato il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="5d63f-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5d63f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d63f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5d63f-116">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="5d63f-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="5d63f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d63f-117">CommonParameters</span></span>
<span data-ttu-id="5d63f-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d63f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d63f-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d63f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d63f-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d63f-120">INPUTS</span></span>

### <span data-ttu-id="5d63f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5d63f-121">System.String</span></span>

## <span data-ttu-id="5d63f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d63f-122">OUTPUTS</span></span>

### <span data-ttu-id="5d63f-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d63f-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="5d63f-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d63f-124">NOTES</span></span>

## <span data-ttu-id="5d63f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d63f-125">RELATED LINKS</span></span>

[<span data-ttu-id="5d63f-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5d63f-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


