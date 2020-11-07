---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 18b363abb6f96eae2a128b869d9930efdde7f41e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853721"
---
# <span data-ttu-id="fd27b-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fd27b-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="fd27b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd27b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd27b-103">Ottiene una configurazione IP dell'interfaccia di rete per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="fd27b-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="fd27b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd27b-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd27b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd27b-105">DESCRIPTION</span></span>
<span data-ttu-id="fd27b-106">Il cmdlet **Get-AzNetworkInterfaceIPConfig** ottiene una configurazione IP di interfaccia di rete da un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="fd27b-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="fd27b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd27b-107">EXAMPLES</span></span>

### <span data-ttu-id="fd27b-108">1: ottenere una configurazione IP di un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="fd27b-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="fd27b-109">Il primo comando ottiene un'interfaccia di rete esistente denominata MYNIC e la archivia nella variabile $nic 1.</span><span class="sxs-lookup"><span data-stu-id="fd27b-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="fd27b-110">Il secondo comando consente di ottenere la configurazione IP denominata Ipconfig1 di questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="fd27b-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="fd27b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd27b-111">PARAMETERS</span></span>

### <span data-ttu-id="fd27b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd27b-112">-DefaultProfile</span></span>
<span data-ttu-id="fd27b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd27b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd27b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd27b-114">-Name</span></span>
<span data-ttu-id="fd27b-115">Specifica il nome della configurazione IP di rete che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="fd27b-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd27b-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fd27b-116">-NetworkInterface</span></span>
<span data-ttu-id="fd27b-117">Specifica un oggetto **NetworkInterface** che contiene la configurazione IP di rete che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="fd27b-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fd27b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd27b-118">CommonParameters</span></span>
<span data-ttu-id="fd27b-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd27b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd27b-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd27b-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd27b-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd27b-121">INPUTS</span></span>

### <span data-ttu-id="fd27b-122">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fd27b-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="fd27b-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd27b-123">OUTPUTS</span></span>

### <span data-ttu-id="fd27b-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd27b-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="fd27b-125">Note</span><span class="sxs-lookup"><span data-stu-id="fd27b-125">NOTES</span></span>
* <span data-ttu-id="fd27b-126">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="fd27b-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fd27b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd27b-127">RELATED LINKS</span></span>

[<span data-ttu-id="fd27b-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fd27b-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fd27b-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fd27b-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fd27b-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fd27b-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="fd27b-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fd27b-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


