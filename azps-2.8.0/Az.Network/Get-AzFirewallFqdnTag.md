---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853737"
---
# <span data-ttu-id="b0aaf-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="b0aaf-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="b0aaf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="b0aaf-103">Ottiene i tag FQDN di Azure firewall disponibili.</span><span class="sxs-lookup"><span data-stu-id="b0aaf-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="b0aaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0aaf-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0aaf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0aaf-105">DESCRIPTION</span></span>
<span data-ttu-id="b0aaf-106">Il cmdlet **Get-AzFirewallFqdnTag** Ottiene l'elenco dei tag FQDN che possono essere usati per le regole delle applicazioni di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="b0aaf-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="b0aaf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0aaf-107">EXAMPLES</span></span>

### <span data-ttu-id="b0aaf-108">1: recuperare tutti i tag FQDN disponibili</span><span class="sxs-lookup"><span data-stu-id="b0aaf-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="b0aaf-109">Questo esempio recupera tutti i tag FQDN disponibili.</span><span class="sxs-lookup"><span data-stu-id="b0aaf-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="b0aaf-110">2: usare il primo tag FQDN disponibile in una regola dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b0aaf-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="b0aaf-111">Questo esempio crea una regola di applicazione firewall usando il primo tag FQDN disponibile</span><span class="sxs-lookup"><span data-stu-id="b0aaf-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="b0aaf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0aaf-112">PARAMETERS</span></span>

### <span data-ttu-id="b0aaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0aaf-113">-DefaultProfile</span></span>
<span data-ttu-id="b0aaf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0aaf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0aaf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0aaf-115">CommonParameters</span></span>
<span data-ttu-id="b0aaf-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0aaf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0aaf-117">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0aaf-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0aaf-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0aaf-118">INPUTS</span></span>

### <span data-ttu-id="b0aaf-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b0aaf-119">None</span></span>

## <span data-ttu-id="b0aaf-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0aaf-120">OUTPUTS</span></span>

### <span data-ttu-id="b0aaf-121">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="b0aaf-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="b0aaf-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b0aaf-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b0aaf-123">Note</span><span class="sxs-lookup"><span data-stu-id="b0aaf-123">NOTES</span></span>

## <span data-ttu-id="b0aaf-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0aaf-124">RELATED LINKS</span></span>

[<span data-ttu-id="b0aaf-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b0aaf-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="b0aaf-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b0aaf-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
