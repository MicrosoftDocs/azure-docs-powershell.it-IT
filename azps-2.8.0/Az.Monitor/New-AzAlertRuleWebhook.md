---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 1b8d58c6519084db5e679d3087c22adab7c2bef6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404004"
---
# <span data-ttu-id="d8453-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d8453-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="d8453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8453-102">SYNOPSIS</span></span>
<span data-ttu-id="d8453-103">Crea una webhook della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="d8453-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="d8453-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8453-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8453-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d8453-105">DESCRIPTION</span></span>
<span data-ttu-id="d8453-106">Il cmdlet **New-AzAlertRuleWebhook** crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="d8453-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="d8453-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8453-107">EXAMPLES</span></span>

### <span data-ttu-id="d8453-108">Esempio 1: Creare una regola di avviso webhook</span><span class="sxs-lookup"><span data-stu-id="d8453-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="d8453-109">Questo comando crea una webhook della regola di avviso specificando solo l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="d8453-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="d8453-110">Esempio 2: Creare un webhook con una proprietà</span><span class="sxs-lookup"><span data-stu-id="d8453-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="d8453-111">Questo comando crea una webhook della regola di avviso per Contoso.com ha una proprietà e quindi la archivia nella $Actual variabile.</span><span class="sxs-lookup"><span data-stu-id="d8453-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="d8453-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8453-112">PARAMETERS</span></span>

### <span data-ttu-id="d8453-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8453-113">-DefaultProfile</span></span>
<span data-ttu-id="d8453-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d8453-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8453-115">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="d8453-115">-Property</span></span>
<span data-ttu-id="d8453-116">Specifica l'elenco delle proprietà nel formato @(proprietà1 = 'valore1',....).</span><span class="sxs-lookup"><span data-stu-id="d8453-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="d8453-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d8453-117">-ServiceUri</span></span>
<span data-ttu-id="d8453-118">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="d8453-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="d8453-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8453-119">CommonParameters</span></span>
<span data-ttu-id="d8453-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8453-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8453-121">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8453-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8453-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="d8453-122">INPUTS</span></span>

### <span data-ttu-id="d8453-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d8453-123">System.String</span></span>

### <span data-ttu-id="d8453-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8453-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8453-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8453-125">OUTPUTS</span></span>

### <span data-ttu-id="d8453-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="d8453-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="d8453-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="d8453-127">NOTES</span></span>

## <span data-ttu-id="d8453-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8453-128">RELATED LINKS</span></span>


[<span data-ttu-id="d8453-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d8453-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d8453-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d8453-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="d8453-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="d8453-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="d8453-132">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d8453-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


