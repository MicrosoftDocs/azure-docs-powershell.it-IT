---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208322"
---
# <span data-ttu-id="e3b01-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="e3b01-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="e3b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b01-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b01-103">Creare una nuova regola di avviso personalizzata per l'elenco dei dispositivi non attendibili per il gruppo di sicurezza IoT (IoT Security)</span><span class="sxs-lookup"><span data-stu-id="e3b01-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="e3b01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3b01-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3b01-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3b01-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b01-106">Il cmdlet New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject crea un nuovo elenco di regole di avviso personalizzate non negate per il gruppo di sicurezza dei dispositivi nella soluzione di sicurezza IoT.</span><span class="sxs-lookup"><span data-stu-id="e3b01-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="e3b01-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3b01-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b01-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3b01-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="e3b01-109">Creare una nuova regola di avviso personalizzata con il tipo di avviso personalizzato "SomeRuleType" e lo stato impostato su desable</span><span class="sxs-lookup"><span data-stu-id="e3b01-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="e3b01-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3b01-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b01-111">-DefaultProfile</span></span>
<span data-ttu-id="e3b01-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b01-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="e3b01-113">-DenylistValue</span></span>
<span data-ttu-id="e3b01-114">Valori dell'elenco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="e3b01-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b01-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e3b01-115">-Enabled</span></span>
<span data-ttu-id="e3b01-116">La regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e3b01-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="e3b01-117">-Type</span><span class="sxs-lookup"><span data-stu-id="e3b01-117">-Type</span></span>
<span data-ttu-id="e3b01-118">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="e3b01-118">Rule type.</span></span>

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

### <span data-ttu-id="e3b01-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b01-119">CommonParameters</span></span>
<span data-ttu-id="e3b01-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b01-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b01-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3b01-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b01-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3b01-122">INPUTS</span></span>

### <span data-ttu-id="e3b01-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3b01-123">None</span></span>

## <span data-ttu-id="e3b01-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3b01-124">OUTPUTS</span></span>

### <span data-ttu-id="e3b01-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3b01-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="e3b01-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3b01-126">NOTES</span></span>

## <span data-ttu-id="e3b01-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3b01-127">RELATED LINKS</span></span>
