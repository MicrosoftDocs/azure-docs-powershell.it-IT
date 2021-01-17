---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486759"
---
# <span data-ttu-id="5fec4-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5fec4-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="5fec4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fec4-102">SYNOPSIS</span></span>
<span data-ttu-id="5fec4-103">Ottiene un criterio di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="5fec4-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="5fec4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fec4-104">SYNTAX</span></span>

### <span data-ttu-id="5fec4-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5fec4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fec4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fec4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fec4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fec4-107">DESCRIPTION</span></span>
<span data-ttu-id="5fec4-108">Il cmdlet **Get-AzFirewallPolicy** ottiene uno o più firewall in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5fec4-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="5fec4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fec4-109">EXAMPLES</span></span>

### <span data-ttu-id="5fec4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5fec4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="5fec4-111">Questo esempio ottiene un criterio firewall denominato "firewallPolicy" nel gruppo risorse "TestRg"</span><span class="sxs-lookup"><span data-stu-id="5fec4-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="5fec4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fec4-112">PARAMETERS</span></span>

### <span data-ttu-id="5fec4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fec4-113">-DefaultProfile</span></span>
<span data-ttu-id="5fec4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fec4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fec4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fec4-115">-Name</span></span>
<span data-ttu-id="5fec4-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5fec4-116">The resource name.</span></span>

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

### <span data-ttu-id="5fec4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fec4-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fec4-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5fec4-118">The resource group name.</span></span>

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

### <span data-ttu-id="5fec4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fec4-119">-ResourceId</span></span>
<span data-ttu-id="5fec4-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5fec4-120">The resource Id.</span></span>

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

### <span data-ttu-id="5fec4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fec4-121">CommonParameters</span></span>
<span data-ttu-id="5fec4-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fec4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fec4-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fec4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fec4-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fec4-124">INPUTS</span></span>

### <span data-ttu-id="5fec4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5fec4-125">System.String</span></span>

## <span data-ttu-id="5fec4-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fec4-126">OUTPUTS</span></span>

### <span data-ttu-id="5fec4-127">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="5fec4-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="5fec4-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 1.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5fec4-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5fec4-129">Note</span><span class="sxs-lookup"><span data-stu-id="5fec4-129">NOTES</span></span>

## <span data-ttu-id="5fec4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fec4-130">RELATED LINKS</span></span>
