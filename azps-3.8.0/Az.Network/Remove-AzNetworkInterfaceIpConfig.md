---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 784374b620af09b00f460ff5c50d0a08baa46233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021977"
---
# <span data-ttu-id="fcb4c-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fcb4c-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="fcb4c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fcb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb4c-103">Rimuove una configurazione IP dell'interfaccia di rete da un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="fcb4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fcb4c-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcb4c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="fcb4c-106">Il cmdlet **Remove-AzNetworkInterfaceIpConfig** consente di rimuovere una configurazione IP di interfaccia di rete da un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="fcb4c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fcb4c-107">EXAMPLES</span></span>

### <span data-ttu-id="fcb4c-108">1: eliminare una configurazione IP da un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="fcb4c-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="fcb4c-109">Il primo comando ottiene un'interfaccia di rete denominata MYNIC e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="fcb4c-110">Il secondo comando rimuove la configurazione IP chiamata IPConfig-1 associata a questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="fcb4c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fcb4c-111">PARAMETERS</span></span>

### <span data-ttu-id="fcb4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb4c-112">-DefaultProfile</span></span>
<span data-ttu-id="fcb4c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcb4c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcb4c-114">-Name</span></span>
<span data-ttu-id="fcb4c-115">Specifica il nome della configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcb4c-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fcb4c-116">-NetworkInterface</span></span>
<span data-ttu-id="fcb4c-117">Specifica un oggetto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="fcb4c-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="fcb4c-118">Questo oggetto contiene la configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcb4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb4c-119">CommonParameters</span></span>
<span data-ttu-id="fcb4c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb4c-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb4c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb4c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fcb4c-122">INPUTS</span></span>

### <span data-ttu-id="fcb4c-123">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fcb4c-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="fcb4c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fcb4c-124">OUTPUTS</span></span>

### <span data-ttu-id="fcb4c-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fcb4c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="fcb4c-126">Note</span><span class="sxs-lookup"><span data-stu-id="fcb4c-126">NOTES</span></span>
* <span data-ttu-id="fcb4c-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="fcb4c-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fcb4c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fcb4c-128">RELATED LINKS</span></span>

[<span data-ttu-id="fcb4c-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fcb4c-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fcb4c-130">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fcb4c-130">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fcb4c-131">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fcb4c-131">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fcb4c-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fcb4c-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


