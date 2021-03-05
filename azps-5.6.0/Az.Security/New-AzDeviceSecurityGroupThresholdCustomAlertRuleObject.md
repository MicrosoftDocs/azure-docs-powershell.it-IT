---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 869512fb91e86d90381bbcba9e492198b9a51005
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984174"
---
# <span data-ttu-id="d5313-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="d5313-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="d5313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5313-102">SYNOPSIS</span></span>
<span data-ttu-id="d5313-103">Creare una nuova regola di avviso personalizzata per la soglia per il gruppo di sicurezza dei dispositivi (Sicurezza IoT)</span><span class="sxs-lookup"><span data-stu-id="d5313-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d5313-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5313-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5313-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5313-105">DESCRIPTION</span></span>
<span data-ttu-id="d5313-106">Il cmdlet New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject crea un nuovo elenco di regole di avviso personalizzate per le soglie per il gruppo di sicurezza dei dispositivi nella soluzione di sicurezza IoT.</span><span class="sxs-lookup"><span data-stu-id="d5313-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d5313-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5313-107">EXAMPLES</span></span>

### <span data-ttu-id="d5313-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5313-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="d5313-109">Creare una nuova regola di avviso personalizzata per la soglia dal tipo "SomeRuleType" con stato abilitato per la soglia minima e massima</span><span class="sxs-lookup"><span data-stu-id="d5313-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="d5313-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5313-110">PARAMETERS</span></span>

### <span data-ttu-id="d5313-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5313-111">-DefaultProfile</span></span>
<span data-ttu-id="d5313-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5313-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5313-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d5313-113">-Enabled</span></span>
<span data-ttu-id="d5313-114">La regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="d5313-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5313-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="d5313-115">-MaxThreshold</span></span>
<span data-ttu-id="d5313-116">Soglia massima.</span><span class="sxs-lookup"><span data-stu-id="d5313-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5313-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="d5313-117">-MinThreshold</span></span>
<span data-ttu-id="d5313-118">Soglia minima.</span><span class="sxs-lookup"><span data-stu-id="d5313-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5313-119">-Type</span><span class="sxs-lookup"><span data-stu-id="d5313-119">-Type</span></span>
<span data-ttu-id="d5313-120">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="d5313-120">Rule type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5313-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5313-121">CommonParameters</span></span>
<span data-ttu-id="d5313-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5313-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5313-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5313-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5313-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5313-124">INPUTS</span></span>

### <span data-ttu-id="d5313-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d5313-125">None</span></span>

## <span data-ttu-id="d5313-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5313-126">OUTPUTS</span></span>

### <span data-ttu-id="d5313-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="d5313-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="d5313-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5313-128">NOTES</span></span>

## <span data-ttu-id="d5313-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5313-129">RELATED LINKS</span></span>
