---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337372"
---
# <span data-ttu-id="77a1b-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="77a1b-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="77a1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="77a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="77a1b-103">Creare una nuova regola di avviso personalizzata soglia per il gruppo sicurezza dispositivi (sicurezza degli avvisi)</span><span class="sxs-lookup"><span data-stu-id="77a1b-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="77a1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="77a1b-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77a1b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="77a1b-106">Il cmdlet New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject crea un nuovo elenco di regole di avviso personalizzate soglia per il gruppo sicurezza dispositivi nella soluzione di sicurezza degli articoli.</span><span class="sxs-lookup"><span data-stu-id="77a1b-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="77a1b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="77a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="77a1b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="77a1b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="77a1b-109">Creare una nuova regola di avviso personalizzata soglia da tipo "SomeRuleType" con i valori Ant Enabled di stato per la soglia minima e massima</span><span class="sxs-lookup"><span data-stu-id="77a1b-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="77a1b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="77a1b-110">PARAMETERS</span></span>

### <span data-ttu-id="77a1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a1b-111">-DefaultProfile</span></span>
<span data-ttu-id="77a1b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="77a1b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77a1b-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="77a1b-113">-Enabled</span></span>
<span data-ttu-id="77a1b-114">È abilitata la regola.</span><span class="sxs-lookup"><span data-stu-id="77a1b-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="77a1b-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="77a1b-115">-MaxThreshold</span></span>
<span data-ttu-id="77a1b-116">Soglia massima.</span><span class="sxs-lookup"><span data-stu-id="77a1b-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="77a1b-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="77a1b-117">-MinThreshold</span></span>
<span data-ttu-id="77a1b-118">Soglia minima.</span><span class="sxs-lookup"><span data-stu-id="77a1b-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="77a1b-119">-Digitare</span><span class="sxs-lookup"><span data-stu-id="77a1b-119">-Type</span></span>
<span data-ttu-id="77a1b-120">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="77a1b-120">Rule type.</span></span>

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

### <span data-ttu-id="77a1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a1b-121">CommonParameters</span></span>
<span data-ttu-id="77a1b-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77a1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a1b-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77a1b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a1b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="77a1b-124">INPUTS</span></span>

### <span data-ttu-id="77a1b-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="77a1b-125">None</span></span>

## <span data-ttu-id="77a1b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="77a1b-126">OUTPUTS</span></span>

### <span data-ttu-id="77a1b-127">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="77a1b-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="77a1b-128">Note</span><span class="sxs-lookup"><span data-stu-id="77a1b-128">NOTES</span></span>

## <span data-ttu-id="77a1b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="77a1b-129">RELATED LINKS</span></span>
