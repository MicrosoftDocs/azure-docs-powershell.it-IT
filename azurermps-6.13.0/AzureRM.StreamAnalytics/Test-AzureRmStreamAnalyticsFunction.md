---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: c62d829da193ae36f10a64149260cf34c6bc20ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520569"
---
# <span data-ttu-id="bbecc-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bbecc-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="bbecc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbecc-102">SYNOPSIS</span></span>
<span data-ttu-id="bbecc-103">Verifica se il flusso di analisi può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="bbecc-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbecc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbecc-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbecc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbecc-105">DESCRIPTION</span></span>
<span data-ttu-id="bbecc-106">Il cmdlet **test-AzureRmStreamAnalyticsFunction** verifica se l'analisi di Azure Stream può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="bbecc-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="bbecc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbecc-107">EXAMPLES</span></span>

### <span data-ttu-id="bbecc-108">Esempio 1: testare una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="bbecc-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="bbecc-109">Questo comando verifica lo stato di connessione della funzione denominata ScoreTweet nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="bbecc-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="bbecc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbecc-110">PARAMETERS</span></span>

### <span data-ttu-id="bbecc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbecc-111">-DefaultProfile</span></span>
<span data-ttu-id="bbecc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbecc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbecc-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="bbecc-113">-JobName</span></span>
<span data-ttu-id="bbecc-114">Specifica il nome del processo di analisi del flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="bbecc-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="bbecc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbecc-115">-Name</span></span>
<span data-ttu-id="bbecc-116">Specifica il nome della funzione analisi flusso che questo cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="bbecc-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="bbecc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbecc-117">-ResourceGroupName</span></span>
<span data-ttu-id="bbecc-118">Specifica il nome del gruppo di risorse a cui appartiene una funzione di analisi dello stream.</span><span class="sxs-lookup"><span data-stu-id="bbecc-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="bbecc-119">Questo cmdlet verifica una funzione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bbecc-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbecc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbecc-120">CommonParameters</span></span>
<span data-ttu-id="bbecc-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbecc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbecc-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbecc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbecc-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbecc-123">INPUTS</span></span>

### <span data-ttu-id="bbecc-124">System. String</span><span class="sxs-lookup"><span data-stu-id="bbecc-124">System.String</span></span>

## <span data-ttu-id="bbecc-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbecc-125">OUTPUTS</span></span>

### <span data-ttu-id="bbecc-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbecc-126">System.Boolean</span></span>

## <span data-ttu-id="bbecc-127">Note</span><span class="sxs-lookup"><span data-stu-id="bbecc-127">NOTES</span></span>

## <span data-ttu-id="bbecc-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbecc-128">RELATED LINKS</span></span>

[<span data-ttu-id="bbecc-129">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bbecc-129">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="bbecc-130">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bbecc-130">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="bbecc-131">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bbecc-131">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


