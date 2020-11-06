---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513215"
---
# <span data-ttu-id="be183-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="be183-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="be183-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be183-102">SYNOPSIS</span></span>
<span data-ttu-id="be183-103">Imposta lo stato obiettivo per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="be183-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be183-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be183-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be183-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be183-105">DESCRIPTION</span></span>
<span data-ttu-id="be183-106">Il cmdlet **set-AzureRmNetworkSecurityGroup** imposta lo stato obiettivo per un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="be183-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="be183-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be183-107">EXAMPLES</span></span>

### <span data-ttu-id="be183-108">Esempio 1: impostare lo stato di un obiettivo per un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="be183-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="be183-109">Questo comando ottiene il gruppo di sicurezza di rete di Azure denominato Nsg1 e aggiunge una regola di sicurezza di rete denominata Rdp-Rule per consentire il traffico Internet sulla porta 3389 per l'oggetto del gruppo di sicurezza di rete recuperato tramite Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="be183-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="be183-110">Il comando mantiene il gruppo di sicurezza di rete di Azure modificato usando **set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="be183-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="be183-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be183-111">PARAMETERS</span></span>

### <span data-ttu-id="be183-112">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="be183-112">-NetworkSecurityGroup</span></span>
<span data-ttu-id="be183-113">Un oggetto gruppo di sicurezza di rete che rappresenta lo stato dell'obiettivo a cui il cmdlet imposta il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="be183-113">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="be183-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be183-114">-DefaultProfile</span></span>
<span data-ttu-id="be183-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be183-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be183-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be183-116">CommonParameters</span></span>
<span data-ttu-id="be183-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be183-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be183-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be183-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be183-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be183-119">INPUTS</span></span>

### <span data-ttu-id="be183-120">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="be183-120">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="be183-121">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="be183-121">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="be183-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be183-122">OUTPUTS</span></span>

### <span data-ttu-id="be183-123">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="be183-123">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="be183-124">Note</span><span class="sxs-lookup"><span data-stu-id="be183-124">NOTES</span></span>

## <span data-ttu-id="be183-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be183-125">RELATED LINKS</span></span>

[<span data-ttu-id="be183-126">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="be183-126">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="be183-127">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="be183-127">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="be183-128">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="be183-128">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


