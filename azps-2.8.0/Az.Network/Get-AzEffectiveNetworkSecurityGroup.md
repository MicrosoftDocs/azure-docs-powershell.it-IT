---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c9dd7695e195386b9dd0921b4a9161a5fb175c6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853261"
---
# <span data-ttu-id="a280b-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a280b-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="a280b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a280b-102">SYNOPSIS</span></span>
<span data-ttu-id="a280b-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a280b-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="a280b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a280b-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a280b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a280b-105">DESCRIPTION</span></span>
<span data-ttu-id="a280b-106">Il cmdlet **Get-AzEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a280b-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="a280b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a280b-107">EXAMPLES</span></span>

### <span data-ttu-id="a280b-108">Esempio 1: ottenere il gruppo di sicurezza di rete effettivo in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="a280b-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="a280b-109">Questo comando consente di ottenere tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a280b-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="a280b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a280b-110">PARAMETERS</span></span>

### <span data-ttu-id="a280b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a280b-111">-DefaultProfile</span></span>
<span data-ttu-id="a280b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a280b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a280b-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a280b-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="a280b-114">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a280b-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="a280b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a280b-115">-ResourceGroupName</span></span>
<span data-ttu-id="a280b-116">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="a280b-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="a280b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a280b-117">CommonParameters</span></span>
<span data-ttu-id="a280b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a280b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a280b-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a280b-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a280b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a280b-120">INPUTS</span></span>

### <span data-ttu-id="a280b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a280b-121">System.String</span></span>

## <span data-ttu-id="a280b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a280b-122">OUTPUTS</span></span>

### <span data-ttu-id="a280b-123">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a280b-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="a280b-124">Note</span><span class="sxs-lookup"><span data-stu-id="a280b-124">NOTES</span></span>

## <span data-ttu-id="a280b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a280b-125">RELATED LINKS</span></span>

[<span data-ttu-id="a280b-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a280b-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


