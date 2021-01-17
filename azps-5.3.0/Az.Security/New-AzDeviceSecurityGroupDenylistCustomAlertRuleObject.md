---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0e1de96eed8b3f1174bebd6a127db91f9733dd67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486299"
---
# <span data-ttu-id="9ae2a-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="9ae2a-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="9ae2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ae2a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ae2a-103">Creare una nuova regola di avviso personalizzata di Deny List per il gruppo sicurezza dispositivi (sicurezza degli avvisi)</span><span class="sxs-lookup"><span data-stu-id="9ae2a-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="9ae2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ae2a-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ae2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ae2a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ae2a-106">Il cmdlet New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject crea un nuovo elenco di regole di avviso personalizzate negate per il gruppo di sicurezza dei dispositivi nella soluzione di sicurezza degli articoli.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="9ae2a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ae2a-107">EXAMPLES</span></span>

### <span data-ttu-id="9ae2a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ae2a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="9ae2a-109">Creare una nuova regola di avviso personalizzata di Deny List con Rull tipo "SomeRuleType" e stato impostato su desable</span><span class="sxs-lookup"><span data-stu-id="9ae2a-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="9ae2a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ae2a-110">PARAMETERS</span></span>

### <span data-ttu-id="9ae2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ae2a-111">-DefaultProfile</span></span>
<span data-ttu-id="9ae2a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ae2a-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="9ae2a-113">-DenylistValue</span></span>
<span data-ttu-id="9ae2a-114">Negare i valori di elenco.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-114">Deny list values.</span></span>

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

### <span data-ttu-id="9ae2a-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9ae2a-115">-Enabled</span></span>
<span data-ttu-id="9ae2a-116">È abilitata la regola.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="9ae2a-117">-Digitare</span><span class="sxs-lookup"><span data-stu-id="9ae2a-117">-Type</span></span>
<span data-ttu-id="9ae2a-118">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-118">Rule type.</span></span>

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

### <span data-ttu-id="9ae2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ae2a-119">CommonParameters</span></span>
<span data-ttu-id="9ae2a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ae2a-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ae2a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ae2a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ae2a-122">INPUTS</span></span>

### <span data-ttu-id="9ae2a-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9ae2a-123">None</span></span>

## <span data-ttu-id="9ae2a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ae2a-124">OUTPUTS</span></span>

### <span data-ttu-id="9ae2a-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ae2a-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="9ae2a-126">Note</span><span class="sxs-lookup"><span data-stu-id="9ae2a-126">NOTES</span></span>

## <span data-ttu-id="9ae2a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ae2a-127">RELATED LINKS</span></span>
