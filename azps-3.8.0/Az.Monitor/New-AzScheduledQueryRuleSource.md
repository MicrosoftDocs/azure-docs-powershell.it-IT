---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0fe5684805dfc3047abb39040d80eb8a388cf5a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018341"
---
# <span data-ttu-id="cf3c0-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cf3c0-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="cf3c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3c0-103">Crea un oggetto di tipo origine</span><span class="sxs-lookup"><span data-stu-id="cf3c0-103">Creates an object of type Source</span></span>

## <span data-ttu-id="cf3c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf3c0-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf3c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf3c0-105">DESCRIPTION</span></span>
<span data-ttu-id="cf3c0-106">Crea un oggetto di tipo source.</span><span class="sxs-lookup"><span data-stu-id="cf3c0-106">Creates an object of type Source.</span></span>
<span data-ttu-id="cf3c0-107">Questo oggetto deve essere passato al comando che crea la regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="cf3c0-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="cf3c0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf3c0-108">EXAMPLES</span></span>

### <span data-ttu-id="cf3c0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf3c0-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="cf3c0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf3c0-110">PARAMETERS</span></span>

### <span data-ttu-id="cf3c0-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="cf3c0-111">-AuthorizedResource</span></span>
<span data-ttu-id="cf3c0-112">Elenco delle risorse autorizzate per questo avviso</span><span class="sxs-lookup"><span data-stu-id="cf3c0-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="cf3c0-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="cf3c0-113">-DataSourceId</span></span>
<span data-ttu-id="cf3c0-114">Origine dati in cui viene creato questo avviso</span><span class="sxs-lookup"><span data-stu-id="cf3c0-114">The data source on which this alert is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3c0-115">-DefaultProfile</span></span>
<span data-ttu-id="cf3c0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf3c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf3c0-117">-Query</span><span class="sxs-lookup"><span data-stu-id="cf3c0-117">-Query</span></span>
<span data-ttu-id="cf3c0-118">Query di avviso</span><span class="sxs-lookup"><span data-stu-id="cf3c0-118">The alert query</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf3c0-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="cf3c0-119">-QueryType</span></span>
<span data-ttu-id="cf3c0-120">Tipo di query-valori attualmente supportati: ResultCount</span><span class="sxs-lookup"><span data-stu-id="cf3c0-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="cf3c0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3c0-121">CommonParameters</span></span>
<span data-ttu-id="cf3c0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3c0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3c0-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf3c0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3c0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf3c0-124">INPUTS</span></span>

### <span data-ttu-id="cf3c0-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cf3c0-125">None</span></span>

## <span data-ttu-id="cf3c0-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf3c0-126">OUTPUTS</span></span>

### <span data-ttu-id="cf3c0-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cf3c0-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="cf3c0-128">Note</span><span class="sxs-lookup"><span data-stu-id="cf3c0-128">NOTES</span></span>

## <span data-ttu-id="cf3c0-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf3c0-129">RELATED LINKS</span></span>
