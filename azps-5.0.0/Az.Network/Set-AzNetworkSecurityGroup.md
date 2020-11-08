---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200698"
---
# <span data-ttu-id="dfc76-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dfc76-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="dfc76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfc76-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc76-103">Aggiorna un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="dfc76-103">Updates a network security group.</span></span>

## <span data-ttu-id="dfc76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfc76-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfc76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfc76-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc76-106">Il cmdlet **set-AzNetworkSecurityGroup** aggiorna un gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="dfc76-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="dfc76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfc76-107">EXAMPLES</span></span>

### <span data-ttu-id="dfc76-108">Esempio 1: aggiornare un gruppo di sicurezza di rete esistente</span><span class="sxs-lookup"><span data-stu-id="dfc76-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="dfc76-109">Questo comando ottiene il gruppo di sicurezza di rete di Azure denominato Nsg1 e aggiunge una regola di sicurezza di rete denominata Rdp-Rule per consentire il traffico Internet sulla porta 3389 per l'oggetto del gruppo di sicurezza di rete recuperato tramite Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="dfc76-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="dfc76-110">Il comando mantiene il gruppo di sicurezza di rete di Azure modificato usando **set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="dfc76-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="dfc76-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfc76-111">PARAMETERS</span></span>

### <span data-ttu-id="dfc76-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfc76-112">-AsJob</span></span>
<span data-ttu-id="dfc76-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dfc76-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc76-114">-DefaultProfile</span></span>
<span data-ttu-id="dfc76-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfc76-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfc76-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dfc76-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="dfc76-117">Specifica un oggetto gruppo di sicurezza di rete che rappresenta lo stato in cui deve essere impostato il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="dfc76-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc76-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfc76-118">-Confirm</span></span>
<span data-ttu-id="dfc76-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfc76-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc76-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc76-120">-WhatIf</span></span>
<span data-ttu-id="dfc76-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfc76-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfc76-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfc76-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc76-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc76-123">CommonParameters</span></span>
<span data-ttu-id="dfc76-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfc76-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc76-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfc76-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc76-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfc76-126">INPUTS</span></span>

### <span data-ttu-id="dfc76-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dfc76-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="dfc76-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfc76-128">OUTPUTS</span></span>

### <span data-ttu-id="dfc76-129">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dfc76-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="dfc76-130">Note</span><span class="sxs-lookup"><span data-stu-id="dfc76-130">NOTES</span></span>

## <span data-ttu-id="dfc76-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfc76-131">RELATED LINKS</span></span>

[<span data-ttu-id="dfc76-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dfc76-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dfc76-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dfc76-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="dfc76-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dfc76-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


