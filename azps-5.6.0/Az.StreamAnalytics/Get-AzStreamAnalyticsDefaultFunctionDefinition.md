---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: c900973947418ebfb1eba3b503fc40a9f81a68ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973966"
---
# <span data-ttu-id="441e2-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="441e2-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="441e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="441e2-102">SYNOPSIS</span></span>
<span data-ttu-id="441e2-103">Ottiene la definizione predefinita di una funzione in Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="441e2-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="441e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="441e2-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="441e2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="441e2-105">DESCRIPTION</span></span>
<span data-ttu-id="441e2-106">Il cmdlet **Get-AzStreamAnalyticsDefaultFunctionDefinition** ottiene la definizione predefinita di una funzione in Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="441e2-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="441e2-107">È possibile usare la definizione predefinita e il cmdlet New-AzStreamAnalyticsFunction per creare una funzione.</span><span class="sxs-lookup"><span data-stu-id="441e2-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="441e2-108">È possibile modificare la definizione predefinita prima di creare una funzione.</span><span class="sxs-lookup"><span data-stu-id="441e2-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="441e2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="441e2-109">EXAMPLES</span></span>

### <span data-ttu-id="441e2-110">Esempio 1: Ottenere la definizione predefinita di una funzione di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="441e2-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="441e2-111">Questo comando ottiene la definizione predefinita della funzione denominata ScoreTweet usando i parametri specificati nella RetrieveDefaultDefinitionRequest.jssul file.</span><span class="sxs-lookup"><span data-stu-id="441e2-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="441e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="441e2-112">PARAMETERS</span></span>

### <span data-ttu-id="441e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441e2-113">-DefaultProfile</span></span>
<span data-ttu-id="441e2-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="441e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="441e2-115">-File</span><span class="sxs-lookup"><span data-stu-id="441e2-115">-File</span></span>
<span data-ttu-id="441e2-116">Specifica il percorso di un file JSON che contiene la rappresentazione JSON (JavaScript Object Notation) del corpo della richiesta per la richiesta di definizione della funzione predefinita.</span><span class="sxs-lookup"><span data-stu-id="441e2-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441e2-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="441e2-117">-JobName</span></span>
<span data-ttu-id="441e2-118">Specifica il nome del processo di Analisi di flusso a cui appartengono le funzioni.</span><span class="sxs-lookup"><span data-stu-id="441e2-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="441e2-119">Questo cmdlet ottiene la definizione predefinita per una funzione nel processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="441e2-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="441e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="441e2-120">-Name</span></span>
<span data-ttu-id="441e2-121">Specifica il nome della funzione Di analisi di flusso per cui questo cmdlet ottiene la definizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="441e2-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="441e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="441e2-123">Specifica il nome del gruppo di risorse a cui appartengono le funzioni di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="441e2-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="441e2-124">Questo cmdlet ottiene una definizione di funzione per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="441e2-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="441e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441e2-125">CommonParameters</span></span>
<span data-ttu-id="441e2-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="441e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441e2-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="441e2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441e2-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="441e2-128">INPUTS</span></span>

### <span data-ttu-id="441e2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="441e2-129">System.String</span></span>

## <span data-ttu-id="441e2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="441e2-130">OUTPUTS</span></span>

### <span data-ttu-id="441e2-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="441e2-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="441e2-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="441e2-132">NOTES</span></span>

## <span data-ttu-id="441e2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="441e2-133">RELATED LINKS</span></span>

[<span data-ttu-id="441e2-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="441e2-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


