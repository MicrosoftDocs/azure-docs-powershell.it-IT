---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517475"
---
# <span data-ttu-id="c63fc-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c63fc-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="c63fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c63fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c63fc-103">Crea un oggetto di configurazione IP del contenitore nic.</span><span class="sxs-lookup"><span data-stu-id="c63fc-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c63fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c63fc-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c63fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c63fc-105">DESCRIPTION</span></span>
<span data-ttu-id="c63fc-106">Il cmdlet **New-AzureRmNetworkProfileContainerNicConfigIpConfig** crea una nuova configurazione IP di configurazione dell'interfaccia di rete container.</span><span class="sxs-lookup"><span data-stu-id="c63fc-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="c63fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c63fc-107">EXAMPLES</span></span>

### <span data-ttu-id="c63fc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c63fc-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="c63fc-109">I primi due comandi creano e inizializzano una VNET e una subnet.</span><span class="sxs-lookup"><span data-stu-id="c63fc-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="c63fc-110">Il terzo comando crea un profilo di configurazione IP del contenitore NIC che fa riferimento alla subnet creata.</span><span class="sxs-lookup"><span data-stu-id="c63fc-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="c63fc-111">Il quarto comando crea una configurazione di interfaccia di rete contenitore che fornisce il profilo di configurazione IP creato nel comando precedente.</span><span class="sxs-lookup"><span data-stu-id="c63fc-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="c63fc-112">Infine, il quinto comando crea un profilo di rete inizializzato con la configurazione dell'interfaccia di rete contenitore archiviata in $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="c63fc-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="c63fc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c63fc-113">PARAMETERS</span></span>

### <span data-ttu-id="c63fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63fc-114">-DefaultProfile</span></span>
<span data-ttu-id="c63fc-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c63fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63fc-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c63fc-116">-Name</span></span>
<span data-ttu-id="c63fc-117">Nome del profilo di configurazione IP della configurazione dell'interfaccia di rete contenitore.</span><span class="sxs-lookup"><span data-stu-id="c63fc-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="c63fc-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="c63fc-118">-Subnet</span></span>
<span data-ttu-id="c63fc-119">Subnet</span><span class="sxs-lookup"><span data-stu-id="c63fc-119">Subnet</span></span>

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

### <span data-ttu-id="c63fc-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c63fc-120">-SubnetId</span></span>
<span data-ttu-id="c63fc-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="c63fc-121">SubnetId</span></span>

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

### <span data-ttu-id="c63fc-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c63fc-122">-Confirm</span></span>
<span data-ttu-id="c63fc-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63fc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c63fc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c63fc-124">-WhatIf</span></span>
<span data-ttu-id="c63fc-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c63fc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c63fc-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c63fc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c63fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63fc-127">CommonParameters</span></span>
<span data-ttu-id="c63fc-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63fc-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c63fc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63fc-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c63fc-130">INPUTS</span></span>

### <span data-ttu-id="c63fc-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c63fc-131">None</span></span>

## <span data-ttu-id="c63fc-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c63fc-132">OUTPUTS</span></span>

### <span data-ttu-id="c63fc-133">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c63fc-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c63fc-134">Note</span><span class="sxs-lookup"><span data-stu-id="c63fc-134">NOTES</span></span>

## <span data-ttu-id="c63fc-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c63fc-135">RELATED LINKS</span></span>
