---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: d479c66b899637f2dc12061b7499fc65b7d59d66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516975"
---
# <span data-ttu-id="7f107-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f107-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="7f107-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f107-102">SYNOPSIS</span></span>
<span data-ttu-id="7f107-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f107-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f107-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f107-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f107-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f107-105">DESCRIPTION</span></span>
<span data-ttu-id="7f107-106">Il cmdlet **Get-AzureRmEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f107-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="7f107-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f107-107">EXAMPLES</span></span>

### <span data-ttu-id="7f107-108">Esempio 1: ottenere il gruppo di sicurezza di rete effettivo in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="7f107-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="7f107-109">Questo comando consente di ottenere tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7f107-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="7f107-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f107-110">PARAMETERS</span></span>

### <span data-ttu-id="7f107-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7f107-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="7f107-112">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f107-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="7f107-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f107-113">-ResourceGroupName</span></span>
<span data-ttu-id="7f107-114">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7f107-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="7f107-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f107-115">-DefaultProfile</span></span>
<span data-ttu-id="7f107-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f107-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f107-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f107-117">CommonParameters</span></span>
<span data-ttu-id="7f107-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f107-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f107-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f107-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f107-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f107-120">INPUTS</span></span>

## <span data-ttu-id="7f107-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f107-121">OUTPUTS</span></span>

### <span data-ttu-id="7f107-122">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f107-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="7f107-123">Note</span><span class="sxs-lookup"><span data-stu-id="7f107-123">NOTES</span></span>

## <span data-ttu-id="7f107-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f107-124">RELATED LINKS</span></span>

[<span data-ttu-id="7f107-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7f107-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


