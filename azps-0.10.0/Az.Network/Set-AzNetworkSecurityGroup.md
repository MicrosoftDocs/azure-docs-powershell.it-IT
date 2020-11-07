---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862766"
---
# <span data-ttu-id="e2a86-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2a86-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="e2a86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2a86-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a86-103">Imposta lo stato obiettivo per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="e2a86-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="e2a86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2a86-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2a86-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2a86-105">DESCRIPTION</span></span>
<span data-ttu-id="e2a86-106">Il cmdlet **set-AzNetworkSecurityGroup** imposta lo stato obiettivo per un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a86-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="e2a86-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2a86-107">EXAMPLES</span></span>

### <span data-ttu-id="e2a86-108">Esempio 1: impostare lo stato di un obiettivo per un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="e2a86-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="e2a86-109">Questo comando ottiene il gruppo di sicurezza di rete di Azure denominato Nsg1 e aggiunge una regola di sicurezza di rete denominata Rdp-Rule per consentire il traffico Internet sulla porta 3389 per l'oggetto del gruppo di sicurezza di rete recuperato tramite Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="e2a86-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="e2a86-110">Il comando mantiene il gruppo di sicurezza di rete di Azure modificato usando **set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="e2a86-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="e2a86-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2a86-111">PARAMETERS</span></span>

### <span data-ttu-id="e2a86-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2a86-112">-AsJob</span></span>
<span data-ttu-id="e2a86-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e2a86-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a86-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a86-114">-DefaultProfile</span></span>
<span data-ttu-id="e2a86-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e2a86-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2a86-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2a86-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e2a86-117">Un oggetto gruppo di sicurezza di rete che rappresenta lo stato dell'obiettivo a cui il cmdlet imposta il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="e2a86-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="e2a86-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a86-118">CommonParameters</span></span>
<span data-ttu-id="e2a86-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a86-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a86-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a86-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a86-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2a86-121">INPUTS</span></span>

### <span data-ttu-id="e2a86-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2a86-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="e2a86-123">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e2a86-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="e2a86-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2a86-124">OUTPUTS</span></span>

### <span data-ttu-id="e2a86-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2a86-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e2a86-126">Note</span><span class="sxs-lookup"><span data-stu-id="e2a86-126">NOTES</span></span>

## <span data-ttu-id="e2a86-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2a86-127">RELATED LINKS</span></span>

[<span data-ttu-id="e2a86-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2a86-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e2a86-129">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2a86-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="e2a86-130">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2a86-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


