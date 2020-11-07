---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: a4d8386cdcdee8b67bea746e40a9035acf3bcce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688554"
---
# <span data-ttu-id="7d37a-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d37a-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7d37a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d37a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d37a-103">Ottenere una configurazione della regola di sicurezza della rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="7d37a-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d37a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d37a-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d37a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d37a-105">DESCRIPTION</span></span>
<span data-ttu-id="7d37a-106">Il cmdlet **Get-AzureRmNetworkSecurityRuleConfig** ottiene una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d37a-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="7d37a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d37a-107">EXAMPLES</span></span>

### <span data-ttu-id="7d37a-108">1: recupero della configurazione di una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="7d37a-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="7d37a-109">Questo comando Recupera la regola predefinita denominata "AllowInternetOutBound" dal gruppo di sicurezza di rete di Azure denominato "nsg1" nel gruppo di risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="7d37a-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="7d37a-110">2: recupero di una configurazione della regola di sicurezza di rete usando solo il nome</span><span class="sxs-lookup"><span data-stu-id="7d37a-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="7d37a-111">Questo comando Recupera la regola definita dall'utente denominata "RDP-Rule" di Azure Network Security Group denominata "nsg1" nel gruppo di risorse "RG1"</span><span class="sxs-lookup"><span data-stu-id="7d37a-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="7d37a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d37a-112">PARAMETERS</span></span>

### <span data-ttu-id="7d37a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d37a-113">-DefaultProfile</span></span>
<span data-ttu-id="7d37a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d37a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d37a-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="7d37a-115">-DefaultRules</span></span>
<span data-ttu-id="7d37a-116">Indica se questo cmdlet ottiene una configurazione di regola creata dall'utente o una configurazione di regola predefinita.</span><span class="sxs-lookup"><span data-stu-id="7d37a-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="7d37a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d37a-117">-Name</span></span>
<span data-ttu-id="7d37a-118">Specifica il nome della configurazione della regola di sicurezza della rete da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7d37a-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="7d37a-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d37a-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7d37a-120">Specifica un oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7d37a-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="7d37a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d37a-121">CommonParameters</span></span>
<span data-ttu-id="7d37a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d37a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d37a-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d37a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d37a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d37a-124">INPUTS</span></span>

### <span data-ttu-id="7d37a-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d37a-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="7d37a-126">Parametri: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d37a-126">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="7d37a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d37a-127">OUTPUTS</span></span>

### <span data-ttu-id="7d37a-128">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="7d37a-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="7d37a-129">Note</span><span class="sxs-lookup"><span data-stu-id="7d37a-129">NOTES</span></span>

## <span data-ttu-id="7d37a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d37a-130">RELATED LINKS</span></span>

[<span data-ttu-id="7d37a-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d37a-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7d37a-132">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d37a-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7d37a-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d37a-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7d37a-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d37a-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


