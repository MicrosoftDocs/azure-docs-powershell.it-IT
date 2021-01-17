---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476531"
---
# <span data-ttu-id="48a16-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="48a16-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="48a16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48a16-102">SYNOPSIS</span></span>
<span data-ttu-id="48a16-103">Creare una nuova whitelist di Threat Intelligence per Azure firewall</span><span class="sxs-lookup"><span data-stu-id="48a16-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="48a16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48a16-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48a16-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48a16-105">DESCRIPTION</span></span>
<span data-ttu-id="48a16-106">Il cmdlet **New-AzFirewallThreatIntelWhitelist** crea un oggetto di tipo whitelist di Intel, che può essere usato per la creazione o l'impostazione di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="48a16-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="48a16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48a16-107">EXAMPLES</span></span>

### <span data-ttu-id="48a16-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="48a16-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="48a16-109">In questo esempio viene creato un elenco di informazioni di base su un elenco di indirizzi di una whitelist contenente un elenco FQDN di due voci e un indirizzo IP whitelist</span><span class="sxs-lookup"><span data-stu-id="48a16-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="48a16-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48a16-110">PARAMETERS</span></span>

### <span data-ttu-id="48a16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a16-111">-DefaultProfile</span></span>
<span data-ttu-id="48a16-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48a16-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48a16-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="48a16-113">-FQDN</span></span>
<span data-ttu-id="48a16-114">Nomi di dominio completi della minaccia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="48a16-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="48a16-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="48a16-115">-IpAddress</span></span>
<span data-ttu-id="48a16-116">Gli indirizzi IP della minaccia di Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="48a16-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="48a16-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a16-117">CommonParameters</span></span>
<span data-ttu-id="48a16-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48a16-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a16-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48a16-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a16-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48a16-120">INPUTS</span></span>

### <span data-ttu-id="48a16-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="48a16-121">None</span></span>

## <span data-ttu-id="48a16-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48a16-122">OUTPUTS</span></span>

### <span data-ttu-id="48a16-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="48a16-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="48a16-124">Note</span><span class="sxs-lookup"><span data-stu-id="48a16-124">NOTES</span></span>

## <span data-ttu-id="48a16-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48a16-125">RELATED LINKS</span></span>

[<span data-ttu-id="48a16-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48a16-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="48a16-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48a16-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="48a16-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48a16-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)