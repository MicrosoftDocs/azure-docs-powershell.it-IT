---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa75146ef26fc19108b918211a83289f73bfe4cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509783"
---
# <span data-ttu-id="7b6e7-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b6e7-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7b6e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b6e7-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6e7-103">Rimuove una regola di sicurezza di rete da un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b6e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b6e7-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b6e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b6e7-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6e7-106">Il cmdlet **Remove-AzureRmNetworkSecurityRuleConfig** rimuove una configurazione della regola di sicurezza di rete da un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="7b6e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b6e7-107">EXAMPLES</span></span>

### <span data-ttu-id="7b6e7-108">Esempio 1: rimuovere una configurazione della regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="7b6e7-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="7b6e7-109">Il primo comando crea una configurazione della regola di sicurezza di rete denominata RDP-Rule e quindi la archivia nella variabile $rule 1.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="7b6e7-110">Il secondo comando crea un gruppo di sicurezza di rete usando la regola in $rule 1 e quindi archivia il gruppo di sicurezza della rete nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="7b6e7-111">Il terzo comando rimuove la configurazione della regola di sicurezza di rete denominata RDP-Rule dal gruppo di sicurezza della rete in $nsg.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="7b6e7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b6e7-112">PARAMETERS</span></span>

### <span data-ttu-id="7b6e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6e7-113">-DefaultProfile</span></span>
<span data-ttu-id="7b6e7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b6e7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b6e7-115">-Name</span></span>
<span data-ttu-id="7b6e7-116">Specifica il nome della configurazione della regola di sicurezza della rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b6e7-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7b6e7-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7b6e7-118">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="7b6e7-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="7b6e7-119">Questo oggetto contiene la configurazione della regola di sicurezza della rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b6e7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6e7-120">CommonParameters</span></span>
<span data-ttu-id="7b6e7-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b6e7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6e7-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b6e7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6e7-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b6e7-123">INPUTS</span></span>

### <span data-ttu-id="7b6e7-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7b6e7-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="7b6e7-125">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7b6e7-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="7b6e7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b6e7-126">OUTPUTS</span></span>

### <span data-ttu-id="7b6e7-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7b6e7-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7b6e7-128">Note</span><span class="sxs-lookup"><span data-stu-id="7b6e7-128">NOTES</span></span>

## <span data-ttu-id="7b6e7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b6e7-129">RELATED LINKS</span></span>

[<span data-ttu-id="7b6e7-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b6e7-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7b6e7-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b6e7-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7b6e7-132">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7b6e7-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="7b6e7-133">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b6e7-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7b6e7-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7b6e7-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


