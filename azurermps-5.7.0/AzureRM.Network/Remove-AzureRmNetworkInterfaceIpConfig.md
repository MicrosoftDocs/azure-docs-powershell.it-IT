---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9cbb814fde6d81449228a18913254cf807d5502c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509787"
---
# <span data-ttu-id="68225-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="68225-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="68225-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68225-102">SYNOPSIS</span></span>
<span data-ttu-id="68225-103">Rimuove una configurazione IP dell'interfaccia di rete da un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="68225-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68225-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68225-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68225-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68225-105">DESCRIPTION</span></span>
<span data-ttu-id="68225-106">Il cmdlet **Remove-AzureRmNetworkInterfaceIpConfig** consente di rimuovere una configurazione IP di interfaccia di rete da un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="68225-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="68225-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68225-107">EXAMPLES</span></span>

### <span data-ttu-id="68225-108">1: eliminare una configurazione IP da un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="68225-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="68225-109">Il primo comando ottiene un'interfaccia di rete denominata MYNIC e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="68225-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="68225-110">Il secondo comando rimuove la configurazione IP chiamata IPConfig-1 associata a questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="68225-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="68225-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68225-111">PARAMETERS</span></span>

### <span data-ttu-id="68225-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68225-112">-DefaultProfile</span></span>
<span data-ttu-id="68225-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68225-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68225-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="68225-114">-Name</span></span>
<span data-ttu-id="68225-115">Specifica il nome della configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="68225-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68225-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68225-116">-NetworkInterface</span></span>
<span data-ttu-id="68225-117">Specifica un oggetto **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="68225-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="68225-118">Questo oggetto contiene la configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="68225-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="68225-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68225-119">CommonParameters</span></span>
<span data-ttu-id="68225-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68225-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68225-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68225-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68225-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68225-122">INPUTS</span></span>

### <span data-ttu-id="68225-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68225-123">PSNetworkInterface</span></span>
<span data-ttu-id="68225-124">Il parametro ' NetworkInterface ' accetta il valore di tipo ' PSNetworkInterface ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="68225-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="68225-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68225-125">OUTPUTS</span></span>

### <span data-ttu-id="68225-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68225-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="68225-127">Note</span><span class="sxs-lookup"><span data-stu-id="68225-127">NOTES</span></span>
* <span data-ttu-id="68225-128">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="68225-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="68225-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68225-129">RELATED LINKS</span></span>

[<span data-ttu-id="68225-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="68225-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="68225-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="68225-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="68225-132">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="68225-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="68225-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="68225-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)

