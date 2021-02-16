---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193870"
---
# <span data-ttu-id="94f72-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="94f72-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="94f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f72-102">SYNOPSIS</span></span>
<span data-ttu-id="94f72-103">Recupera i tag FQDN del firewall di Azure disponibili.</span><span class="sxs-lookup"><span data-stu-id="94f72-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="94f72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94f72-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f72-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94f72-105">DESCRIPTION</span></span>
<span data-ttu-id="94f72-106">Il cmdlet **Get-AzFirewallFqdnTag** ottiene l'elenco dei tag FQDN che possono essere usati per le regole delle applicazioni del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="94f72-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="94f72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94f72-107">EXAMPLES</span></span>

### <span data-ttu-id="94f72-108">1: Recuperare tutti i tag FQDN disponibili</span><span class="sxs-lookup"><span data-stu-id="94f72-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="94f72-109">Questo esempio recupera tutti i tag FQDN disponibili.</span><span class="sxs-lookup"><span data-stu-id="94f72-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="94f72-110">2: Usare il primo tag FQDN disponibile in una regola di applicazione</span><span class="sxs-lookup"><span data-stu-id="94f72-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="94f72-111">Questo esempio crea una regola dell'applicazione del firewall usando il primo tag FQDN disponibile</span><span class="sxs-lookup"><span data-stu-id="94f72-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="94f72-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94f72-112">PARAMETERS</span></span>

### <span data-ttu-id="94f72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f72-113">-DefaultProfile</span></span>
<span data-ttu-id="94f72-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94f72-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f72-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f72-115">CommonParameters</span></span>
<span data-ttu-id="94f72-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f72-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f72-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94f72-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f72-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="94f72-118">INPUTS</span></span>

### <span data-ttu-id="94f72-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94f72-119">None</span></span>

## <span data-ttu-id="94f72-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94f72-120">OUTPUTS</span></span>

### <span data-ttu-id="94f72-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="94f72-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="94f72-122">System.Collections.generic.IMur'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="94f72-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="94f72-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="94f72-123">NOTES</span></span>

## <span data-ttu-id="94f72-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94f72-124">RELATED LINKS</span></span>

[<span data-ttu-id="94f72-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="94f72-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="94f72-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="94f72-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
