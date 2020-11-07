---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: aaace7e8bb7d1f2ed57ebad28f7b5a3399f0e190
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854446"
---
# <span data-ttu-id="031cf-101">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="031cf-101">New-AzContainerNicConfig</span></span>

## <span data-ttu-id="031cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="031cf-102">SYNOPSIS</span></span>
<span data-ttu-id="031cf-103">Crea un nuovo oggetto di configurazione dell'interfaccia di rete contenitore.</span><span class="sxs-lookup"><span data-stu-id="031cf-103">Creates a new container network interface configuration object.</span></span>

## <span data-ttu-id="031cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="031cf-104">SYNTAX</span></span>

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="031cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="031cf-105">DESCRIPTION</span></span>
<span data-ttu-id="031cf-106">Il cmdlet **New-AzContainerNicConfig** crea un nuovo oggetto di configurazione dell'interfaccia di rete contenitore.</span><span class="sxs-lookup"><span data-stu-id="031cf-106">The **New-AzContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="031cf-107">Questo oggetto determina le caratteristiche dell'interfaccia di rete contenitore create facendo riferimento al profilo di rete padre.</span><span class="sxs-lookup"><span data-stu-id="031cf-107">This object determines the characteristics of container network interface created referencing the parent network profile.</span></span>

## <span data-ttu-id="031cf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="031cf-108">EXAMPLES</span></span>

### <span data-ttu-id="031cf-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="031cf-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="031cf-110">Il primo comando crea una configurazione di interfaccia di rete contenitore vuota.</span><span class="sxs-lookup"><span data-stu-id="031cf-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="031cf-111">Il secondo crea un nuovo profilo di rete, passando la configurazione dell'interfaccia di rete del contenitore creato in precedenza come argomento al cmdlet New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="031cf-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="031cf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="031cf-112">PARAMETERS</span></span>

### <span data-ttu-id="031cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="031cf-113">-DefaultProfile</span></span>
<span data-ttu-id="031cf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="031cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="031cf-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="031cf-115">-IpConfiguration</span></span>
<span data-ttu-id="031cf-116">Raccolta di profili di configurazione IP che determinano quali configurazioni IP vengono create quando viene creata un'istanza di nic contenitore da questa configurazione dell'interfaccia di rete del contenitore</span><span class="sxs-lookup"><span data-stu-id="031cf-116">Collection of IP configuration profiles which determine what ip configurations are created when a container nic is instantiated from this container network interface configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031cf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="031cf-117">-Name</span></span>
<span data-ttu-id="031cf-118">Nome della configurazione dell'interfaccia di rete del contenitore.</span><span class="sxs-lookup"><span data-stu-id="031cf-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="031cf-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="031cf-119">-Confirm</span></span>
<span data-ttu-id="031cf-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="031cf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="031cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="031cf-121">-WhatIf</span></span>
<span data-ttu-id="031cf-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="031cf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="031cf-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="031cf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="031cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031cf-124">CommonParameters</span></span>
<span data-ttu-id="031cf-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="031cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031cf-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="031cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031cf-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="031cf-127">INPUTS</span></span>

### <span data-ttu-id="031cf-128">Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile []</span><span class="sxs-lookup"><span data-stu-id="031cf-128">Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]</span></span>

## <span data-ttu-id="031cf-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="031cf-129">OUTPUTS</span></span>

### <span data-ttu-id="031cf-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="031cf-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="031cf-131">Note</span><span class="sxs-lookup"><span data-stu-id="031cf-131">NOTES</span></span>

## <span data-ttu-id="031cf-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="031cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="031cf-133">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="031cf-133">New-AzContainerNicConfigIpConfig</span></span>](./New-AzContainerNicConfigIpConfig.md)
