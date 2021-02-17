---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182902"
---
# <span data-ttu-id="90369-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="90369-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="90369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90369-102">SYNOPSIS</span></span>
<span data-ttu-id="90369-103">Verifica se Stream Analytics può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="90369-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="90369-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90369-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90369-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="90369-105">DESCRIPTION</span></span>
<span data-ttu-id="90369-106">Il **cmdlet Test-AzStreamAnalyticsFunction** verifica se Azure Stream Analytics può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="90369-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="90369-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90369-107">EXAMPLES</span></span>

### <span data-ttu-id="90369-108">Esempio 1: Testare una funzione di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="90369-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="90369-109">Questo comando verifica lo stato di connessione della funzione denominata ScoreTweet nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="90369-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="90369-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90369-110">PARAMETERS</span></span>

### <span data-ttu-id="90369-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90369-111">-DefaultProfile</span></span>
<span data-ttu-id="90369-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90369-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90369-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="90369-113">-JobName</span></span>
<span data-ttu-id="90369-114">Specifica il nome del processo di Analisi di flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="90369-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="90369-115">-Name</span><span class="sxs-lookup"><span data-stu-id="90369-115">-Name</span></span>
<span data-ttu-id="90369-116">Specifica il nome della funzione Analisi di flusso testata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90369-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="90369-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90369-117">-ResourceGroupName</span></span>
<span data-ttu-id="90369-118">Specifica il nome del gruppo di risorse a cui appartiene una funzione di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="90369-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="90369-119">Questo cmdlet verifica una funzione nel gruppo di risorse specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="90369-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="90369-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90369-120">CommonParameters</span></span>
<span data-ttu-id="90369-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90369-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90369-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90369-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90369-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="90369-123">INPUTS</span></span>

### <span data-ttu-id="90369-124">System.String</span><span class="sxs-lookup"><span data-stu-id="90369-124">System.String</span></span>

## <span data-ttu-id="90369-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90369-125">OUTPUTS</span></span>

### <span data-ttu-id="90369-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90369-126">System.Boolean</span></span>

## <span data-ttu-id="90369-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="90369-127">NOTES</span></span>

## <span data-ttu-id="90369-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90369-128">RELATED LINKS</span></span>

[<span data-ttu-id="90369-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="90369-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="90369-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="90369-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="90369-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="90369-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


