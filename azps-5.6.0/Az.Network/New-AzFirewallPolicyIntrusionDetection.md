---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: 3587917e1a4216445e59b182ce6307c7a94684bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996490"
---
# <span data-ttu-id="e165a-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="e165a-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="e165a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e165a-102">SYNOPSIS</span></span>
<span data-ttu-id="e165a-103">Crea un nuovo rilevamento delle intrusioni dei criteri del firewall di Azure da associare ai criteri del firewall</span><span class="sxs-lookup"><span data-stu-id="e165a-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="e165a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e165a-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e165a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e165a-105">DESCRIPTION</span></span>
<span data-ttu-id="e165a-106">Il cmdlet **New-AzFirewallPolicyIntrusionDetection** crea un oggetto di rilevamento delle intrusioni dei criteri del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="e165a-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="e165a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e165a-107">EXAMPLES</span></span>

### <span data-ttu-id="e165a-108">Esempio 1: 1.</span><span class="sxs-lookup"><span data-stu-id="e165a-108">Example 1: 1.</span></span> <span data-ttu-id="e165a-109">Creare il rilevamento delle intrusioni con la modalità</span><span class="sxs-lookup"><span data-stu-id="e165a-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="e165a-110">Questo esempio crea il rilevamento delle intrusioni con la modalità di avviso (rilevamento)</span><span class="sxs-lookup"><span data-stu-id="e165a-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="e165a-111">Esempio 2: 2.</span><span class="sxs-lookup"><span data-stu-id="e165a-111">Example 2: 2.</span></span> <span data-ttu-id="e165a-112">Creare il rilevamento delle intrusioni con override della firma</span><span class="sxs-lookup"><span data-stu-id="e165a-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="e165a-113">Questo esempio crea il rilevamento delle intrusioni con override della firma specifici</span><span class="sxs-lookup"><span data-stu-id="e165a-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="e165a-114">Esempio 3: 3.</span><span class="sxs-lookup"><span data-stu-id="e165a-114">Example 3: 3.</span></span> <span data-ttu-id="e165a-115">Creare criteri del firewall con rilevamento delle intrusioni configurato con impostazione del traffico bypass</span><span class="sxs-lookup"><span data-stu-id="e165a-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="e165a-116">Questo esempio crea il rilevamento delle intrusioni con l'impostazione bypass traffico</span><span class="sxs-lookup"><span data-stu-id="e165a-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="e165a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e165a-117">PARAMETERS</span></span>

### <span data-ttu-id="e165a-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="e165a-118">-BypassTraffic</span></span>
<span data-ttu-id="e165a-119">Elenco di regole per il traffico da bypassare.</span><span class="sxs-lookup"><span data-stu-id="e165a-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e165a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e165a-120">-DefaultProfile</span></span>
<span data-ttu-id="e165a-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e165a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e165a-122">-Mode</span><span class="sxs-lookup"><span data-stu-id="e165a-122">-Mode</span></span>
<span data-ttu-id="e165a-123">Stato generale rilevamento delle intrusioni.</span><span class="sxs-lookup"><span data-stu-id="e165a-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e165a-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="e165a-124">-SignatureOverride</span></span>
<span data-ttu-id="e165a-125">Elenco di stati specifici delle firme.</span><span class="sxs-lookup"><span data-stu-id="e165a-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e165a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e165a-126">-Confirm</span></span>
<span data-ttu-id="e165a-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e165a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e165a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e165a-128">-WhatIf</span></span>
<span data-ttu-id="e165a-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e165a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e165a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e165a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e165a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e165a-131">CommonParameters</span></span>
<span data-ttu-id="e165a-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e165a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e165a-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e165a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e165a-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="e165a-134">INPUTS</span></span>

### <span data-ttu-id="e165a-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e165a-135">None</span></span>

## <span data-ttu-id="e165a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e165a-136">OUTPUTS</span></span>

### <span data-ttu-id="e165a-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="e165a-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="e165a-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="e165a-138">NOTES</span></span>

## <span data-ttu-id="e165a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e165a-139">RELATED LINKS</span></span>
