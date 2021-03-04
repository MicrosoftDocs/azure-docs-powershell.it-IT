---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 6ed82377de2a87b3bc40d3d4e8dff6af751ed1f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958590"
---
# <span data-ttu-id="6aabe-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6aabe-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="6aabe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aabe-102">SYNOPSIS</span></span>
<span data-ttu-id="6aabe-103">Crea un oggetto di configurazione IP della configurazione ip del contenitore.</span><span class="sxs-lookup"><span data-stu-id="6aabe-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="6aabe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6aabe-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aabe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6aabe-105">DESCRIPTION</span></span>
<span data-ttu-id="6aabe-106">Il cmdlet **New-AzContainerNicConfigIpConfig crea** una nuova configurazione IP di configurazione dell'interfaccia di rete del contenitore.</span><span class="sxs-lookup"><span data-stu-id="6aabe-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="6aabe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6aabe-107">EXAMPLES</span></span>

### <span data-ttu-id="6aabe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6aabe-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="6aabe-109">I primi due comandi creano e inizializzano una vnet e una subnet.</span><span class="sxs-lookup"><span data-stu-id="6aabe-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="6aabe-110">Il terzo comando crea un profilo di configurazione ip contenitore nic che fa riferimento alla subnet creata.</span><span class="sxs-lookup"><span data-stu-id="6aabe-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="6aabe-111">Il quarto comando crea una configurazione dell'interfaccia di rete contenitore che fornisce il profilo di configurazione IP creato nel comando precedente.</span><span class="sxs-lookup"><span data-stu-id="6aabe-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="6aabe-112">Infine, il quinto comando crea un profilo di rete inizializzato con la configurazione dell'interfaccia di rete contenitore archiviata in $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="6aabe-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="6aabe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6aabe-113">PARAMETERS</span></span>

### <span data-ttu-id="6aabe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aabe-114">-DefaultProfile</span></span>
<span data-ttu-id="6aabe-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6aabe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aabe-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6aabe-116">-Name</span></span>
<span data-ttu-id="6aabe-117">Nome del profilo di configurazione IP della configurazione dell'interfaccia di rete dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="6aabe-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="6aabe-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6aabe-118">-Subnet</span></span>
<span data-ttu-id="6aabe-119">Subnet</span><span class="sxs-lookup"><span data-stu-id="6aabe-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aabe-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6aabe-120">-SubnetId</span></span>
<span data-ttu-id="6aabe-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="6aabe-121">SubnetId</span></span>

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

### <span data-ttu-id="6aabe-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aabe-122">-Confirm</span></span>
<span data-ttu-id="6aabe-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aabe-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aabe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aabe-124">-WhatIf</span></span>
<span data-ttu-id="6aabe-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6aabe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aabe-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6aabe-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aabe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aabe-127">CommonParameters</span></span>
<span data-ttu-id="6aabe-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aabe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aabe-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aabe-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aabe-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="6aabe-130">INPUTS</span></span>

### <span data-ttu-id="6aabe-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6aabe-131">None</span></span>

## <span data-ttu-id="6aabe-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6aabe-132">OUTPUTS</span></span>

### <span data-ttu-id="6aabe-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6aabe-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="6aabe-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="6aabe-134">NOTES</span></span>

## <span data-ttu-id="6aabe-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6aabe-135">RELATED LINKS</span></span>

[<span data-ttu-id="6aabe-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6aabe-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
