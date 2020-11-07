---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: f9139514850fe9d538c58d14813e91d2d24de502
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676387"
---
# <span data-ttu-id="95037-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95037-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="95037-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95037-102">SYNOPSIS</span></span>
<span data-ttu-id="95037-103">Verifica se il flusso di analisi può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="95037-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="95037-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95037-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95037-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95037-105">DESCRIPTION</span></span>
<span data-ttu-id="95037-106">Il cmdlet **test-AzStreamAnalyticsFunction** verifica se l'analisi di Azure Stream può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="95037-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="95037-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95037-107">EXAMPLES</span></span>

### <span data-ttu-id="95037-108">Esempio 1: testare una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="95037-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="95037-109">Questo comando verifica lo stato di connessione della funzione denominata ScoreTweet nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="95037-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="95037-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95037-110">PARAMETERS</span></span>

### <span data-ttu-id="95037-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95037-111">-DefaultProfile</span></span>
<span data-ttu-id="95037-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95037-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95037-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="95037-113">-JobName</span></span>
<span data-ttu-id="95037-114">Specifica il nome del processo di analisi del flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="95037-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="95037-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="95037-115">-Name</span></span>
<span data-ttu-id="95037-116">Specifica il nome della funzione analisi flusso che questo cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="95037-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="95037-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95037-117">-ResourceGroupName</span></span>
<span data-ttu-id="95037-118">Specifica il nome del gruppo di risorse a cui appartiene una funzione di analisi dello stream.</span><span class="sxs-lookup"><span data-stu-id="95037-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="95037-119">Questo cmdlet verifica una funzione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="95037-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="95037-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95037-120">CommonParameters</span></span>
<span data-ttu-id="95037-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95037-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95037-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95037-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95037-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95037-123">INPUTS</span></span>

### <span data-ttu-id="95037-124">System. String</span><span class="sxs-lookup"><span data-stu-id="95037-124">System.String</span></span>

## <span data-ttu-id="95037-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95037-125">OUTPUTS</span></span>

### <span data-ttu-id="95037-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95037-126">System.Boolean</span></span>

## <span data-ttu-id="95037-127">Note</span><span class="sxs-lookup"><span data-stu-id="95037-127">NOTES</span></span>

## <span data-ttu-id="95037-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95037-128">RELATED LINKS</span></span>

[<span data-ttu-id="95037-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95037-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="95037-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95037-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="95037-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="95037-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


