---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 91144275806c5e3a6913d39990ad68644c71b244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003309"
---
# <span data-ttu-id="d85a3-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d85a3-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="d85a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d85a3-103">Aggiorna un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d85a3-103">Updates a network security group.</span></span>

## <span data-ttu-id="d85a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d85a3-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d85a3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d85a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d85a3-106">Il cmdlet **Set-AzNetworkSecurityGroup** aggiorna un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d85a3-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="d85a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d85a3-107">EXAMPLES</span></span>

### <span data-ttu-id="d85a3-108">Esempio 1: Aggiornare un gruppo di sicurezza di rete esistente</span><span class="sxs-lookup"><span data-stu-id="d85a3-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="d85a3-109">Questo comando ottiene il gruppo di sicurezza di rete Azure denominato Nsg1 e aggiunge una regola di sicurezza di rete denominata Rdp-Rule per consentire il traffico Internet sulla porta 3389 all'oggetto gruppo di sicurezza di rete recuperato usando Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="d85a3-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="d85a3-110">Il comando mantiene il gruppo di sicurezza di rete Azure modificato usando **Set-AzNetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="d85a3-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="d85a3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d85a3-111">PARAMETERS</span></span>

### <span data-ttu-id="d85a3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d85a3-112">-AsJob</span></span>
<span data-ttu-id="d85a3-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d85a3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d85a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85a3-114">-DefaultProfile</span></span>
<span data-ttu-id="d85a3-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d85a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d85a3-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d85a3-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d85a3-117">Specifica un oggetto gruppo di sicurezza di rete che rappresenta lo stato su cui deve essere impostato il gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d85a3-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="d85a3-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d85a3-118">-Confirm</span></span>
<span data-ttu-id="d85a3-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d85a3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d85a3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d85a3-120">-WhatIf</span></span>
<span data-ttu-id="d85a3-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d85a3-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d85a3-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d85a3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d85a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85a3-123">CommonParameters</span></span>
<span data-ttu-id="d85a3-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85a3-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d85a3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85a3-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d85a3-126">INPUTS</span></span>

### <span data-ttu-id="d85a3-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d85a3-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d85a3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d85a3-128">OUTPUTS</span></span>

### <span data-ttu-id="d85a3-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d85a3-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d85a3-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="d85a3-130">NOTES</span></span>

## <span data-ttu-id="d85a3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d85a3-131">RELATED LINKS</span></span>

[<span data-ttu-id="d85a3-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d85a3-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="d85a3-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d85a3-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="d85a3-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d85a3-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


