---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4a387da5b8f1f4ed9e6f3653a32ff8880ffaa734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514635"
---
# <span data-ttu-id="46404-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="46404-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="46404-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46404-102">SYNOPSIS</span></span>
<span data-ttu-id="46404-103">Ottiene funzioni in un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="46404-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46404-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46404-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46404-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46404-105">DESCRIPTION</span></span>
<span data-ttu-id="46404-106">Il cmdlet **Get-AzureRmStreamAnalyticsFunction** ottiene un elenco delle funzioni definite in un processo di analisi di Azure Stream o informazioni su una funzione specifica.</span><span class="sxs-lookup"><span data-stu-id="46404-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="46404-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46404-107">EXAMPLES</span></span>

### <span data-ttu-id="46404-108">Esempio 1: ottenere tutte le funzioni di analisi dello stream</span><span class="sxs-lookup"><span data-stu-id="46404-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="46404-109">Questo comando consente di ottenere le funzioni definite nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="46404-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="46404-110">Esempio 2: ottenere una specifica funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="46404-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="46404-111">Questo comando ottiene le informazioni sulla funzione denominata ScoreTweet definita nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="46404-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="46404-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46404-112">PARAMETERS</span></span>

### <span data-ttu-id="46404-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="46404-113">-JobName</span></span>
<span data-ttu-id="46404-114">Specifica il nome del processo di analisi del flusso a cui appartengono le funzioni.</span><span class="sxs-lookup"><span data-stu-id="46404-114">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="46404-115">Questo cmdlet ottiene le funzioni per il processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="46404-115">This cmdlet gets functions for the job that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46404-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="46404-116">-Name</span></span>
<span data-ttu-id="46404-117">Specifica il nome della funzione flusso di analisi che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="46404-117">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46404-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46404-118">-ResourceGroupName</span></span>
<span data-ttu-id="46404-119">Specifica il nome del gruppo di risorse a cui appartiene le funzioni di analisi flusso.</span><span class="sxs-lookup"><span data-stu-id="46404-119">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="46404-120">Questo cmdlet ottiene le funzioni per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="46404-120">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="46404-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46404-121">-DefaultProfile</span></span>
<span data-ttu-id="46404-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46404-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46404-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46404-123">CommonParameters</span></span>
<span data-ttu-id="46404-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46404-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46404-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46404-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46404-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46404-126">INPUTS</span></span>

## <span data-ttu-id="46404-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46404-127">OUTPUTS</span></span>

### <span data-ttu-id="46404-128">System. Collections. Generic. list [Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction, Microsoft. Azure. Commands. StreamAnalytics], Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="46404-128">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="46404-129">Note</span><span class="sxs-lookup"><span data-stu-id="46404-129">NOTES</span></span>

## <span data-ttu-id="46404-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46404-130">RELATED LINKS</span></span>

[<span data-ttu-id="46404-131">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="46404-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="46404-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="46404-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="46404-133">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="46404-133">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


