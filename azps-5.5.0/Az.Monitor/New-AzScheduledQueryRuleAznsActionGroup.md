---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184926"
---
# <span data-ttu-id="169e0-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="169e0-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="169e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="169e0-102">SYNOPSIS</span></span>
<span data-ttu-id="169e0-103">Crea un oggetto di tipo Gruppo di azioni Azns</span><span class="sxs-lookup"><span data-stu-id="169e0-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="169e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="169e0-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="169e0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="169e0-105">DESCRIPTION</span></span>
<span data-ttu-id="169e0-106">Crea un oggetto di tipo Gruppo di azioni azns.</span><span class="sxs-lookup"><span data-stu-id="169e0-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="169e0-107">Questo oggetto deve essere passato al comando che crea la regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="169e0-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="169e0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="169e0-108">EXAMPLES</span></span>

### <span data-ttu-id="169e0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="169e0-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="169e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="169e0-110">PARAMETERS</span></span>

### <span data-ttu-id="169e0-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="169e0-111">-ActionGroup</span></span>
<span data-ttu-id="169e0-112">Elenco dei gruppi di azioni a cui inviare una notifica</span><span class="sxs-lookup"><span data-stu-id="169e0-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169e0-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="169e0-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="169e0-114">Payload Webhook personalizzato</span><span class="sxs-lookup"><span data-stu-id="169e0-114">The customized webhook payload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169e0-115">-DefaultProfile</span></span>
<span data-ttu-id="169e0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="169e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="169e0-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="169e0-117">-EmailSubject</span></span>
<span data-ttu-id="169e0-118">Oggetto del messaggio di posta elettronica della notifica di avviso</span><span class="sxs-lookup"><span data-stu-id="169e0-118">The email subject of alert notification</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169e0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169e0-119">CommonParameters</span></span>
<span data-ttu-id="169e0-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169e0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169e0-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="169e0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169e0-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="169e0-122">INPUTS</span></span>

### <span data-ttu-id="169e0-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="169e0-123">None</span></span>

## <span data-ttu-id="169e0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="169e0-124">OUTPUTS</span></span>

### <span data-ttu-id="169e0-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="169e0-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="169e0-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="169e0-126">NOTES</span></span>

## <span data-ttu-id="169e0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="169e0-127">RELATED LINKS</span></span>
