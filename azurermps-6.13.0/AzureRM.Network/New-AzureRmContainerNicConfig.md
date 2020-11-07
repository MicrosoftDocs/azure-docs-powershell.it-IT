---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfig.md
ms.openlocfilehash: b697fcd991304401e2af754cc223f19b956f2143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688392"
---
# <span data-ttu-id="dbd73-101">New-AzureRmNetworkProfileContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="dbd73-101">New-AzureRmNetworkProfileContainerNicConfig</span></span>

## <span data-ttu-id="dbd73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbd73-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd73-103">Crea un nuovo oggetto di configurazione dell'interfaccia di rete contenitore.</span><span class="sxs-lookup"><span data-stu-id="dbd73-103">Creates a new container network interface configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbd73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbd73-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbd73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbd73-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd73-106">Il cmdlet **New-AzureRmNetworkProfileContainerNicConfig** crea un nuovo oggetto di configurazione dell'interfaccia di rete contenitore.</span><span class="sxs-lookup"><span data-stu-id="dbd73-106">The **New-AzureRmNetworkProfileContainerNicConfig** cmdlet creates a new container network interface configuration object.</span></span> <span data-ttu-id="dbd73-107">Questo oggetto determina le caratteristiche della rete di contenitori interfacs creata facendo riferimento al profilo di rete padre.</span><span class="sxs-lookup"><span data-stu-id="dbd73-107">This object determines the characteristics of container network interfacs created referencing the parent network profile.</span></span>

## <span data-ttu-id="dbd73-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbd73-108">EXAMPLES</span></span>

### <span data-ttu-id="dbd73-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbd73-109">Example 1</span></span>
```powershell
$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="dbd73-110">Il primo comando crea una configurazione di interfaccia di rete contenitore vuota.</span><span class="sxs-lookup"><span data-stu-id="dbd73-110">The first command creates an empty container network interface configuration.</span></span> <span data-ttu-id="dbd73-111">Il secondo crea un nuovo profilo di rete, passando la configurazione dell'interfaccia di rete del contenitore creato in precedenza come argomento al cmdlet New-NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="dbd73-111">The second creates a new network profile, passing the previously created container network interface configuration as an argument to the New-NetworkProfile cmdlet.</span></span>

## <span data-ttu-id="dbd73-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbd73-112">PARAMETERS</span></span>

### <span data-ttu-id="dbd73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd73-113">-DefaultProfile</span></span>
<span data-ttu-id="dbd73-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd73-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbd73-115">-IpConfiguration</span></span>
<span data-ttu-id="dbd73-116">{{Fill IpConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="dbd73-116">{{Fill IpConfiguration Description}}</span></span>

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

### <span data-ttu-id="dbd73-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbd73-117">-Name</span></span>
<span data-ttu-id="dbd73-118">Nome della configurazione dell'interfaccia di rete del contenitore.</span><span class="sxs-lookup"><span data-stu-id="dbd73-118">Name of the container network interface configuration.</span></span>

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

### <span data-ttu-id="dbd73-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dbd73-119">-Confirm</span></span>
<span data-ttu-id="dbd73-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbd73-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd73-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd73-121">-WhatIf</span></span>
<span data-ttu-id="dbd73-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbd73-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbd73-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbd73-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd73-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd73-124">CommonParameters</span></span>
<span data-ttu-id="dbd73-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbd73-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd73-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd73-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd73-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbd73-127">INPUTS</span></span>

### <span data-ttu-id="dbd73-128">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSIPConfigurationProfile, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dbd73-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dbd73-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbd73-129">OUTPUTS</span></span>

### <span data-ttu-id="dbd73-130">Microsoft. Azure. Commands. Network. Models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="dbd73-130">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="dbd73-131">Note</span><span class="sxs-lookup"><span data-stu-id="dbd73-131">NOTES</span></span>

## <span data-ttu-id="dbd73-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbd73-132">RELATED LINKS</span></span>
