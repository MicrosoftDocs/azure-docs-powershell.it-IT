---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: 619219a300bb1b7317ea4c8c5fce442d43b74ff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513812"
---
# <span data-ttu-id="07725-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="07725-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="07725-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07725-102">SYNOPSIS</span></span>
<span data-ttu-id="07725-103">Crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="07725-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07725-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07725-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07725-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07725-105">DESCRIPTION</span></span>
<span data-ttu-id="07725-106">Il cmdlet **New-AzureRmAlertRuleWebhook** crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="07725-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="07725-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07725-107">EXAMPLES</span></span>

### <span data-ttu-id="07725-108">Esempio 1: creare un hook di regole di avviso</span><span class="sxs-lookup"><span data-stu-id="07725-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="07725-109">Questo comando crea una regola di avviso webhook specificando solo l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="07725-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="07725-110">Esempio 2: creare un hook con una proprietà</span><span class="sxs-lookup"><span data-stu-id="07725-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="07725-111">Questo comando crea una regola di avviso webhook per Contoso.com che contiene una proprietà e la archivia nella variabile $Actual.</span><span class="sxs-lookup"><span data-stu-id="07725-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="07725-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07725-112">PARAMETERS</span></span>

### <span data-ttu-id="07725-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07725-113">-DefaultProfile</span></span>
<span data-ttu-id="07725-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="07725-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07725-115">-Property</span><span class="sxs-lookup"><span data-stu-id="07725-115">-Property</span></span>
<span data-ttu-id="07725-116">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="07725-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07725-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="07725-117">-ServiceUri</span></span>
<span data-ttu-id="07725-118">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="07725-118">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07725-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07725-119">CommonParameters</span></span>
<span data-ttu-id="07725-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07725-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07725-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07725-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07725-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07725-122">INPUTS</span></span>

### <span data-ttu-id="07725-123">System. String</span><span class="sxs-lookup"><span data-stu-id="07725-123">System.String</span></span>

### <span data-ttu-id="07725-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="07725-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07725-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07725-125">OUTPUTS</span></span>

### <span data-ttu-id="07725-126">Microsoft. Azure. Management. monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="07725-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="07725-127">Note</span><span class="sxs-lookup"><span data-stu-id="07725-127">NOTES</span></span>

## <span data-ttu-id="07725-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07725-128">RELATED LINKS</span></span>

[<span data-ttu-id="07725-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="07725-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="07725-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="07725-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="07725-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="07725-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="07725-132">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="07725-132">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="07725-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="07725-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)

