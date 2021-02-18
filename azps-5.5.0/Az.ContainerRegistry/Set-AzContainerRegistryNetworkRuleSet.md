---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181454"
---
# <span data-ttu-id="6e7a0-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e7a0-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="6e7a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e7a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e7a0-103">Creare o aggiornare un set di regole di rete.</span><span class="sxs-lookup"><span data-stu-id="6e7a0-103">Create or update a network rule set.</span></span> <span data-ttu-id="6e7a0-104">Il set di regole può essere applicato solo al Registro di sistema "Premium".</span><span class="sxs-lookup"><span data-stu-id="6e7a0-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="6e7a0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e7a0-105">SYNTAX</span></span>

### <span data-ttu-id="6e7a0-106">AddAddNetworkRuleWithoutInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e7a0-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e7a0-107">AddNetworkRuleWithObjectObject</span><span class="sxs-lookup"><span data-stu-id="6e7a0-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e7a0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e7a0-108">DESCRIPTION</span></span>
<span data-ttu-id="6e7a0-109">Creare o aggiornare un set di regole di rete</span><span class="sxs-lookup"><span data-stu-id="6e7a0-109">Create or update a network rule set</span></span>

## <span data-ttu-id="6e7a0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e7a0-110">EXAMPLES</span></span>

### <span data-ttu-id="6e7a0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6e7a0-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="6e7a0-112">Creare un nuovo set di regole di rete.</span><span class="sxs-lookup"><span data-stu-id="6e7a0-112">Create a new network rule set.</span></span>

## <span data-ttu-id="6e7a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e7a0-113">PARAMETERS</span></span>

### <span data-ttu-id="6e7a0-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="6e7a0-114">-DefaultAction</span></span>
<span data-ttu-id="6e7a0-115">L'azione predefinita può essere "Consenti" o "Nega"</span><span class="sxs-lookup"><span data-stu-id="6e7a0-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e7a0-116">-DefaultProfile</span></span>
<span data-ttu-id="6e7a0-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e7a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e7a0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e7a0-118">-InputObject</span></span>
<span data-ttu-id="6e7a0-119">Input PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e7a0-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7a0-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="6e7a0-120">-NetworkRule</span></span>
<span data-ttu-id="6e7a0-121">Elenco delle regole di rete</span><span class="sxs-lookup"><span data-stu-id="6e7a0-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e7a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e7a0-122">CommonParameters</span></span>
<span data-ttu-id="6e7a0-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e7a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e7a0-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e7a0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e7a0-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e7a0-125">INPUTS</span></span>

### <span data-ttu-id="6e7a0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6e7a0-126">System.String</span></span>

### <span data-ttu-id="6e7a0-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6e7a0-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="6e7a0-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e7a0-128">OUTPUTS</span></span>

### <span data-ttu-id="6e7a0-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6e7a0-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="6e7a0-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e7a0-130">NOTES</span></span>

## <span data-ttu-id="6e7a0-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e7a0-131">RELATED LINKS</span></span>
