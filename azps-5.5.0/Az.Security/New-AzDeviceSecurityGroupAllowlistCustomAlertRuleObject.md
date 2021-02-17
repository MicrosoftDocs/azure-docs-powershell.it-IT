---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197918"
---
# <span data-ttu-id="91e09-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="91e09-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="91e09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e09-102">SYNOPSIS</span></span>
<span data-ttu-id="91e09-103">Creare una nuova regola di avviso personalizzata per l'elenco di indirizzi consentiti per il gruppo di sicurezza dei dispositivi (Sicurezza IoT)</span><span class="sxs-lookup"><span data-stu-id="91e09-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="91e09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91e09-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91e09-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91e09-105">DESCRIPTION</span></span>
<span data-ttu-id="91e09-106">Il New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet crea un nuovo elenco di regole di avviso personalizzate consentite per il gruppo di sicurezza dei dispositivi nella soluzione di sicurezza IoT.</span><span class="sxs-lookup"><span data-stu-id="91e09-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="91e09-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91e09-107">EXAMPLES</span></span>

### <span data-ttu-id="91e09-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91e09-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="91e09-109">Crea nuovo avviso personalizzato dell'elenco di utenti consentiti dal tipo "LocalUserNotAllowed" con stato impostato su disable</span><span class="sxs-lookup"><span data-stu-id="91e09-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="91e09-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91e09-110">PARAMETERS</span></span>

### <span data-ttu-id="91e09-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="91e09-111">-AllowlistValue</span></span>
<span data-ttu-id="91e09-112">Valori di elenco consentiti.</span><span class="sxs-lookup"><span data-stu-id="91e09-112">Allow list values.</span></span>

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

### <span data-ttu-id="91e09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e09-113">-DefaultProfile</span></span>
<span data-ttu-id="91e09-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91e09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91e09-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="91e09-115">-Enabled</span></span>
<span data-ttu-id="91e09-116">La regola è abilitata.</span><span class="sxs-lookup"><span data-stu-id="91e09-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="91e09-117">-Type</span><span class="sxs-lookup"><span data-stu-id="91e09-117">-Type</span></span>
<span data-ttu-id="91e09-118">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="91e09-118">Rule type.</span></span>

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

### <span data-ttu-id="91e09-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e09-119">CommonParameters</span></span>
<span data-ttu-id="91e09-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e09-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e09-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91e09-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e09-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="91e09-122">INPUTS</span></span>

### <span data-ttu-id="91e09-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="91e09-123">None</span></span>

## <span data-ttu-id="91e09-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91e09-124">OUTPUTS</span></span>

### <span data-ttu-id="91e09-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="91e09-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="91e09-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="91e09-126">NOTES</span></span>

## <span data-ttu-id="91e09-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91e09-127">RELATED LINKS</span></span>
