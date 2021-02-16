---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189735"
---
# <span data-ttu-id="d9ae8-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d9ae8-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d9ae8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ae8-103">Ottiene una configurazione IP dell'interfaccia di rete per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="d9ae8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9ae8-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9ae8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ae8-106">Il cmdlet **Get-AzNetworkInterfaceIPConfig ottiene** una configurazione IP dell'interfaccia di rete da un'interfaccia di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="d9ae8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9ae8-107">EXAMPLES</span></span>

### <span data-ttu-id="d9ae8-108">1: Ottenere una configurazione IP di un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="d9ae8-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="d9ae8-109">Il primo comando ottiene un'interfaccia di rete esistente denominata mynic e la archivia nella variabile $nic 1.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="d9ae8-110">Il secondo comando ottiene la configurazione IP denominata ipconfig1 di questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="d9ae8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ae8-111">PARAMETERS</span></span>

### <span data-ttu-id="d9ae8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ae8-112">-DefaultProfile</span></span>
<span data-ttu-id="d9ae8-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9ae8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ae8-114">-Name</span></span>
<span data-ttu-id="d9ae8-115">Specifica il nome della configurazione IP di rete che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9ae8-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d9ae8-116">-NetworkInterface</span></span>
<span data-ttu-id="d9ae8-117">Specifica un oggetto **NetworkInterface** che contiene la configurazione IP di rete che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9ae8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ae8-118">CommonParameters</span></span>
<span data-ttu-id="d9ae8-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ae8-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9ae8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ae8-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9ae8-121">INPUTS</span></span>

### <span data-ttu-id="d9ae8-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d9ae8-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d9ae8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9ae8-123">OUTPUTS</span></span>

### <span data-ttu-id="d9ae8-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9ae8-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="d9ae8-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9ae8-125">NOTES</span></span>
* <span data-ttu-id="d9ae8-126">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="d9ae8-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d9ae8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9ae8-127">RELATED LINKS</span></span>

[<span data-ttu-id="d9ae8-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d9ae8-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d9ae8-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d9ae8-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d9ae8-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d9ae8-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d9ae8-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d9ae8-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


