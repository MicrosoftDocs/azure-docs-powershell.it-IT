---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688080"
---
# <span data-ttu-id="af332-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="af332-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="af332-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af332-102">SYNOPSIS</span></span>
<span data-ttu-id="af332-103">Ottiene i tag FQDN di Azure firewall disponibili.</span><span class="sxs-lookup"><span data-stu-id="af332-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af332-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af332-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af332-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af332-105">DESCRIPTION</span></span>
<span data-ttu-id="af332-106">Il cmdlet **Get-AzureRmFirewallFqdnTag** Ottiene l'elenco dei tag FQDN che possono essere usati per le regole delle applicazioni di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="af332-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="af332-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af332-107">EXAMPLES</span></span>

### <span data-ttu-id="af332-108">1: recuperare tutti i tag FQDN disponibili</span><span class="sxs-lookup"><span data-stu-id="af332-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="af332-109">Questo esempio recupera tutti i tag FQDN disponibili.</span><span class="sxs-lookup"><span data-stu-id="af332-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="af332-110">2: usare il primo tag FQDN disponibile in una regola dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="af332-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="af332-111">Questo esempio crea una regola di applicazione firewall usando il primo tag FQDN disponibile</span><span class="sxs-lookup"><span data-stu-id="af332-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="af332-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af332-112">PARAMETERS</span></span>

### <span data-ttu-id="af332-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af332-113">-DefaultProfile</span></span>
<span data-ttu-id="af332-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af332-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af332-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af332-115">CommonParameters</span></span>
<span data-ttu-id="af332-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af332-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af332-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af332-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af332-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af332-118">INPUTS</span></span>

### <span data-ttu-id="af332-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="af332-119">None</span></span>
<span data-ttu-id="af332-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="af332-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af332-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af332-121">OUTPUTS</span></span>

### <span data-ttu-id="af332-122">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="af332-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="af332-123">Note</span><span class="sxs-lookup"><span data-stu-id="af332-123">NOTES</span></span>

## <span data-ttu-id="af332-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af332-124">RELATED LINKS</span></span>

[<span data-ttu-id="af332-125">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="af332-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="af332-126">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="af332-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
