---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 348732794a0cf16233f9a139e86ed89658fc5ac2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866833"
---
# <span data-ttu-id="57f87-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57f87-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="57f87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57f87-102">SYNOPSIS</span></span>
<span data-ttu-id="57f87-103">Imposta lo stato obiettivo per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="57f87-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57f87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57f87-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57f87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57f87-105">DESCRIPTION</span></span>
<span data-ttu-id="57f87-106">Il cmdlet **set-AzureRmNetworkSecurityGroup** imposta lo stato obiettivo per un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="57f87-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="57f87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57f87-107">EXAMPLES</span></span>

### <span data-ttu-id="57f87-108">Esempio 1: impostare lo stato di un obiettivo per un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="57f87-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="57f87-109">Questo comando ottiene il gruppo di sicurezza di rete di Azure denominato Nsg1 e aggiunge una regola di sicurezza di rete denominata Rdp-Rule per consentire il traffico Internet sulla porta 3389 per l'oggetto del gruppo di sicurezza di rete recuperato tramite Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="57f87-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="57f87-110">Il comando mantiene il gruppo di sicurezza di rete di Azure modificato usando **set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="57f87-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="57f87-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57f87-111">PARAMETERS</span></span>

### <span data-ttu-id="57f87-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57f87-112">-AsJob</span></span>
<span data-ttu-id="57f87-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="57f87-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57f87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f87-114">-DefaultProfile</span></span>
<span data-ttu-id="57f87-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57f87-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57f87-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57f87-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="57f87-117">Un oggetto gruppo di sicurezza di rete che rappresenta lo stato dell'obiettivo a cui il cmdlet imposta il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="57f87-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="57f87-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f87-118">CommonParameters</span></span>
<span data-ttu-id="57f87-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57f87-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f87-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f87-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f87-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57f87-121">INPUTS</span></span>

### <span data-ttu-id="57f87-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57f87-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="57f87-123">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="57f87-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="57f87-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57f87-124">OUTPUTS</span></span>

### <span data-ttu-id="57f87-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57f87-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="57f87-126">Note</span><span class="sxs-lookup"><span data-stu-id="57f87-126">NOTES</span></span>

## <span data-ttu-id="57f87-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57f87-127">RELATED LINKS</span></span>

[<span data-ttu-id="57f87-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57f87-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="57f87-129">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57f87-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="57f87-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57f87-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


