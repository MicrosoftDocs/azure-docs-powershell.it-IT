---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 1252c452cc6ad7996a8dcddcb915da251b0b5039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678097"
---
# <span data-ttu-id="d3609-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3609-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="d3609-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3609-102">SYNOPSIS</span></span>
<span data-ttu-id="d3609-103">Rimuove una regola di sicurezza di rete da un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d3609-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="d3609-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3609-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3609-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3609-105">DESCRIPTION</span></span>
<span data-ttu-id="d3609-106">Il cmdlet **Remove-AzNetworkSecurityRuleConfig** rimuove una configurazione della regola di sicurezza di rete da un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3609-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="d3609-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3609-107">EXAMPLES</span></span>

### <span data-ttu-id="d3609-108">Esempio 1: rimuovere una configurazione della regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="d3609-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="d3609-109">Il primo comando crea una configurazione della regola di sicurezza di rete denominata RDP-Rule e quindi la archivia nella variabile $rule 1.</span><span class="sxs-lookup"><span data-stu-id="d3609-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="d3609-110">Il secondo comando crea un gruppo di sicurezza di rete usando la regola in $rule 1 e quindi archivia il gruppo di sicurezza della rete nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="d3609-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="d3609-111">Il terzo comando rimuove la configurazione della regola di sicurezza di rete denominata RDP-Rule dal gruppo di sicurezza della rete in $nsg.</span><span class="sxs-lookup"><span data-stu-id="d3609-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="d3609-112">Il comando avanti salva la modifica.</span><span class="sxs-lookup"><span data-stu-id="d3609-112">The forth command saves the change.</span></span>

## <span data-ttu-id="d3609-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3609-113">PARAMETERS</span></span>

### <span data-ttu-id="d3609-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3609-114">-DefaultProfile</span></span>
<span data-ttu-id="d3609-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3609-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3609-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3609-116">-Name</span></span>
<span data-ttu-id="d3609-117">Specifica il nome della configurazione della regola di sicurezza della rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3609-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d3609-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d3609-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="d3609-119">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="d3609-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="d3609-120">Questo oggetto contiene la configurazione della regola di sicurezza della rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d3609-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="d3609-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3609-121">CommonParameters</span></span>
<span data-ttu-id="d3609-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3609-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3609-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3609-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3609-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3609-124">INPUTS</span></span>

### <span data-ttu-id="d3609-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d3609-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d3609-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3609-126">OUTPUTS</span></span>

### <span data-ttu-id="d3609-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d3609-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="d3609-128">Note</span><span class="sxs-lookup"><span data-stu-id="d3609-128">NOTES</span></span>

## <span data-ttu-id="d3609-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3609-129">RELATED LINKS</span></span>

[<span data-ttu-id="d3609-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3609-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d3609-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3609-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d3609-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d3609-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="d3609-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3609-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="d3609-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3609-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

