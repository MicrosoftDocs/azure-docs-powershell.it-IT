---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8d8254b5002edcf40b0807e296ab680ea32ca10e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688273"
---
# <span data-ttu-id="73c16-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73c16-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="73c16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73c16-102">SYNOPSIS</span></span>
<span data-ttu-id="73c16-103">Ottiene una configurazione IP dell'interfaccia di rete per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="73c16-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73c16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73c16-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73c16-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73c16-105">DESCRIPTION</span></span>
<span data-ttu-id="73c16-106">Il cmdlet **Get-AzureRmNetworkInterfaceIPConfig** ottiene una configurazione IP di interfaccia di rete da un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="73c16-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="73c16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73c16-107">EXAMPLES</span></span>

### <span data-ttu-id="73c16-108">1: ottenere una configurazione IP di un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="73c16-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="73c16-109">Il primo comando ottiene un'interfaccia di rete esistente denominata MYNIC e la archivia nella variabile $nic 1.</span><span class="sxs-lookup"><span data-stu-id="73c16-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="73c16-110">Il secondo comando consente di ottenere la configurazione IP denominata Ipconfig1 di questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="73c16-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="73c16-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73c16-111">PARAMETERS</span></span>

### <span data-ttu-id="73c16-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c16-112">-DefaultProfile</span></span>
<span data-ttu-id="73c16-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73c16-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73c16-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="73c16-114">-Name</span></span>
<span data-ttu-id="73c16-115">Specifica il nome della configurazione IP di rete che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="73c16-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="73c16-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="73c16-116">-NetworkInterface</span></span>
<span data-ttu-id="73c16-117">Specifica un oggetto **NetworkInterface** che contiene la configurazione IP di rete che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="73c16-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="73c16-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c16-118">CommonParameters</span></span>
<span data-ttu-id="73c16-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c16-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c16-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c16-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c16-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73c16-121">INPUTS</span></span>

### <span data-ttu-id="73c16-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="73c16-122">PSNetworkInterface</span></span>
<span data-ttu-id="73c16-123">Il parametro ' NetworkInterface ' accetta il valore di tipo ' PSNetworkInterface ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="73c16-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="73c16-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73c16-124">OUTPUTS</span></span>

### <span data-ttu-id="73c16-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="73c16-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="73c16-126">Note</span><span class="sxs-lookup"><span data-stu-id="73c16-126">NOTES</span></span>
* <span data-ttu-id="73c16-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="73c16-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="73c16-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73c16-128">RELATED LINKS</span></span>

[<span data-ttu-id="73c16-129">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73c16-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="73c16-130">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73c16-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="73c16-131">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73c16-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="73c16-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="73c16-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)

