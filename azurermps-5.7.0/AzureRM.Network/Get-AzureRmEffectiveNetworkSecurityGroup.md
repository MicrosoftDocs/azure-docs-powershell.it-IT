---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: a7c131db8ce5a3489bc2a869e31b0ef7ab89f3c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686476"
---
# <span data-ttu-id="3ab9a-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3ab9a-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="3ab9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ab9a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab9a-103">Ottiene il gruppo di sicurezza di rete effettivo di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ab9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ab9a-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ab9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ab9a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ab9a-106">Il cmdlet **Get-AzureRmEffectiveNetworkSecurityGroup** restituisce il gruppo di sicurezza di rete effettivo applicato a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="3ab9a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ab9a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ab9a-108">Esempio 1: ottenere il gruppo di sicurezza di rete effettivo in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="3ab9a-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="3ab9a-109">Questo comando consente di ottenere tutte le regole di sicurezza di rete effettive associate all'interfaccia di rete denominata MyNetworkInterface nel gruppo di risorse denominato myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="3ab9a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ab9a-110">PARAMETERS</span></span>

### <span data-ttu-id="3ab9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab9a-111">-DefaultProfile</span></span>
<span data-ttu-id="3ab9a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ab9a-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="3ab9a-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="3ab9a-114">Specifica il nome di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="3ab9a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab9a-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ab9a-116">Specifica il gruppo di risorse di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="3ab9a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab9a-117">CommonParameters</span></span>
<span data-ttu-id="3ab9a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab9a-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ab9a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab9a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ab9a-120">INPUTS</span></span>

### <span data-ttu-id="3ab9a-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ab9a-121">None</span></span>
<span data-ttu-id="3ab9a-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3ab9a-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ab9a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ab9a-123">OUTPUTS</span></span>

### <span data-ttu-id="3ab9a-124">Microsoft. Azure. Commands. Network. Models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3ab9a-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="3ab9a-125">Note</span><span class="sxs-lookup"><span data-stu-id="3ab9a-125">NOTES</span></span>

## <span data-ttu-id="3ab9a-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ab9a-126">RELATED LINKS</span></span>

[<span data-ttu-id="3ab9a-127">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ab9a-127">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


