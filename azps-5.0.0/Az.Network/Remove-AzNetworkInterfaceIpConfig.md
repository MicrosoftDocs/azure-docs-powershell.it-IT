---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200716"
---
# <span data-ttu-id="c0e78-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c0e78-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="c0e78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0e78-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e78-103">Rimuove una configurazione IP dell'interfaccia di rete da un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c0e78-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="c0e78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0e78-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0e78-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0e78-105">DESCRIPTION</span></span>
<span data-ttu-id="c0e78-106">Il cmdlet **Remove-AzNetworkInterfaceIpConfig** consente di rimuovere una configurazione IP di interfaccia di rete da un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e78-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="c0e78-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0e78-107">EXAMPLES</span></span>

### <span data-ttu-id="c0e78-108">Esempio 1: eliminare una configurazione IP da un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="c0e78-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="c0e78-109">Il primo comando ottiene un'interfaccia di rete denominata MYNIC e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="c0e78-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="c0e78-110">Il secondo comando rimuove la configurazione IP chiamata IPConfig-1 associata a questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c0e78-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="c0e78-111">Il terzo comando imposta le modifiche apportate all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="c0e78-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="c0e78-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0e78-112">PARAMETERS</span></span>

### <span data-ttu-id="c0e78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e78-113">-DefaultProfile</span></span>
<span data-ttu-id="c0e78-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e78-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0e78-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0e78-115">-Name</span></span>
<span data-ttu-id="c0e78-116">Specifica il nome della configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c0e78-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="c0e78-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c0e78-117">-NetworkInterface</span></span>
<span data-ttu-id="c0e78-118">Specifica un oggetto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="c0e78-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="c0e78-119">Questo oggetto contiene la configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c0e78-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="c0e78-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e78-120">CommonParameters</span></span>
<span data-ttu-id="c0e78-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e78-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e78-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e78-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e78-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0e78-123">INPUTS</span></span>

### <span data-ttu-id="c0e78-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c0e78-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c0e78-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0e78-125">OUTPUTS</span></span>

### <span data-ttu-id="c0e78-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c0e78-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c0e78-127">Note</span><span class="sxs-lookup"><span data-stu-id="c0e78-127">NOTES</span></span>
* <span data-ttu-id="c0e78-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="c0e78-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c0e78-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0e78-129">RELATED LINKS</span></span>

[<span data-ttu-id="c0e78-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c0e78-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c0e78-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c0e78-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c0e78-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c0e78-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c0e78-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c0e78-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)

