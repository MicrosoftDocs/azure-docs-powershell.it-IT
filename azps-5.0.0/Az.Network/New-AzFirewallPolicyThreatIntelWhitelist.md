---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199868"
---
# <span data-ttu-id="b85e1-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="b85e1-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="b85e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b85e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b85e1-103">Creare una nuova whitelist di Threat Intelligence per i criteri di firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="b85e1-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="b85e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b85e1-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b85e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b85e1-105">DESCRIPTION</span></span>
<span data-ttu-id="b85e1-106">Il cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** crea un oggetto di tipo whitelist di Intel, che può essere usato per la creazione o l'impostazione di un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="b85e1-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="b85e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b85e1-107">EXAMPLES</span></span>

### <span data-ttu-id="b85e1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b85e1-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="b85e1-109">In questo esempio viene creato un elenco di informazioni di base di un elenco di un elenco di indirizzi IP di un elenco e un elenco di due voci</span><span class="sxs-lookup"><span data-stu-id="b85e1-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="b85e1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b85e1-110">PARAMETERS</span></span>

### <span data-ttu-id="b85e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85e1-111">-DefaultProfile</span></span>
<span data-ttu-id="b85e1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b85e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b85e1-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="b85e1-113">-FQDN</span></span>
<span data-ttu-id="b85e1-114">Nomi di dominio completi della minaccia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="b85e1-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="b85e1-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b85e1-115">-IpAddress</span></span>
<span data-ttu-id="b85e1-116">Gli indirizzi IP della minaccia di Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="b85e1-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="b85e1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85e1-117">CommonParameters</span></span>
<span data-ttu-id="b85e1-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85e1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85e1-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b85e1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85e1-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b85e1-120">INPUTS</span></span>

### <span data-ttu-id="b85e1-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b85e1-121">None</span></span>

## <span data-ttu-id="b85e1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b85e1-122">OUTPUTS</span></span>

### <span data-ttu-id="b85e1-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="b85e1-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="b85e1-124">Note</span><span class="sxs-lookup"><span data-stu-id="b85e1-124">NOTES</span></span>

## <span data-ttu-id="b85e1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b85e1-125">RELATED LINKS</span></span>