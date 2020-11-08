---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021302"
---
# <span data-ttu-id="77a48-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="77a48-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="77a48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77a48-102">SYNOPSIS</span></span>
<span data-ttu-id="77a48-103">Ottiene un gruppo di insiemi di regole dei criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="77a48-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="77a48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77a48-104">SYNTAX</span></span>

### <span data-ttu-id="77a48-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="77a48-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77a48-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77a48-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77a48-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77a48-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77a48-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77a48-108">DESCRIPTION</span></span>
<span data-ttu-id="77a48-109">Il cmdlet **Get-AzFirewallPolicyRuleCollectionGroup** ottiene il RuleCollectionGroup menzionato da un criterio firewall</span><span class="sxs-lookup"><span data-stu-id="77a48-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="77a48-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77a48-110">EXAMPLES</span></span>

### <span data-ttu-id="77a48-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77a48-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="77a48-112">Questo esempio ottiene la regola collectionGroup nel criterio firewall $fp</span><span class="sxs-lookup"><span data-stu-id="77a48-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="77a48-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77a48-113">PARAMETERS</span></span>

### <span data-ttu-id="77a48-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="77a48-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="77a48-115">Criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="77a48-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a48-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="77a48-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="77a48-117">Nome criterio firewall</span><span class="sxs-lookup"><span data-stu-id="77a48-117">The Firewall policy name</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a48-118">-DefaultProfile</span></span>
<span data-ttu-id="77a48-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77a48-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a48-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="77a48-120">-Name</span></span>
<span data-ttu-id="77a48-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="77a48-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77a48-122">-ResourceGroupName</span></span>
<span data-ttu-id="77a48-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="77a48-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a48-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77a48-124">-ResourceId</span></span>
<span data-ttu-id="77a48-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="77a48-125">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a48-126">CommonParameters</span></span>
<span data-ttu-id="77a48-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77a48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a48-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77a48-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a48-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77a48-129">INPUTS</span></span>

### <span data-ttu-id="77a48-130">System. String</span><span class="sxs-lookup"><span data-stu-id="77a48-130">System.String</span></span>

### <span data-ttu-id="77a48-131">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="77a48-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="77a48-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77a48-132">OUTPUTS</span></span>

### <span data-ttu-id="77a48-133">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="77a48-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="77a48-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="77a48-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="77a48-135">Note</span><span class="sxs-lookup"><span data-stu-id="77a48-135">NOTES</span></span>

## <span data-ttu-id="77a48-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77a48-136">RELATED LINKS</span></span>
