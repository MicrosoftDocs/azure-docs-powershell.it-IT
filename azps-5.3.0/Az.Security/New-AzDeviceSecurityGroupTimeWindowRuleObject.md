---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486300"
---
# <span data-ttu-id="980ea-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="980ea-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="980ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="980ea-102">SYNOPSIS</span></span>
<span data-ttu-id="980ea-103">Creare una nuova regola per la finestra temporale per il gruppo sicurezza dispositivi (sicurezza degli Stati)</span><span class="sxs-lookup"><span data-stu-id="980ea-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="980ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="980ea-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="980ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="980ea-105">DESCRIPTION</span></span>
<span data-ttu-id="980ea-106">Il cmdlet New-AzDeviceSecurityGroupTimeWindowRuleObject crea un nuovo elenco di regole di avviso per le finestre temporali per il gruppo sicurezza dispositivi nella soluzione di sicurezza degli articoli.</span><span class="sxs-lookup"><span data-stu-id="980ea-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="980ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="980ea-107">EXAMPLES</span></span>

### <span data-ttu-id="980ea-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="980ea-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="980ea-109">Creare una nuova regola per la finestra temporale da "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="980ea-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="980ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="980ea-110">PARAMETERS</span></span>

### <span data-ttu-id="980ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980ea-111">-DefaultProfile</span></span>
<span data-ttu-id="980ea-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="980ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="980ea-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="980ea-113">-Enabled</span></span>
<span data-ttu-id="980ea-114">È abilitata la regola.</span><span class="sxs-lookup"><span data-stu-id="980ea-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="980ea-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="980ea-115">-MaxThreshold</span></span>
<span data-ttu-id="980ea-116">Soglia massima.</span><span class="sxs-lookup"><span data-stu-id="980ea-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="980ea-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="980ea-117">-MinThreshold</span></span>
<span data-ttu-id="980ea-118">Soglia minima.</span><span class="sxs-lookup"><span data-stu-id="980ea-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="980ea-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="980ea-119">-TimeWindowSize</span></span>
<span data-ttu-id="980ea-120">Dimensioni della finestra ora.</span><span class="sxs-lookup"><span data-stu-id="980ea-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980ea-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="980ea-121">-Type</span></span>
<span data-ttu-id="980ea-122">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="980ea-122">Rule type.</span></span>

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

### <span data-ttu-id="980ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980ea-123">CommonParameters</span></span>
<span data-ttu-id="980ea-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="980ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980ea-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="980ea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980ea-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="980ea-126">INPUTS</span></span>

### <span data-ttu-id="980ea-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="980ea-127">None</span></span>

## <span data-ttu-id="980ea-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="980ea-128">OUTPUTS</span></span>

### <span data-ttu-id="980ea-129">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="980ea-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="980ea-130">Note</span><span class="sxs-lookup"><span data-stu-id="980ea-130">NOTES</span></span>

## <span data-ttu-id="980ea-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="980ea-131">RELATED LINKS</span></span>
