---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 29002234ac769ffd46aa3ca338e5ce61f0e3b848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509544"
---
# <span data-ttu-id="83cc8-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83cc8-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="83cc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="83cc8-103">Verifica se il flusso di analisi può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="83cc8-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83cc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83cc8-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83cc8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="83cc8-106">Il cmdlet **test-AzureRmStreamAnalyticsFunction** verifica se l'analisi di Azure Stream può connettersi a una funzione.</span><span class="sxs-lookup"><span data-stu-id="83cc8-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="83cc8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83cc8-107">EXAMPLES</span></span>

### <span data-ttu-id="83cc8-108">Esempio 1: testare una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="83cc8-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="83cc8-109">Questo comando verifica lo stato di connessione della funzione denominata ScoreTweet nel processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="83cc8-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="83cc8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83cc8-110">PARAMETERS</span></span>

### <span data-ttu-id="83cc8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83cc8-111">-DefaultProfile</span></span>
<span data-ttu-id="83cc8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83cc8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83cc8-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="83cc8-113">-JobName</span></span>
<span data-ttu-id="83cc8-114">Specifica il nome del processo di analisi del flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="83cc8-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="83cc8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="83cc8-115">-Name</span></span>
<span data-ttu-id="83cc8-116">Specifica il nome della funzione analisi flusso che questo cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="83cc8-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="83cc8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83cc8-117">-ResourceGroupName</span></span>
<span data-ttu-id="83cc8-118">Specifica il nome del gruppo di risorse a cui appartiene una funzione di analisi dello stream.</span><span class="sxs-lookup"><span data-stu-id="83cc8-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="83cc8-119">Questo cmdlet verifica una funzione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="83cc8-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="83cc8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83cc8-120">CommonParameters</span></span>
<span data-ttu-id="83cc8-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83cc8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83cc8-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83cc8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83cc8-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83cc8-123">INPUTS</span></span>

### <span data-ttu-id="83cc8-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="83cc8-124">None</span></span>
<span data-ttu-id="83cc8-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="83cc8-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83cc8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83cc8-126">OUTPUTS</span></span>

### <span data-ttu-id="83cc8-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="83cc8-127">System.Object</span></span>

## <span data-ttu-id="83cc8-128">Note</span><span class="sxs-lookup"><span data-stu-id="83cc8-128">NOTES</span></span>

## <span data-ttu-id="83cc8-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83cc8-129">RELATED LINKS</span></span>

[<span data-ttu-id="83cc8-130">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83cc8-130">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="83cc8-131">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83cc8-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="83cc8-132">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="83cc8-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


