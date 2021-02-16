---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: c296c44c96d756dc0ca3a107d8eee265a9226b15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184479"
---
# <span data-ttu-id="22d84-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="22d84-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="22d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d84-102">SYNOPSIS</span></span>
<span data-ttu-id="22d84-103">Crea una nuova impostazione del traffico bypass per il rilevamento delle intrusioni dei criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="22d84-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="22d84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22d84-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d84-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22d84-105">DESCRIPTION</span></span>
<span data-ttu-id="22d84-106">Il cmdlet **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** crea un oggetto traffico di bypass per il rilevamento delle intrusioni dei criteri del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="22d84-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="22d84-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22d84-107">EXAMPLES</span></span>

### <span data-ttu-id="22d84-108">Esempio 1: 1.</span><span class="sxs-lookup"><span data-stu-id="22d84-108">Example 1: 1.</span></span> <span data-ttu-id="22d84-109">Creare il traffico bypass con una porta e un indirizzo di origine specifici</span><span class="sxs-lookup"><span data-stu-id="22d84-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="22d84-110">Questo esempio crea il rilevamento delle intrusioni con l'impostazione bypass traffico</span><span class="sxs-lookup"><span data-stu-id="22d84-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="22d84-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22d84-111">PARAMETERS</span></span>

### <span data-ttu-id="22d84-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d84-112">-DefaultProfile</span></span>
<span data-ttu-id="22d84-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22d84-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d84-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="22d84-114">-Description</span></span>
<span data-ttu-id="22d84-115">Ignora descrizione impostazione.</span><span class="sxs-lookup"><span data-stu-id="22d84-115">Bypass setting description.</span></span>

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

### <span data-ttu-id="22d84-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="22d84-116">-DestinationAddress</span></span>
<span data-ttu-id="22d84-117">Elenco di indirizzi IP o intervalli IP di destinazione.</span><span class="sxs-lookup"><span data-stu-id="22d84-117">List of destination IP addresses or ranges.</span></span>

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

### <span data-ttu-id="22d84-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="22d84-118">-DestinationIpGroup</span></span>
<span data-ttu-id="22d84-119">Elenco dei gruppi IpGroup di destinazione.</span><span class="sxs-lookup"><span data-stu-id="22d84-119">List of destination IpGroups.</span></span>

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

### <span data-ttu-id="22d84-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="22d84-120">-DestinationPort</span></span>
<span data-ttu-id="22d84-121">Elenco di porte o intervalli di destinazione.</span><span class="sxs-lookup"><span data-stu-id="22d84-121">List of destination ports or ranges.</span></span>

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

### <span data-ttu-id="22d84-122">-Name</span><span class="sxs-lookup"><span data-stu-id="22d84-122">-Name</span></span>
<span data-ttu-id="22d84-123">Ignora nome impostazione.</span><span class="sxs-lookup"><span data-stu-id="22d84-123">Bypass setting name.</span></span>

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

### <span data-ttu-id="22d84-124">-Protocol</span><span class="sxs-lookup"><span data-stu-id="22d84-124">-Protocol</span></span>
<span data-ttu-id="22d84-125">Bypassare il protocollo di impostazione.</span><span class="sxs-lookup"><span data-stu-id="22d84-125">Bypass setting protocol.</span></span>

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

### <span data-ttu-id="22d84-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="22d84-126">-SourceAddress</span></span>
<span data-ttu-id="22d84-127">Elenco di indirizzi IP o intervalli di origine.</span><span class="sxs-lookup"><span data-stu-id="22d84-127">List of source IP addresses or ranges.</span></span>

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

### <span data-ttu-id="22d84-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="22d84-128">-SourceIpGroup</span></span>
<span data-ttu-id="22d84-129">Elenco dei gruppi IpGroup di origine.</span><span class="sxs-lookup"><span data-stu-id="22d84-129">List of source IpGroups.</span></span>

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

### <span data-ttu-id="22d84-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22d84-130">-Confirm</span></span>
<span data-ttu-id="22d84-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22d84-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d84-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d84-132">-WhatIf</span></span>
<span data-ttu-id="22d84-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22d84-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d84-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22d84-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d84-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d84-135">CommonParameters</span></span>
<span data-ttu-id="22d84-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d84-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d84-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22d84-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d84-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="22d84-138">INPUTS</span></span>

### <span data-ttu-id="22d84-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22d84-139">None</span></span>

## <span data-ttu-id="22d84-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22d84-140">OUTPUTS</span></span>

### <span data-ttu-id="22d84-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="22d84-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="22d84-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="22d84-142">NOTES</span></span>

## <span data-ttu-id="22d84-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22d84-143">RELATED LINKS</span></span>
