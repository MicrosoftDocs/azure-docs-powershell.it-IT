---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 485f244caa78bffda71d6129990c76daa8b173c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861114"
---
# <span data-ttu-id="5d581-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="5d581-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="5d581-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d581-102">SYNOPSIS</span></span>
<span data-ttu-id="5d581-103">Crea un oggetto di tipo gruppo di azioni Azns</span><span class="sxs-lookup"><span data-stu-id="5d581-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="5d581-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d581-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d581-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d581-105">DESCRIPTION</span></span>
<span data-ttu-id="5d581-106">Crea un oggetto di tipo gruppo di azioni Azns.</span><span class="sxs-lookup"><span data-stu-id="5d581-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="5d581-107">Questo oggetto deve essere passato al comando che crea la regola di avviso del log.</span><span class="sxs-lookup"><span data-stu-id="5d581-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="5d581-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d581-108">EXAMPLES</span></span>

### <span data-ttu-id="5d581-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d581-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="5d581-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d581-110">PARAMETERS</span></span>

### <span data-ttu-id="5d581-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="5d581-111">-ActionGroup</span></span>
<span data-ttu-id="5d581-112">Elenco di gruppi di azioni a cui inviare una notifica</span><span class="sxs-lookup"><span data-stu-id="5d581-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="5d581-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="5d581-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="5d581-114">Payload webhook personalizzato</span><span class="sxs-lookup"><span data-stu-id="5d581-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="5d581-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d581-115">-DefaultProfile</span></span>
<span data-ttu-id="5d581-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d581-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d581-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="5d581-117">-EmailSubject</span></span>
<span data-ttu-id="5d581-118">Oggetto della notifica di avviso di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="5d581-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="5d581-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d581-119">CommonParameters</span></span>
<span data-ttu-id="5d581-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d581-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d581-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d581-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d581-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d581-122">INPUTS</span></span>

### <span data-ttu-id="5d581-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5d581-123">None</span></span>

## <span data-ttu-id="5d581-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d581-124">OUTPUTS</span></span>

### <span data-ttu-id="5d581-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="5d581-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="5d581-126">Note</span><span class="sxs-lookup"><span data-stu-id="5d581-126">NOTES</span></span>

## <span data-ttu-id="5d581-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d581-127">RELATED LINKS</span></span>
