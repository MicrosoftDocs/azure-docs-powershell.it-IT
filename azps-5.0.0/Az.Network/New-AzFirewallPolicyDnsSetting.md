---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203125"
---
# <span data-ttu-id="404f2-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="404f2-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="404f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="404f2-102">SYNOPSIS</span></span>
<span data-ttu-id="404f2-103">Crea una nuova impostazione DNS per i criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="404f2-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="404f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="404f2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="404f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="404f2-105">DESCRIPTION</span></span>
<span data-ttu-id="404f2-106">Il cmdlet **New-AzFirewallPolicyDnsSetting** crea un oggetto Setting DNS per i criteri di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="404f2-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="404f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="404f2-107">EXAMPLES</span></span>

### <span data-ttu-id="404f2-108">1. creare un criterio vuoto</span><span class="sxs-lookup"><span data-stu-id="404f2-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="404f2-109">Questo esempio crea un oggetto Setting DNS con l'impostazione dell'abilitazione del proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="404f2-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="404f2-110">2. creare un criterio vuoto con la modalità ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="404f2-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="404f2-111">Questo esempio crea un oggetto Setting DNS con l'impostazione dell'abilitazione del proxy DNS e l'impostazione di server DNS personalizzati.</span><span class="sxs-lookup"><span data-stu-id="404f2-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="404f2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="404f2-112">PARAMETERS</span></span>

### <span data-ttu-id="404f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404f2-113">-DefaultProfile</span></span>
<span data-ttu-id="404f2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="404f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="404f2-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="404f2-115">-EnableProxy</span></span>
<span data-ttu-id="404f2-116">Abilita proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="404f2-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="404f2-117">Per impostazione predefinita, è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="404f2-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="404f2-118">-Server</span><span class="sxs-lookup"><span data-stu-id="404f2-118">-Server</span></span>
<span data-ttu-id="404f2-119">Elenco dei server DNS</span><span class="sxs-lookup"><span data-stu-id="404f2-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="404f2-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="404f2-120">-Confirm</span></span>
<span data-ttu-id="404f2-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="404f2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404f2-122">-WhatIf</span></span>
<span data-ttu-id="404f2-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="404f2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="404f2-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="404f2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="404f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404f2-125">CommonParameters</span></span>
<span data-ttu-id="404f2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404f2-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="404f2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404f2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="404f2-128">INPUTS</span></span>

### <span data-ttu-id="404f2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="404f2-129">None</span></span>

## <span data-ttu-id="404f2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="404f2-130">OUTPUTS</span></span>

### <span data-ttu-id="404f2-131">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="404f2-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="404f2-132">Note</span><span class="sxs-lookup"><span data-stu-id="404f2-132">NOTES</span></span>

## <span data-ttu-id="404f2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="404f2-133">RELATED LINKS</span></span>
