---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 38f7d6780b598606d0a0938178309ed67e602315
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967918"
---
# <span data-ttu-id="6f289-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f289-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="6f289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f289-102">SYNOPSIS</span></span>
<span data-ttu-id="6f289-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6f289-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="6f289-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f289-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f289-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f289-105">DESCRIPTION</span></span>
<span data-ttu-id="6f289-106">Il cmdlet **Get-AzEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6f289-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="6f289-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f289-107">EXAMPLES</span></span>

### <span data-ttu-id="6f289-108">Esempio 1: Ottenere il gruppo di sicurezza di rete effettivo su un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="6f289-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="6f289-109">Questo comando recupera tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6f289-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="6f289-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f289-110">PARAMETERS</span></span>

### <span data-ttu-id="6f289-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f289-111">-DefaultProfile</span></span>
<span data-ttu-id="6f289-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f289-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f289-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="6f289-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="6f289-114">È stato specificato il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6f289-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="6f289-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f289-115">-ResourceGroupName</span></span>
<span data-ttu-id="6f289-116">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6f289-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="6f289-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f289-117">CommonParameters</span></span>
<span data-ttu-id="6f289-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f289-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f289-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f289-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f289-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f289-120">INPUTS</span></span>

### <span data-ttu-id="6f289-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6f289-121">System.String</span></span>

## <span data-ttu-id="6f289-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f289-122">OUTPUTS</span></span>

### <span data-ttu-id="6f289-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6f289-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="6f289-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f289-124">NOTES</span></span>

## <span data-ttu-id="6f289-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f289-125">RELATED LINKS</span></span>

[<span data-ttu-id="6f289-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f289-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


