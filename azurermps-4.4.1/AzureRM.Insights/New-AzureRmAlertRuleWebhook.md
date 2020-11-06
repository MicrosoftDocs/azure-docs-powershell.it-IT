---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521241"
---
# <span data-ttu-id="b0280-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b0280-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="b0280-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0280-102">SYNOPSIS</span></span>
<span data-ttu-id="b0280-103">Crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="b0280-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0280-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0280-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0280-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0280-105">DESCRIPTION</span></span>
<span data-ttu-id="b0280-106">Il cmdlet **New-AzureRmAlertRuleWebhook** crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="b0280-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="b0280-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0280-107">EXAMPLES</span></span>

### <span data-ttu-id="b0280-108">Esempio 1: creare un hook di regole di avviso</span><span class="sxs-lookup"><span data-stu-id="b0280-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="b0280-109">Questo comando crea una regola di avviso webhook specificando solo l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="b0280-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="b0280-110">Esempio 2: creare un hook con una proprietà</span><span class="sxs-lookup"><span data-stu-id="b0280-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="b0280-111">Questo comando crea una regola di avviso webhook per Contoso.com che contiene una proprietà e la archivia nella variabile $Actual.</span><span class="sxs-lookup"><span data-stu-id="b0280-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="b0280-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0280-112">PARAMETERS</span></span>

### <span data-ttu-id="b0280-113">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="b0280-113">-Properties</span></span>
<span data-ttu-id="b0280-114">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="b0280-114">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="b0280-115">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="b0280-115">-ServiceUri</span></span>
<span data-ttu-id="b0280-116">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="b0280-116">Specifies the service URI.</span></span>

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

### <span data-ttu-id="b0280-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0280-117">-DefaultProfile</span></span>
<span data-ttu-id="b0280-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0280-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0280-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0280-119">CommonParameters</span></span>
<span data-ttu-id="b0280-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0280-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0280-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0280-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0280-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0280-122">INPUTS</span></span>

## <span data-ttu-id="b0280-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0280-123">OUTPUTS</span></span>

### <span data-ttu-id="b0280-124">Microsoft. Azure. Management. monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="b0280-124">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="b0280-125">Note</span><span class="sxs-lookup"><span data-stu-id="b0280-125">NOTES</span></span>

## <span data-ttu-id="b0280-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0280-126">RELATED LINKS</span></span>

[<span data-ttu-id="b0280-127">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b0280-127">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="b0280-128">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b0280-128">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b0280-129">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b0280-129">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b0280-130">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b0280-130">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="b0280-131">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="b0280-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


