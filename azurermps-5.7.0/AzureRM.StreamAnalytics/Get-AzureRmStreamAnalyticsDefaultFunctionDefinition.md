---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: bc04c78538e808ce67813a3d706c35817102cfc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512135"
---
# <span data-ttu-id="cba75-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="cba75-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="cba75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cba75-102">SYNOPSIS</span></span>
<span data-ttu-id="cba75-103">Ottiene la definizione predefinita di una funzione in flusso di analisi.</span><span class="sxs-lookup"><span data-stu-id="cba75-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cba75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cba75-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba75-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cba75-105">DESCRIPTION</span></span>
<span data-ttu-id="cba75-106">Il cmdlet **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** ottiene la definizione predefinita di una funzione in Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="cba75-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="cba75-107">Puoi usare la definizione predefinita e il cmdlet New-AzureRmStreamAnalyticsFunction per creare una funzione.</span><span class="sxs-lookup"><span data-stu-id="cba75-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="cba75-108">È possibile modificare la definizione predefinita prima di creare una funzione.</span><span class="sxs-lookup"><span data-stu-id="cba75-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="cba75-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cba75-109">EXAMPLES</span></span>

### <span data-ttu-id="cba75-110">Esempio 1: ottenere la definizione predefinita di una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="cba75-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="cba75-111">Questo comando ottiene la definizione predefinita della funzione denominata ScoreTweet usando i parametri specificati nella RetrieveDefaultDefinitionRequest.jssu file.</span><span class="sxs-lookup"><span data-stu-id="cba75-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="cba75-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cba75-112">PARAMETERS</span></span>

### <span data-ttu-id="cba75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba75-113">-DefaultProfile</span></span>
<span data-ttu-id="cba75-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cba75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba75-115">-File</span><span class="sxs-lookup"><span data-stu-id="cba75-115">-File</span></span>
<span data-ttu-id="cba75-116">Specifica il percorso di un file con estensione JSON che contiene la rappresentazione JSON (JavaScript Object Notation) del corpo della richiesta per la richiesta di definizione della funzione recupera predefinita.</span><span class="sxs-lookup"><span data-stu-id="cba75-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba75-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="cba75-117">-JobName</span></span>
<span data-ttu-id="cba75-118">Specifica il nome del processo di analisi del flusso a cui appartengono le funzioni.</span><span class="sxs-lookup"><span data-stu-id="cba75-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="cba75-119">Questo cmdlet ottiene la definizione predefinita per una funzione nel processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cba75-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba75-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cba75-120">-Name</span></span>
<span data-ttu-id="cba75-121">Specifica il nome della funzione analisi flusso per cui questo cmdlet ottiene la definizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cba75-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba75-122">-ResourceGroupName</span></span>
<span data-ttu-id="cba75-123">Specifica il nome del gruppo di risorse a cui appartiene le funzioni di analisi flusso.</span><span class="sxs-lookup"><span data-stu-id="cba75-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="cba75-124">Questo cmdlet ottiene una definizione di funzione per il gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cba75-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba75-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba75-125">CommonParameters</span></span>
<span data-ttu-id="cba75-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba75-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba75-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cba75-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba75-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cba75-128">INPUTS</span></span>

### <span data-ttu-id="cba75-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cba75-129">None</span></span>
<span data-ttu-id="cba75-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="cba75-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cba75-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cba75-131">OUTPUTS</span></span>

### <span data-ttu-id="cba75-132">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="cba75-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="cba75-133">Note</span><span class="sxs-lookup"><span data-stu-id="cba75-133">NOTES</span></span>

## <span data-ttu-id="cba75-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cba75-134">RELATED LINKS</span></span>

[<span data-ttu-id="cba75-135">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="cba75-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


