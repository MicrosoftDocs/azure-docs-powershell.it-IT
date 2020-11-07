---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 23c32ae1520ac750aa91db3a5924b2a4d292417a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854058"
---
# <span data-ttu-id="d3d26-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d3d26-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="d3d26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3d26-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d26-103">Crea un oggetto di tipo origine</span><span class="sxs-lookup"><span data-stu-id="d3d26-103">Creates an object of type Source</span></span>

## <span data-ttu-id="d3d26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3d26-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3d26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3d26-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d26-106">Crea un oggetto di tipo source.</span><span class="sxs-lookup"><span data-stu-id="d3d26-106">Creates an object of type Source.</span></span>
<span data-ttu-id="d3d26-107">Questo oggetto deve essere passato al comando che crea la regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="d3d26-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="d3d26-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3d26-108">EXAMPLES</span></span>

### <span data-ttu-id="d3d26-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3d26-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="d3d26-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3d26-110">PARAMETERS</span></span>

### <span data-ttu-id="d3d26-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="d3d26-111">-AuthorizedResource</span></span>
<span data-ttu-id="d3d26-112">Elenco delle risorse autorizzate per questo avviso</span><span class="sxs-lookup"><span data-stu-id="d3d26-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="d3d26-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="d3d26-113">-DataSourceId</span></span>
<span data-ttu-id="d3d26-114">Origine dati in cui viene creato questo avviso</span><span class="sxs-lookup"><span data-stu-id="d3d26-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="d3d26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d26-115">-DefaultProfile</span></span>
<span data-ttu-id="d3d26-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d26-117">-Query</span><span class="sxs-lookup"><span data-stu-id="d3d26-117">-Query</span></span>
<span data-ttu-id="d3d26-118">Query di avviso</span><span class="sxs-lookup"><span data-stu-id="d3d26-118">The alert query</span></span>

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

### <span data-ttu-id="d3d26-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="d3d26-119">-QueryType</span></span>
<span data-ttu-id="d3d26-120">Tipo di query-valori attualmente supportati: ResultCount</span><span class="sxs-lookup"><span data-stu-id="d3d26-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="d3d26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d26-121">CommonParameters</span></span>
<span data-ttu-id="d3d26-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d26-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3d26-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d26-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3d26-124">INPUTS</span></span>

### <span data-ttu-id="d3d26-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d3d26-125">None</span></span>

## <span data-ttu-id="d3d26-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3d26-126">OUTPUTS</span></span>

### <span data-ttu-id="d3d26-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d3d26-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="d3d26-128">Note</span><span class="sxs-lookup"><span data-stu-id="d3d26-128">NOTES</span></span>

## <span data-ttu-id="d3d26-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3d26-129">RELATED LINKS</span></span>
