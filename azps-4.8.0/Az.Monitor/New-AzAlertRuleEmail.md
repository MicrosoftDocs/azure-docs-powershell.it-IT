---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189586"
---
# <span data-ttu-id="049b1-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="049b1-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="049b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="049b1-102">SYNOPSIS</span></span>
<span data-ttu-id="049b1-103">Crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="049b1-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="049b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="049b1-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="049b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="049b1-105">DESCRIPTION</span></span>
<span data-ttu-id="049b1-106">Il cmdlet **New-AzAlertRuleEmail** crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="049b1-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="049b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="049b1-107">EXAMPLES</span></span>

### <span data-ttu-id="049b1-108">Esempio 1: creare un'azione di posta elettronica regola di avviso per i proprietari dei servizi</span><span class="sxs-lookup"><span data-stu-id="049b1-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="049b1-109">Questo comando crea un'azione di posta elettronica regola di avviso da inviare per i proprietari del servizio quando viene attivata una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="049b1-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="049b1-110">Esempio 2: creare un'azione di posta elettronica regola di avviso per i proprietari non del servizio</span><span class="sxs-lookup"><span data-stu-id="049b1-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="049b1-111">Questo comando crea un'azione di posta elettronica regola di avviso per gli indirizzi di posta elettronica specificati, ma non per i proprietari del servizio.</span><span class="sxs-lookup"><span data-stu-id="049b1-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="049b1-112">Esempio 3: creare un'azione di posta elettronica regola di avviso per proprietari di servizi e proprietari non di servizi</span><span class="sxs-lookup"><span data-stu-id="049b1-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="049b1-113">Questo comando crea un'azione di posta elettronica regola di avviso per l'indirizzo specificato e per i proprietari del servizio.</span><span class="sxs-lookup"><span data-stu-id="049b1-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="049b1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="049b1-114">PARAMETERS</span></span>

### <span data-ttu-id="049b1-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="049b1-115">-CustomEmail</span></span>
<span data-ttu-id="049b1-116">Specifica un elenco di indirizzi di posta elettronica delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="049b1-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="049b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049b1-117">-DefaultProfile</span></span>
<span data-ttu-id="049b1-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="049b1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="049b1-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="049b1-119">-SendToServiceOwner</span></span>
<span data-ttu-id="049b1-120">Indica che questa operazione Invia un messaggio di posta elettronica ai proprietari del servizio quando viene attivata la regola.</span><span class="sxs-lookup"><span data-stu-id="049b1-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="049b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049b1-121">CommonParameters</span></span>
<span data-ttu-id="049b1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049b1-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="049b1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049b1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="049b1-124">INPUTS</span></span>

### <span data-ttu-id="049b1-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="049b1-125">System.String[]</span></span>

### <span data-ttu-id="049b1-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="049b1-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="049b1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="049b1-127">OUTPUTS</span></span>

### <span data-ttu-id="049b1-128">Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="049b1-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="049b1-129">Note</span><span class="sxs-lookup"><span data-stu-id="049b1-129">NOTES</span></span>

## <span data-ttu-id="049b1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="049b1-130">RELATED LINKS</span></span>

[<span data-ttu-id="049b1-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="049b1-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="049b1-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="049b1-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="049b1-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="049b1-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="049b1-134">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="049b1-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

