---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: eed81fbd222220225a67378c67aa1d32d440577a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960397"
---
# <span data-ttu-id="87a5f-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="87a5f-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="87a5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="87a5f-103">Creare un nuovo elenco degli elenchi dei criteri di Threat Intelligence per i criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="87a5f-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="87a5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87a5f-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87a5f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="87a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="87a5f-106">Il cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** crea un oggetto threat intel whitelist, che può essere usato per creare o impostare un criterio del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="87a5f-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="87a5f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87a5f-107">EXAMPLES</span></span>

### <span data-ttu-id="87a5f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87a5f-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="87a5f-109">In questo esempio viene creata una lista bianca di informazioni sulle minacce che contiene un elenco di voci FQDN di una voce e un elenco indirizzi Ip di due voci</span><span class="sxs-lookup"><span data-stu-id="87a5f-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="87a5f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87a5f-110">PARAMETERS</span></span>

### <span data-ttu-id="87a5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a5f-111">-DefaultProfile</span></span>
<span data-ttu-id="87a5f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87a5f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a5f-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="87a5f-113">-FQDN</span></span>
<span data-ttu-id="87a5f-114">FQDN della threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="87a5f-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a5f-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="87a5f-115">-IpAddress</span></span>
<span data-ttu-id="87a5f-116">Indirizzi IP della minaccia Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="87a5f-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a5f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a5f-117">CommonParameters</span></span>
<span data-ttu-id="87a5f-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a5f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a5f-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87a5f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a5f-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="87a5f-120">INPUTS</span></span>

### <span data-ttu-id="87a5f-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="87a5f-121">None</span></span>

## <span data-ttu-id="87a5f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87a5f-122">OUTPUTS</span></span>

### <span data-ttu-id="87a5f-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="87a5f-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="87a5f-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="87a5f-124">NOTES</span></span>

## <span data-ttu-id="87a5f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87a5f-125">RELATED LINKS</span></span>
