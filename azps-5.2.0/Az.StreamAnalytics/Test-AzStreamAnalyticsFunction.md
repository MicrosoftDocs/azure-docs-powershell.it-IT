---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366225"
---
# <span data-ttu-id="37597-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="37597-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="37597-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37597-102">SYNOPSIS</span></span>
<span data-ttu-id="37597-103">Verifica se il flusso di analisi può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="37597-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="37597-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37597-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37597-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37597-105">DESCRIPTION</span></span>
<span data-ttu-id="37597-106">Il cmdlet **test-AzStreamAnalyticsFunction** verifica se l'analisi di Azure Stream può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="37597-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="37597-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37597-107">EXAMPLES</span></span>

### <span data-ttu-id="37597-108">Esempio 1: testare una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="37597-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="37597-109">Questo comando verifica lo stato di connessione della funzione denominata ScoreTweet nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="37597-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="37597-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37597-110">PARAMETERS</span></span>

### <span data-ttu-id="37597-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37597-111">-DefaultProfile</span></span>
<span data-ttu-id="37597-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37597-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37597-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="37597-113">-JobName</span></span>
<span data-ttu-id="37597-114">Specifica il nome del processo di analisi del flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="37597-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="37597-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="37597-115">-Name</span></span>
<span data-ttu-id="37597-116">Specifica il nome della funzione analisi flusso che questo cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="37597-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="37597-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37597-117">-ResourceGroupName</span></span>
<span data-ttu-id="37597-118">Specifica il nome del gruppo di risorse a cui appartiene una funzione di analisi dello stream.</span><span class="sxs-lookup"><span data-stu-id="37597-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="37597-119">Questo cmdlet verifica una funzione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="37597-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="37597-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37597-120">CommonParameters</span></span>
<span data-ttu-id="37597-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37597-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37597-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37597-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37597-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37597-123">INPUTS</span></span>

### <span data-ttu-id="37597-124">System. String</span><span class="sxs-lookup"><span data-stu-id="37597-124">System.String</span></span>

## <span data-ttu-id="37597-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37597-125">OUTPUTS</span></span>

### <span data-ttu-id="37597-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37597-126">System.Boolean</span></span>

## <span data-ttu-id="37597-127">Note</span><span class="sxs-lookup"><span data-stu-id="37597-127">NOTES</span></span>

## <span data-ttu-id="37597-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37597-128">RELATED LINKS</span></span>

[<span data-ttu-id="37597-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="37597-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="37597-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="37597-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="37597-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="37597-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


