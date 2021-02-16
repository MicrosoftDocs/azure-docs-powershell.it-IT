---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: d2389a8d4880b576e51cda41ac3c15bd091257c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184470"
---
# <span data-ttu-id="c5057-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="c5057-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="c5057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5057-102">SYNOPSIS</span></span>
<span data-ttu-id="c5057-103">Crea un nuovo override della firma di rilevamento dell'intrusione dei criteri del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="c5057-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="c5057-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5057-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5057-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5057-105">DESCRIPTION</span></span>
<span data-ttu-id="c5057-106">Il cmdlet **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** crea un oggetto override per la firma dei criteri del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5057-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="c5057-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5057-107">EXAMPLES</span></span>

### <span data-ttu-id="c5057-108">Esempio 1: 1.</span><span class="sxs-lookup"><span data-stu-id="c5057-108">Example 1: 1.</span></span> <span data-ttu-id="c5057-109">Creare il rilevamento delle intrusioni con override della firma</span><span class="sxs-lookup"><span data-stu-id="c5057-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="c5057-110">Questo esempio crea il rilevamento delle intrusioni con firma specifica override sulla modalità negata</span><span class="sxs-lookup"><span data-stu-id="c5057-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="c5057-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5057-111">PARAMETERS</span></span>

### <span data-ttu-id="c5057-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5057-112">-DefaultProfile</span></span>
<span data-ttu-id="c5057-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5057-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5057-114">-Id</span><span class="sxs-lookup"><span data-stu-id="c5057-114">-Id</span></span>
<span data-ttu-id="c5057-115">ID firma.</span><span class="sxs-lookup"><span data-stu-id="c5057-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5057-116">-Modalità</span><span class="sxs-lookup"><span data-stu-id="c5057-116">-Mode</span></span>
<span data-ttu-id="c5057-117">Stato della firma.</span><span class="sxs-lookup"><span data-stu-id="c5057-117">Signature state.</span></span>

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

### <span data-ttu-id="c5057-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5057-118">-Confirm</span></span>
<span data-ttu-id="c5057-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5057-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5057-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5057-120">-WhatIf</span></span>
<span data-ttu-id="c5057-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5057-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5057-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5057-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5057-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5057-123">CommonParameters</span></span>
<span data-ttu-id="c5057-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5057-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5057-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5057-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5057-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5057-126">INPUTS</span></span>

### <span data-ttu-id="c5057-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c5057-127">None</span></span>

## <span data-ttu-id="c5057-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5057-128">OUTPUTS</span></span>

### <span data-ttu-id="c5057-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="c5057-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="c5057-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5057-130">NOTES</span></span>

## <span data-ttu-id="c5057-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5057-131">RELATED LINKS</span></span>
