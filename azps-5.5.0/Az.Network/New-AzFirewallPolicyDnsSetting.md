---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187063"
---
# <span data-ttu-id="4ab06-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="4ab06-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="4ab06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ab06-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab06-103">Crea una nuova impostazione DNS per i criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab06-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="4ab06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ab06-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ab06-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ab06-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab06-106">Il cmdlet **New-AzFirewallPolicyDnsSetting crea** un oggetto impostazioni DNS per i criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="4ab06-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="4ab06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ab06-107">EXAMPLES</span></span>

### <span data-ttu-id="4ab06-108">1. Creare un criterio vuoto</span><span class="sxs-lookup"><span data-stu-id="4ab06-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="4ab06-109">Questo esempio crea un oggetto Dns Setting con l'impostazione dell'abilitazione del proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="4ab06-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="4ab06-110">2. Creare criteri vuoti con la modalità ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="4ab06-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="4ab06-111">In questo esempio viene creato un oggetto Dns Setting con l'impostazione dell'abilitazione del proxy DNS e l'impostazione di server DNS personalizzati.</span><span class="sxs-lookup"><span data-stu-id="4ab06-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="4ab06-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ab06-112">PARAMETERS</span></span>

### <span data-ttu-id="4ab06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab06-113">-DefaultProfile</span></span>
<span data-ttu-id="4ab06-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ab06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab06-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="4ab06-115">-EnableProxy</span></span>
<span data-ttu-id="4ab06-116">Abilitare il proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="4ab06-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="4ab06-117">Per impostazione predefinita, questa opzione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="4ab06-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="4ab06-118">-Server</span><span class="sxs-lookup"><span data-stu-id="4ab06-118">-Server</span></span>
<span data-ttu-id="4ab06-119">Elenco dei server DNS</span><span class="sxs-lookup"><span data-stu-id="4ab06-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="4ab06-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ab06-120">-Confirm</span></span>
<span data-ttu-id="4ab06-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ab06-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ab06-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab06-122">-WhatIf</span></span>
<span data-ttu-id="4ab06-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ab06-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ab06-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ab06-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ab06-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab06-125">CommonParameters</span></span>
<span data-ttu-id="4ab06-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab06-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab06-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ab06-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab06-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ab06-128">INPUTS</span></span>

### <span data-ttu-id="4ab06-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4ab06-129">None</span></span>

## <span data-ttu-id="4ab06-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ab06-130">OUTPUTS</span></span>

### <span data-ttu-id="4ab06-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="4ab06-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="4ab06-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ab06-132">NOTES</span></span>

## <span data-ttu-id="4ab06-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ab06-133">RELATED LINKS</span></span>
