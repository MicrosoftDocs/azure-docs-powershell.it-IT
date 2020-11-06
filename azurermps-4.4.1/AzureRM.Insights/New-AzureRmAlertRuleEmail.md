---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519170"
---
# <span data-ttu-id="095f1-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="095f1-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="095f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="095f1-102">SYNOPSIS</span></span>
<span data-ttu-id="095f1-103">Crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="095f1-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="095f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="095f1-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="095f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="095f1-105">DESCRIPTION</span></span>
<span data-ttu-id="095f1-106">Il cmdlet **New-AzureRmAlertRuleEmail** crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="095f1-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="095f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="095f1-107">EXAMPLES</span></span>

### <span data-ttu-id="095f1-108">Esempio 1: creare un'azione di posta elettronica regola di avviso per i proprietari dei servizi</span><span class="sxs-lookup"><span data-stu-id="095f1-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="095f1-109">Questo comando crea un'azione di posta elettronica regola di avviso da inviare per i proprietari del servizio quando viene attivata una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="095f1-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="095f1-110">Esempio 2: creare un'azione di posta elettronica regola di avviso per i proprietari non del servizio</span><span class="sxs-lookup"><span data-stu-id="095f1-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="095f1-111">Questo comando crea un'azione di posta elettronica regola di avviso per gli indirizzi di posta elettronica specificati, ma non per i proprietari del servizio.</span><span class="sxs-lookup"><span data-stu-id="095f1-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="095f1-112">Esempio 3: creare un'azione di posta elettronica regola di avviso per proprietari di servizi e proprietari non di servizi</span><span class="sxs-lookup"><span data-stu-id="095f1-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

<span data-ttu-id="095f1-113">Questo comando crea un'azione di posta elettronica regola di avviso per l'indirizzo specificato e per i proprietari del servizio.</span><span class="sxs-lookup"><span data-stu-id="095f1-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="095f1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="095f1-114">PARAMETERS</span></span>

### <span data-ttu-id="095f1-115">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="095f1-115">-CustomEmails</span></span>
<span data-ttu-id="095f1-116">Specifica un elenco di indirizzi di posta elettronica delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="095f1-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="095f1-117">-SendToServiceOwners</span><span class="sxs-lookup"><span data-stu-id="095f1-117">-SendToServiceOwners</span></span>
<span data-ttu-id="095f1-118">Indica che questa operazione Invia un messaggio di posta elettronica ai proprietari del servizio quando viene attivata la regola.</span><span class="sxs-lookup"><span data-stu-id="095f1-118">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="095f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095f1-119">-DefaultProfile</span></span>
<span data-ttu-id="095f1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="095f1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095f1-121">CommonParameters</span></span>
<span data-ttu-id="095f1-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095f1-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="095f1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095f1-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="095f1-124">INPUTS</span></span>

## <span data-ttu-id="095f1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="095f1-125">OUTPUTS</span></span>

### <span data-ttu-id="095f1-126">Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="095f1-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="095f1-127">Note</span><span class="sxs-lookup"><span data-stu-id="095f1-127">NOTES</span></span>

## <span data-ttu-id="095f1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="095f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="095f1-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="095f1-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="095f1-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="095f1-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="095f1-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="095f1-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="095f1-132">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="095f1-132">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


