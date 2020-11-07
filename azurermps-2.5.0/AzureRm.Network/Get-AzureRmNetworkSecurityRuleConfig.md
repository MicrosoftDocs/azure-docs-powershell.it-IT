---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 55f2ad108b6392a2f17c7b1539c5ebe7cccc3c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867036"
---
# <span data-ttu-id="c17a3-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c17a3-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c17a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c17a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c17a3-103">Ottenere una configurazione della regola di sicurezza della rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="c17a3-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c17a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c17a3-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c17a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c17a3-105">DESCRIPTION</span></span>
<span data-ttu-id="c17a3-106">Il cmdlet **Get-AzureRmNetworkSecurityRuleConfig** ottiene una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="c17a3-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="c17a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c17a3-107">EXAMPLES</span></span>

### <span data-ttu-id="c17a3-108">1: recupero della configurazione di una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="c17a3-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="c17a3-109">Questo comando Recupera la regola predefinita denominata "AllowInternetOutBound" dal gruppo di sicurezza di rete di Azure denominato "nsg1" nel gruppo di risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="c17a3-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="c17a3-110">2: recupero di una configurazione della regola di sicurezza di rete usando solo il nome</span><span class="sxs-lookup"><span data-stu-id="c17a3-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="c17a3-111">Questo comando Recupera la regola definita dall'utente denominata "RDP-Rule" di Azure Network Security Group denominata "nsg1" nel gruppo di risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="c17a3-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="c17a3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c17a3-112">PARAMETERS</span></span>

### <span data-ttu-id="c17a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17a3-113">-DefaultProfile</span></span>
<span data-ttu-id="c17a3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c17a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c17a3-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="c17a3-115">-DefaultRules</span></span>
<span data-ttu-id="c17a3-116">Indica se questo cmdlet ottiene una configurazione di regola creata dall'utente o una configurazione di regola predefinita.</span><span class="sxs-lookup"><span data-stu-id="c17a3-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="c17a3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c17a3-117">-Name</span></span>
<span data-ttu-id="c17a3-118">Specifica il nome della configurazione della regola di sicurezza della rete da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c17a3-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="c17a3-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c17a3-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c17a3-120">Specifica un oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c17a3-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="c17a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17a3-121">CommonParameters</span></span>
<span data-ttu-id="c17a3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c17a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17a3-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c17a3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17a3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c17a3-124">INPUTS</span></span>

### <span data-ttu-id="c17a3-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c17a3-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="c17a3-126">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c17a3-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="c17a3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c17a3-127">OUTPUTS</span></span>

### <span data-ttu-id="c17a3-128">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="c17a3-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="c17a3-129">Note</span><span class="sxs-lookup"><span data-stu-id="c17a3-129">NOTES</span></span>

## <span data-ttu-id="c17a3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c17a3-130">RELATED LINKS</span></span>

[<span data-ttu-id="c17a3-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c17a3-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c17a3-132">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c17a3-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c17a3-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c17a3-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c17a3-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c17a3-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


