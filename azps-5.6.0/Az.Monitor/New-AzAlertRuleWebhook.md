---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 22afc323e827c543150bffb317f1b5db5275d82c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979885"
---
# <span data-ttu-id="a2f2b-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="a2f2b-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="a2f2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f2b-103">Crea una webhook della regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="a2f2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2f2b-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2f2b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="a2f2b-106">Il cmdlet **New-AzAlertRuleWebhook** crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="a2f2b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="a2f2b-108">Esempio 1: Creare una regola di avviso webhook</span><span class="sxs-lookup"><span data-stu-id="a2f2b-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="a2f2b-109">Questo comando crea una webhook della regola di avviso specificando solo l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="a2f2b-110">Esempio 2: Creare un webhook con una proprietà</span><span class="sxs-lookup"><span data-stu-id="a2f2b-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="a2f2b-111">Questo comando crea una webhook della regola di avviso per Contoso.com ha una proprietà e quindi la archivia nella $Actual variabile.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="a2f2b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2f2b-112">PARAMETERS</span></span>

### <span data-ttu-id="a2f2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f2b-113">-DefaultProfile</span></span>
<span data-ttu-id="a2f2b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a2f2b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2f2b-115">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2f2b-115">-Property</span></span>
<span data-ttu-id="a2f2b-116">Specifica l'elenco delle proprietà nel formato @(proprietà1 = 'valore1',....).</span><span class="sxs-lookup"><span data-stu-id="a2f2b-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="a2f2b-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="a2f2b-117">-ServiceUri</span></span>
<span data-ttu-id="a2f2b-118">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="a2f2b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f2b-119">CommonParameters</span></span>
<span data-ttu-id="a2f2b-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f2b-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2f2b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f2b-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2f2b-122">INPUTS</span></span>

### <span data-ttu-id="a2f2b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a2f2b-123">System.String</span></span>

### <span data-ttu-id="a2f2b-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2f2b-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2f2b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2f2b-125">OUTPUTS</span></span>

### <span data-ttu-id="a2f2b-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="a2f2b-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="a2f2b-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2f2b-127">NOTES</span></span>

## <span data-ttu-id="a2f2b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2f2b-128">RELATED LINKS</span></span>

[<span data-ttu-id="a2f2b-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="a2f2b-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="a2f2b-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a2f2b-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="a2f2b-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a2f2b-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="a2f2b-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="a2f2b-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="a2f2b-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="a2f2b-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


