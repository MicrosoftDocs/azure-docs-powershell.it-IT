---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
ms.openlocfilehash: 20134cc0f2eef927361439fb431bc4ab9308a9a1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867098"
---
# <span data-ttu-id="23af9-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="23af9-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="23af9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23af9-102">SYNOPSIS</span></span>
<span data-ttu-id="23af9-103">Crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="23af9-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23af9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23af9-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23af9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23af9-105">DESCRIPTION</span></span>
<span data-ttu-id="23af9-106">Il cmdlet **New-AzureRmAlertRuleEmail** crea un'azione di posta elettronica per una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="23af9-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="23af9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23af9-107">EXAMPLES</span></span>

### <span data-ttu-id="23af9-108">Esempio 1: creare un'azione di posta elettronica regola di avviso per i proprietari dei servizi</span><span class="sxs-lookup"><span data-stu-id="23af9-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="23af9-109">Questo comando crea un'azione di posta elettronica regola di avviso da inviare per i proprietari del servizio quando viene attivata una regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="23af9-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="23af9-110">Esempio 2: creare un'azione di posta elettronica regola di avviso per i proprietari non del servizio</span><span class="sxs-lookup"><span data-stu-id="23af9-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="23af9-111">Questo comando crea un'azione di posta elettronica regola di avviso per gli indirizzi di posta elettronica specificati, ma non per i proprietari del servizio.</span><span class="sxs-lookup"><span data-stu-id="23af9-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="23af9-112">Esempio 3: creare un'azione di posta elettronica regola di avviso per proprietari di servizi e proprietari non di servizi</span><span class="sxs-lookup"><span data-stu-id="23af9-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="23af9-113">Questo comando crea un'azione di posta elettronica regola di avviso per l'indirizzo specificato e per i proprietari del servizio.</span><span class="sxs-lookup"><span data-stu-id="23af9-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="23af9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23af9-114">PARAMETERS</span></span>

### <span data-ttu-id="23af9-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="23af9-115">-CustomEmail</span></span>
<span data-ttu-id="23af9-116">Specifica un elenco di indirizzi di posta elettronica delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="23af9-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="23af9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23af9-117">-DefaultProfile</span></span>
<span data-ttu-id="23af9-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="23af9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23af9-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="23af9-119">-SendToServiceOwner</span></span>
<span data-ttu-id="23af9-120">Indica che questa operazione Invia un messaggio di posta elettronica ai proprietari del servizio quando viene attivata la regola.</span><span class="sxs-lookup"><span data-stu-id="23af9-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="23af9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23af9-121">CommonParameters</span></span>
<span data-ttu-id="23af9-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23af9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23af9-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23af9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23af9-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23af9-124">INPUTS</span></span>

### <span data-ttu-id="23af9-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="23af9-125">System.String[]</span></span>

### <span data-ttu-id="23af9-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23af9-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23af9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23af9-127">OUTPUTS</span></span>

### <span data-ttu-id="23af9-128">Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="23af9-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="23af9-129">Note</span><span class="sxs-lookup"><span data-stu-id="23af9-129">NOTES</span></span>

## <span data-ttu-id="23af9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23af9-130">RELATED LINKS</span></span>



[<span data-ttu-id="23af9-131">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="23af9-131">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="23af9-132">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="23af9-132">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="23af9-133">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="23af9-133">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


