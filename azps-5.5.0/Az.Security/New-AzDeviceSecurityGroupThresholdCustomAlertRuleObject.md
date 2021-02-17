---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197919"
---
# <span data-ttu-id="9b13c-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b13c-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="9b13c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b13c-102">SYNOPSIS</span></span>
<span data-ttu-id="9b13c-103">Creare una nuova regola di avviso personalizzata per la soglia per il gruppo di sicurezza dei dispositivi (Sicurezza IoT)</span><span class="sxs-lookup"><span data-stu-id="9b13c-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="9b13c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b13c-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b13c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b13c-105">DESCRIPTION</span></span>
<span data-ttu-id="9b13c-106">Il cmdlet New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject crea un nuovo elenco di regole di avviso personalizzate per le soglie per il gruppo di sicurezza dei dispositivi nella soluzione di sicurezza IoT.</span><span class="sxs-lookup"><span data-stu-id="9b13c-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="9b13c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b13c-107">EXAMPLES</span></span>

### <span data-ttu-id="9b13c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b13c-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="9b13c-109">Creare una nuova regola di avviso personalizzata per la soglia dal tipo "SomeRuleType" con stato abilitato per la soglia minima e massima</span><span class="sxs-lookup"><span data-stu-id="9b13c-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="9b13c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b13c-110">PARAMETERS</span></span>

### <span data-ttu-id="9b13c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b13c-111">-DefaultProfile</span></span>
<span data-ttu-id="9b13c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b13c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b13c-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9b13c-113">-Enabled</span></span>
<span data-ttu-id="9b13c-114">La regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9b13c-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="9b13c-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="9b13c-115">-MaxThreshold</span></span>
<span data-ttu-id="9b13c-116">Soglia massima.</span><span class="sxs-lookup"><span data-stu-id="9b13c-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="9b13c-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="9b13c-117">-MinThreshold</span></span>
<span data-ttu-id="9b13c-118">Soglia minima.</span><span class="sxs-lookup"><span data-stu-id="9b13c-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="9b13c-119">-Type</span><span class="sxs-lookup"><span data-stu-id="9b13c-119">-Type</span></span>
<span data-ttu-id="9b13c-120">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="9b13c-120">Rule type.</span></span>

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

### <span data-ttu-id="9b13c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b13c-121">CommonParameters</span></span>
<span data-ttu-id="9b13c-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b13c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b13c-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b13c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b13c-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b13c-124">INPUTS</span></span>

### <span data-ttu-id="9b13c-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9b13c-125">None</span></span>

## <span data-ttu-id="9b13c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b13c-126">OUTPUTS</span></span>

### <span data-ttu-id="9b13c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="9b13c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="9b13c-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b13c-128">NOTES</span></span>

## <span data-ttu-id="9b13c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b13c-129">RELATED LINKS</span></span>
