---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 2e4179019f74a8fd85b5f0ea3471bc586864172a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192795"
---
# <span data-ttu-id="98c93-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="98c93-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="98c93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98c93-102">SYNOPSIS</span></span>
<span data-ttu-id="98c93-103">Crea una nuova impostazione DNS per i criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="98c93-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="98c93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98c93-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-ProxyNotRequiredForNetworkRule] [-Server <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c93-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98c93-105">DESCRIPTION</span></span>
<span data-ttu-id="98c93-106">Il cmdlet **New-AzFirewallPolicyDnsSetting** crea un oggetto Setting DNS per i criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="98c93-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="98c93-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98c93-107">EXAMPLES</span></span>

### <span data-ttu-id="98c93-108">1. creare un criterio vuoto</span><span class="sxs-lookup"><span data-stu-id="98c93-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="98c93-109">Questo esempio crea un oggetto Setting DNS con l'impostazione dell'abilitazione del proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="98c93-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="98c93-110">2. creare un criterio vuoto con la modalità ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="98c93-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```
<span data-ttu-id="98c93-111">Questo esempio crea un oggetto Setting DNS con l'impostazione dell'abilitazione del proxy DNS e l'impostazione di server DNS personalizzati.</span><span class="sxs-lookup"><span data-stu-id="98c93-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="98c93-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98c93-112">PARAMETERS</span></span>

### <span data-ttu-id="98c93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c93-113">-DefaultProfile</span></span>
<span data-ttu-id="98c93-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98c93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c93-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="98c93-115">-EnableProxy</span></span>
<span data-ttu-id="98c93-116">Abilita proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="98c93-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="98c93-117">Per impostazione predefinita, è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="98c93-117">By default it is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c93-118">-ProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="98c93-118">-ProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="98c93-119">Richiede la funzionalità proxy DNS per gli FQDN nelle regole di rete.</span><span class="sxs-lookup"><span data-stu-id="98c93-119">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>
<span data-ttu-id="98c93-120">Per impostazione predefinita, è vero.</span><span class="sxs-lookup"><span data-stu-id="98c93-120">By default it is true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c93-121">-Server</span><span class="sxs-lookup"><span data-stu-id="98c93-121">-Server</span></span>
<span data-ttu-id="98c93-122">Elenco dei server DNS</span><span class="sxs-lookup"><span data-stu-id="98c93-122">The list of DNS Servers</span></span>

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

### <span data-ttu-id="98c93-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98c93-123">-Confirm</span></span>
<span data-ttu-id="98c93-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c93-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c93-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c93-125">-WhatIf</span></span>
<span data-ttu-id="98c93-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98c93-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98c93-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98c93-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c93-128">CommonParameters</span></span>
<span data-ttu-id="98c93-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c93-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98c93-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c93-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98c93-131">INPUTS</span></span>

### <span data-ttu-id="98c93-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="98c93-132">None</span></span>

## <span data-ttu-id="98c93-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98c93-133">OUTPUTS</span></span>

### <span data-ttu-id="98c93-134">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="98c93-134">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="98c93-135">Note</span><span class="sxs-lookup"><span data-stu-id="98c93-135">NOTES</span></span>

## <span data-ttu-id="98c93-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98c93-136">RELATED LINKS</span></span>
