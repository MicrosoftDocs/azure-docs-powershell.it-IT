---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981694"
---
# <span data-ttu-id="2d6d7-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="2d6d7-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="2d6d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6d7-103">Crea una nuova impostazione del traffico bypass per il rilevamento delle intrusioni dei criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2d6d7-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="2d6d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d6d7-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d6d7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2d6d7-105">DESCRIPTION</span></span>
<span data-ttu-id="2d6d7-106">Il cmdlet **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** crea un oggetto traffico di bypass per il rilevamento delle intrusioni dei criteri del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="2d6d7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d6d7-107">EXAMPLES</span></span>

### <span data-ttu-id="2d6d7-108">Esempio 1: 1.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-108">Example 1: 1.</span></span> <span data-ttu-id="2d6d7-109">Creare il traffico bypass con una porta e un indirizzo di origine specifici</span><span class="sxs-lookup"><span data-stu-id="2d6d7-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="2d6d7-110">Questo esempio crea il rilevamento delle intrusioni con l'impostazione bypass traffico</span><span class="sxs-lookup"><span data-stu-id="2d6d7-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="2d6d7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d6d7-111">PARAMETERS</span></span>

### <span data-ttu-id="2d6d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6d7-112">-DefaultProfile</span></span>
<span data-ttu-id="2d6d7-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d6d7-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d6d7-114">-Description</span></span>
<span data-ttu-id="2d6d7-115">Ignora descrizione impostazione.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-115">Bypass setting description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d7-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2d6d7-116">-DestinationAddress</span></span>
<span data-ttu-id="2d6d7-117">Elenco di indirizzi IP o intervalli IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-117">List of destination IP addresses or ranges.</span></span>

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

### <span data-ttu-id="2d6d7-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d6d7-118">-DestinationIpGroup</span></span>
<span data-ttu-id="2d6d7-119">Elenco dei gruppi IpGroup di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-119">List of destination IpGroups.</span></span>

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

### <span data-ttu-id="2d6d7-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2d6d7-120">-DestinationPort</span></span>
<span data-ttu-id="2d6d7-121">Elenco di porte o intervalli di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2d6d7-122">-Name</span></span>
<span data-ttu-id="2d6d7-123">Ignora nome impostazione.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-123">Bypass setting name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d7-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2d6d7-124">-Protocol</span></span>
<span data-ttu-id="2d6d7-125">Bypassare il protocollo di impostazione.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d7-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="2d6d7-126">-SourceAddress</span></span>
<span data-ttu-id="2d6d7-127">Elenco di indirizzi IP o intervalli di origine.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-127">List of source IP addresses or ranges.</span></span>

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

### <span data-ttu-id="2d6d7-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d6d7-128">-SourceIpGroup</span></span>
<span data-ttu-id="2d6d7-129">Elenco dei gruppi IpGroup di origine.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-129">List of source IpGroups.</span></span>

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

### <span data-ttu-id="2d6d7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d6d7-130">-Confirm</span></span>
<span data-ttu-id="2d6d7-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d6d7-132">-WhatIf</span></span>
<span data-ttu-id="2d6d7-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d6d7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6d7-135">CommonParameters</span></span>
<span data-ttu-id="2d6d7-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6d7-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6d7-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="2d6d7-138">INPUTS</span></span>

### <span data-ttu-id="2d6d7-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2d6d7-139">None</span></span>

## <span data-ttu-id="2d6d7-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d6d7-140">OUTPUTS</span></span>

### <span data-ttu-id="2d6d7-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="2d6d7-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="2d6d7-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="2d6d7-142">NOTES</span></span>

## <span data-ttu-id="2d6d7-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d6d7-143">RELATED LINKS</span></span>
