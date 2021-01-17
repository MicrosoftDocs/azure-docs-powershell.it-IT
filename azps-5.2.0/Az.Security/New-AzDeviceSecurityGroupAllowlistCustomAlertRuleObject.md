---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337396"
---
# <span data-ttu-id="43455-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="43455-101">New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject</span></span>

## <span data-ttu-id="43455-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43455-102">SYNOPSIS</span></span>
<span data-ttu-id="43455-103">Creare una nuova regola di avviso personalizzata elenco Consenti per il gruppo sicurezza dispositivi (sicurezza degli avvisi)</span><span class="sxs-lookup"><span data-stu-id="43455-103">Create new allow list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="43455-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43455-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43455-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43455-105">DESCRIPTION</span></span>
<span data-ttu-id="43455-106">Il cmdlet New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject crea un nuovo elenco di regole di avviso personalizzate consentite per il gruppo di sicurezza dei dispositivi nella soluzione di sicurezza degli articoli.</span><span class="sxs-lookup"><span data-stu-id="43455-106">The New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet creates a new list of allowed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="43455-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43455-107">EXAMPLES</span></span>

### <span data-ttu-id="43455-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43455-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

<span data-ttu-id="43455-109">Creare un nuovo elenco di avvisi Rull da tipo "LocalUserNotAllowed" con stato impostato su Disabilita</span><span class="sxs-lookup"><span data-stu-id="43455-109">Create new allow list custom alert rull from type "LocalUserNotAllowed" with status set to disable</span></span>

## <span data-ttu-id="43455-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43455-110">PARAMETERS</span></span>

### <span data-ttu-id="43455-111">-AllowlistValue</span><span class="sxs-lookup"><span data-stu-id="43455-111">-AllowlistValue</span></span>
<span data-ttu-id="43455-112">Consenti valori elenco.</span><span class="sxs-lookup"><span data-stu-id="43455-112">Allow list values.</span></span>

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

### <span data-ttu-id="43455-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43455-113">-DefaultProfile</span></span>
<span data-ttu-id="43455-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43455-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43455-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="43455-115">-Enabled</span></span>
<span data-ttu-id="43455-116">È abilitata la regola.</span><span class="sxs-lookup"><span data-stu-id="43455-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="43455-117">-Digitare</span><span class="sxs-lookup"><span data-stu-id="43455-117">-Type</span></span>
<span data-ttu-id="43455-118">Tipo di regola.</span><span class="sxs-lookup"><span data-stu-id="43455-118">Rule type.</span></span>

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

### <span data-ttu-id="43455-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43455-119">CommonParameters</span></span>
<span data-ttu-id="43455-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43455-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43455-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43455-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43455-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43455-122">INPUTS</span></span>

### <span data-ttu-id="43455-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="43455-123">None</span></span>

## <span data-ttu-id="43455-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43455-124">OUTPUTS</span></span>

### <span data-ttu-id="43455-125">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="43455-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule</span></span>

## <span data-ttu-id="43455-126">Note</span><span class="sxs-lookup"><span data-stu-id="43455-126">NOTES</span></span>

## <span data-ttu-id="43455-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43455-127">RELATED LINKS</span></span>
