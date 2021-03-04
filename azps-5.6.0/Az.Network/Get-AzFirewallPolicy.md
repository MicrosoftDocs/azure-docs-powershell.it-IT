---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: 056a70f6c085f3c0a936f9e144708c7258a3d5c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956926"
---
# <span data-ttu-id="18528-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="18528-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="18528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18528-102">SYNOPSIS</span></span>
<span data-ttu-id="18528-103">Ottiene un criterio firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="18528-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="18528-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18528-104">SYNTAX</span></span>

### <span data-ttu-id="18528-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18528-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18528-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18528-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18528-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18528-107">DESCRIPTION</span></span>
<span data-ttu-id="18528-108">Il cmdlet **Get-AzFirewallPolicy** ottiene uno o più firewall in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="18528-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="18528-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18528-109">EXAMPLES</span></span>

### <span data-ttu-id="18528-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18528-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="18528-111">Questo esempio ottiene un criterio del firewall denominato "firewallPolicy" nel gruppo di risorse "TestRg"</span><span class="sxs-lookup"><span data-stu-id="18528-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="18528-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18528-112">PARAMETERS</span></span>

### <span data-ttu-id="18528-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18528-113">-DefaultProfile</span></span>
<span data-ttu-id="18528-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18528-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18528-115">-Name</span><span class="sxs-lookup"><span data-stu-id="18528-115">-Name</span></span>
<span data-ttu-id="18528-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="18528-116">The resource name.</span></span>

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

### <span data-ttu-id="18528-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18528-117">-ResourceGroupName</span></span>
<span data-ttu-id="18528-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="18528-118">The resource group name.</span></span>

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

### <span data-ttu-id="18528-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18528-119">-ResourceId</span></span>
<span data-ttu-id="18528-120">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="18528-120">The resource Id.</span></span>

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

### <span data-ttu-id="18528-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18528-121">CommonParameters</span></span>
<span data-ttu-id="18528-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18528-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18528-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18528-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18528-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="18528-124">INPUTS</span></span>

### <span data-ttu-id="18528-125">System.String</span><span class="sxs-lookup"><span data-stu-id="18528-125">System.String</span></span>

## <span data-ttu-id="18528-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18528-126">OUTPUTS</span></span>

### <span data-ttu-id="18528-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="18528-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="18528-128">System.Collections.generic.IMur'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="18528-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="18528-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="18528-129">NOTES</span></span>

## <span data-ttu-id="18528-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18528-130">RELATED LINKS</span></span>
