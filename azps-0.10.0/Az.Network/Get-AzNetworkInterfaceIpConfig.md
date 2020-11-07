---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 5936a7e3f15919e00fa052a2950fd31e69ca32fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860757"
---
# <span data-ttu-id="9ae7b-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ae7b-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="9ae7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ae7b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae7b-103">Ottiene una configurazione IP dell'interfaccia di rete per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="9ae7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ae7b-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ae7b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ae7b-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae7b-106">Il cmdlet **Get-AzNetworkInterfaceIPConfig** ottiene una configurazione IP di interfaccia di rete da un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="9ae7b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ae7b-107">EXAMPLES</span></span>

### <span data-ttu-id="9ae7b-108">1: ottenere una configurazione IP di un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="9ae7b-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="9ae7b-109">Il primo comando ottiene un'interfaccia di rete esistente denominata MYNIC e la archivia nella variabile $nic 1.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="9ae7b-110">Il secondo comando consente di ottenere la configurazione IP denominata Ipconfig1 di questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="9ae7b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ae7b-111">PARAMETERS</span></span>

### <span data-ttu-id="9ae7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae7b-112">-DefaultProfile</span></span>
<span data-ttu-id="9ae7b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ae7b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ae7b-114">-Name</span></span>
<span data-ttu-id="9ae7b-115">Specifica il nome della configurazione IP di rete che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ae7b-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9ae7b-116">-NetworkInterface</span></span>
<span data-ttu-id="9ae7b-117">Specifica un oggetto **NetworkInterface** che contiene la configurazione IP di rete che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ae7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae7b-118">CommonParameters</span></span>
<span data-ttu-id="9ae7b-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae7b-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ae7b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae7b-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ae7b-121">INPUTS</span></span>

### <span data-ttu-id="9ae7b-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9ae7b-122">PSNetworkInterface</span></span>
<span data-ttu-id="9ae7b-123">Il parametro ' NetworkInterface ' accetta il valore di tipo ' PSNetworkInterface ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9ae7b-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="9ae7b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ae7b-124">OUTPUTS</span></span>

### <span data-ttu-id="9ae7b-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ae7b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="9ae7b-126">Note</span><span class="sxs-lookup"><span data-stu-id="9ae7b-126">NOTES</span></span>
* <span data-ttu-id="9ae7b-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="9ae7b-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9ae7b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ae7b-128">RELATED LINKS</span></span>

[<span data-ttu-id="9ae7b-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ae7b-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ae7b-130">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ae7b-130">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ae7b-131">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ae7b-131">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ae7b-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ae7b-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


