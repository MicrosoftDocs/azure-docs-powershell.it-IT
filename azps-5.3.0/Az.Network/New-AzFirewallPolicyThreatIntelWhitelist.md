---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475906"
---
# <span data-ttu-id="907d8-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="907d8-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="907d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="907d8-102">SYNOPSIS</span></span>
<span data-ttu-id="907d8-103">Creare una nuova whitelist di Threat Intelligence per i criteri di firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="907d8-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="907d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="907d8-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="907d8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="907d8-105">DESCRIPTION</span></span>
<span data-ttu-id="907d8-106">Il cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** crea un oggetto di tipo whitelist di Intel, che può essere usato per la creazione o l'impostazione di un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="907d8-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="907d8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="907d8-107">EXAMPLES</span></span>

### <span data-ttu-id="907d8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="907d8-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="907d8-109">In questo esempio viene creato un elenco di informazioni di base di un elenco di un elenco di indirizzi IP di un elenco e un elenco di due voci</span><span class="sxs-lookup"><span data-stu-id="907d8-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="907d8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="907d8-110">PARAMETERS</span></span>

### <span data-ttu-id="907d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907d8-111">-DefaultProfile</span></span>
<span data-ttu-id="907d8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="907d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="907d8-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="907d8-113">-FQDN</span></span>
<span data-ttu-id="907d8-114">Nomi di dominio completi della minaccia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="907d8-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="907d8-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="907d8-115">-IpAddress</span></span>
<span data-ttu-id="907d8-116">Gli indirizzi IP della minaccia di Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="907d8-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="907d8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907d8-117">CommonParameters</span></span>
<span data-ttu-id="907d8-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907d8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907d8-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="907d8-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907d8-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="907d8-120">INPUTS</span></span>

### <span data-ttu-id="907d8-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="907d8-121">None</span></span>

## <span data-ttu-id="907d8-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="907d8-122">OUTPUTS</span></span>

### <span data-ttu-id="907d8-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="907d8-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="907d8-124">Note</span><span class="sxs-lookup"><span data-stu-id="907d8-124">NOTES</span></span>

## <span data-ttu-id="907d8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="907d8-125">RELATED LINKS</span></span>
