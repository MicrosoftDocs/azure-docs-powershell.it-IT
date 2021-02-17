---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: aa1570a1c8a2fc6101976c7cc6dc670e268f1c97
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399380"
---
# <span data-ttu-id="b5804-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b5804-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="b5804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5804-102">SYNOPSIS</span></span>
<span data-ttu-id="b5804-103">Crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="b5804-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="b5804-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5804-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5804-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5804-105">DESCRIPTION</span></span>
<span data-ttu-id="b5804-106">Il cmdlet **New-AzAlertRuleEmail** crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="b5804-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="b5804-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5804-107">EXAMPLES</span></span>

### <span data-ttu-id="b5804-108">Esempio 1: Creare un'azione di posta elettronica con una regola di avviso per i proprietari dei servizi</span><span class="sxs-lookup"><span data-stu-id="b5804-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="b5804-109">Questo comando crea un'azione di posta elettronica relativa a una regola di avviso da inviare ai proprietari dei servizi quando viene creata una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="b5804-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="b5804-110">Esempio 2: Creare un'azione di posta elettronica con una regola di avviso per i proprietari di servizi non</span><span class="sxs-lookup"><span data-stu-id="b5804-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="b5804-111">Questo comando crea un'azione di posta elettronica con una regola di avviso per gli indirizzi di posta elettronica specificati, ma non per i proprietari dei servizi.</span><span class="sxs-lookup"><span data-stu-id="b5804-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="b5804-112">Esempio 3: Creare un'azione di posta elettronica con una regola di avviso per proprietari di servizi e non proprietari di servizi</span><span class="sxs-lookup"><span data-stu-id="b5804-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="b5804-113">Questo comando crea un'azione di posta elettronica con una regola di avviso per l'indirizzo specificato e per i proprietari dei servizi.</span><span class="sxs-lookup"><span data-stu-id="b5804-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="b5804-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5804-114">PARAMETERS</span></span>

### <span data-ttu-id="b5804-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="b5804-115">-CustomEmail</span></span>
<span data-ttu-id="b5804-116">Specifica un elenco di indirizzi di posta elettronica separati da virgola.</span><span class="sxs-lookup"><span data-stu-id="b5804-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5804-117">-DefaultProfile</span></span>
<span data-ttu-id="b5804-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b5804-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5804-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="b5804-119">-SendToServiceOwner</span></span>
<span data-ttu-id="b5804-120">Indica che questa operazione invia un messaggio di posta elettronica ai proprietari del servizio quando la regola viene applicata.</span><span class="sxs-lookup"><span data-stu-id="b5804-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5804-121">CommonParameters</span></span>
<span data-ttu-id="b5804-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5804-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5804-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5804-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5804-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5804-124">INPUTS</span></span>

### <span data-ttu-id="b5804-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b5804-125">System.String[]</span></span>

### <span data-ttu-id="b5804-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b5804-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b5804-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5804-127">OUTPUTS</span></span>

### <span data-ttu-id="b5804-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="b5804-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="b5804-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5804-129">NOTES</span></span>

## <span data-ttu-id="b5804-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5804-130">RELATED LINKS</span></span>


[<span data-ttu-id="b5804-131">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5804-131">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="b5804-132">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b5804-132">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="b5804-133">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b5804-133">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


