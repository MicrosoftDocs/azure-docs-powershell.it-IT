---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206939"
---
# <span data-ttu-id="a4361-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a4361-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="a4361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4361-102">SYNOPSIS</span></span>
<span data-ttu-id="a4361-103">Ottenere una configurazione delle regole di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="a4361-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="a4361-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4361-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4361-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4361-105">DESCRIPTION</span></span>
<span data-ttu-id="a4361-106">Il **cmdlet Get-AzNetworkSecurityRuleConfig ottiene** una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4361-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="a4361-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4361-107">EXAMPLES</span></span>

### <span data-ttu-id="a4361-108">1: Recupero di una configurazione di una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="a4361-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="a4361-109">Questo comando recupera la regola predefinita denominata "AllowInternetOutBound" dal gruppo di sicurezza di rete Azure denominato "nsg1" nel gruppo di risorse "rg1"</span><span class="sxs-lookup"><span data-stu-id="a4361-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="a4361-110">2: Recuperare la configurazione di una regola di sicurezza di rete usando solo il nome</span><span class="sxs-lookup"><span data-stu-id="a4361-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="a4361-111">Questo comando recupera la regola definita dall'utente denominata "rdp-rule" dal gruppo di sicurezza di rete Azure denominato "nsg1" nel gruppo di risorse "rg1"</span><span class="sxs-lookup"><span data-stu-id="a4361-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="a4361-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4361-112">PARAMETERS</span></span>

### <span data-ttu-id="a4361-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4361-113">-DefaultProfile</span></span>
<span data-ttu-id="a4361-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4361-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4361-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="a4361-115">-DefaultRules</span></span>
<span data-ttu-id="a4361-116">Indica se questo cmdlet ottiene una configurazione di regola creata dall'utente o una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4361-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="a4361-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a4361-117">-Name</span></span>
<span data-ttu-id="a4361-118">Specifica il nome della configurazione della regola di sicurezza di rete da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a4361-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="a4361-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a4361-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a4361-120">Specifica un oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza di rete da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a4361-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="a4361-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4361-121">CommonParameters</span></span>
<span data-ttu-id="a4361-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4361-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4361-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4361-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4361-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4361-124">INPUTS</span></span>

### <span data-ttu-id="a4361-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a4361-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a4361-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4361-126">OUTPUTS</span></span>

### <span data-ttu-id="a4361-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a4361-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="a4361-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4361-128">NOTES</span></span>

## <span data-ttu-id="a4361-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4361-129">RELATED LINKS</span></span>

[<span data-ttu-id="a4361-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a4361-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a4361-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a4361-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a4361-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a4361-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a4361-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a4361-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


