---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191438"
---
# <span data-ttu-id="2c31e-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2c31e-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="2c31e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c31e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c31e-103">Crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="2c31e-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="2c31e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c31e-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c31e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c31e-105">DESCRIPTION</span></span>
<span data-ttu-id="2c31e-106">Il cmdlet **New-AzAlertRuleWebhook** crea una regola di avviso webhook.</span><span class="sxs-lookup"><span data-stu-id="2c31e-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="2c31e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c31e-107">EXAMPLES</span></span>

### <span data-ttu-id="2c31e-108">Esempio 1: creare un hook di regole di avviso</span><span class="sxs-lookup"><span data-stu-id="2c31e-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="2c31e-109">Questo comando crea una regola di avviso webhook specificando solo l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="2c31e-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="2c31e-110">Esempio 2: creare un hook con una proprietà</span><span class="sxs-lookup"><span data-stu-id="2c31e-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="2c31e-111">Questo comando crea una regola di avviso webhook per Contoso.com che contiene una proprietà e la archivia nella variabile $Actual.</span><span class="sxs-lookup"><span data-stu-id="2c31e-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="2c31e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c31e-112">PARAMETERS</span></span>

### <span data-ttu-id="2c31e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c31e-113">-DefaultProfile</span></span>
<span data-ttu-id="2c31e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2c31e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c31e-115">-Property</span><span class="sxs-lookup"><span data-stu-id="2c31e-115">-Property</span></span>
<span data-ttu-id="2c31e-116">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="2c31e-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="2c31e-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="2c31e-117">-ServiceUri</span></span>
<span data-ttu-id="2c31e-118">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="2c31e-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="2c31e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c31e-119">CommonParameters</span></span>
<span data-ttu-id="2c31e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c31e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c31e-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c31e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c31e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c31e-122">INPUTS</span></span>

### <span data-ttu-id="2c31e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2c31e-123">System.String</span></span>

### <span data-ttu-id="2c31e-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2c31e-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2c31e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c31e-125">OUTPUTS</span></span>

### <span data-ttu-id="2c31e-126">Microsoft. Azure. Management. monitor. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="2c31e-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="2c31e-127">Note</span><span class="sxs-lookup"><span data-stu-id="2c31e-127">NOTES</span></span>

## <span data-ttu-id="2c31e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c31e-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c31e-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c31e-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="2c31e-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c31e-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="2c31e-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2c31e-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="2c31e-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="2c31e-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="2c31e-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="2c31e-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


