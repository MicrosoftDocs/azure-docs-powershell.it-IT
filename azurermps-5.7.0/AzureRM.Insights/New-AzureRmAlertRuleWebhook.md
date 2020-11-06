---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: 24f882ce9190553028a7d0eed80480da4c4f2bfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515704"
---
# <span data-ttu-id="7e68d-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7e68d-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="7e68d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e68d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e68d-103">Crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="7e68d-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e68d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e68d-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e68d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e68d-105">DESCRIPTION</span></span>
<span data-ttu-id="7e68d-106">Il cmdlet **New-AzureRmAlertRuleWebhook** crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="7e68d-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="7e68d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e68d-107">EXAMPLES</span></span>

### <span data-ttu-id="7e68d-108">Esempio 1: creare un hook di regole di avviso</span><span class="sxs-lookup"><span data-stu-id="7e68d-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="7e68d-109">Questo comando crea una regola di avviso webhook specificando solo l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="7e68d-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="7e68d-110">Esempio 2: creare un hook con una proprietà</span><span class="sxs-lookup"><span data-stu-id="7e68d-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="7e68d-111">Questo comando crea una regola di avviso webhook per Contoso.com che contiene una proprietà e la archivia nella variabile $Actual.</span><span class="sxs-lookup"><span data-stu-id="7e68d-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="7e68d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e68d-112">PARAMETERS</span></span>

### <span data-ttu-id="7e68d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e68d-113">-DefaultProfile</span></span>
<span data-ttu-id="7e68d-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7e68d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e68d-115">-Property</span><span class="sxs-lookup"><span data-stu-id="7e68d-115">-Property</span></span>
<span data-ttu-id="7e68d-116">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="7e68d-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e68d-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="7e68d-117">-ServiceUri</span></span>
<span data-ttu-id="7e68d-118">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="7e68d-118">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e68d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e68d-119">CommonParameters</span></span>
<span data-ttu-id="7e68d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e68d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e68d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e68d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e68d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e68d-122">INPUTS</span></span>

### <span data-ttu-id="7e68d-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7e68d-123">None</span></span>
<span data-ttu-id="7e68d-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7e68d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e68d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e68d-125">OUTPUTS</span></span>

### <span data-ttu-id="7e68d-126">Microsoft. Azure. Management. monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="7e68d-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="7e68d-127">Note</span><span class="sxs-lookup"><span data-stu-id="7e68d-127">NOTES</span></span>

## <span data-ttu-id="7e68d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e68d-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e68d-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e68d-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="7e68d-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e68d-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7e68d-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e68d-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7e68d-132">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="7e68d-132">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="7e68d-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="7e68d-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


