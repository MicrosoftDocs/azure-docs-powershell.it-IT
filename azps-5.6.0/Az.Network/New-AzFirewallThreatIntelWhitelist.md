---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 18946b74ea72ac3d5db2dd683657eda60b8eeec5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964157"
---
# <span data-ttu-id="868f3-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="868f3-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="868f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="868f3-102">SYNOPSIS</span></span>
<span data-ttu-id="868f3-103">Creare una nuova lista bianca di Threat Intelligence per il Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="868f3-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="868f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="868f3-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="868f3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="868f3-105">DESCRIPTION</span></span>
<span data-ttu-id="868f3-106">Il cmdlet **New-AzFirewallThreatIntelWhitelist** crea un oggetto threat intel whitelist, che può essere usato quando si crea o si imposta un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="868f3-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="868f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="868f3-107">EXAMPLES</span></span>

### <span data-ttu-id="868f3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="868f3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="868f3-109">In questo esempio viene creata una lista bianca di informazioni sulle minacce che contiene un elenco di due voci FQDN e un elenco indirizzi Ip di due voci.</span><span class="sxs-lookup"><span data-stu-id="868f3-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="868f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="868f3-110">PARAMETERS</span></span>

### <span data-ttu-id="868f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868f3-111">-DefaultProfile</span></span>
<span data-ttu-id="868f3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="868f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="868f3-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="868f3-113">-FQDN</span></span>
<span data-ttu-id="868f3-114">FQDN della threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="868f3-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="868f3-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="868f3-115">-IpAddress</span></span>
<span data-ttu-id="868f3-116">Indirizzi IP della minaccia Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="868f3-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="868f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868f3-117">CommonParameters</span></span>
<span data-ttu-id="868f3-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="868f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868f3-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="868f3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868f3-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="868f3-120">INPUTS</span></span>

### <span data-ttu-id="868f3-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="868f3-121">None</span></span>

## <span data-ttu-id="868f3-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="868f3-122">OUTPUTS</span></span>

### <span data-ttu-id="868f3-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="868f3-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="868f3-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="868f3-124">NOTES</span></span>

## <span data-ttu-id="868f3-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="868f3-125">RELATED LINKS</span></span>

[<span data-ttu-id="868f3-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="868f3-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="868f3-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="868f3-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="868f3-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="868f3-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)