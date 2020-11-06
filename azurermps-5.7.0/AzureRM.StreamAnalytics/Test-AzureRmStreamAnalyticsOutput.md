---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519820"
---
# <span data-ttu-id="e6f39-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6f39-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="e6f39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6f39-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f39-103">Verifica lo stato di connessione di un output.</span><span class="sxs-lookup"><span data-stu-id="e6f39-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6f39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6f39-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6f39-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6f39-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f39-106">Il cmdlet **test-AzureRmStreamAnalyticsOutput** verifica la possibilità di una connessione di analisi dello stream a un output.</span><span class="sxs-lookup"><span data-stu-id="e6f39-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="e6f39-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6f39-107">EXAMPLES</span></span>

### <span data-ttu-id="e6f39-108">ESEMPIO 1: verificare lo stato di connessione di un output</span><span class="sxs-lookup"><span data-stu-id="e6f39-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="e6f39-109">Questo verifica lo stato di connessione dell'output di output in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="e6f39-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="e6f39-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6f39-110">PARAMETERS</span></span>

### <span data-ttu-id="e6f39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f39-111">-DefaultProfile</span></span>
<span data-ttu-id="e6f39-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f39-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="e6f39-113">-JobName</span></span>
<span data-ttu-id="e6f39-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'output di analisi di Azure Stream desiderato.</span><span class="sxs-lookup"><span data-stu-id="e6f39-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e6f39-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6f39-115">-Name</span></span>
<span data-ttu-id="e6f39-116">Specifica il nome dell'output di analisi di Azure Stream da testare.</span><span class="sxs-lookup"><span data-stu-id="e6f39-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="e6f39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f39-117">-ResourceGroupName</span></span>
<span data-ttu-id="e6f39-118">Specifica il nome del gruppo di risorse a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="e6f39-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="e6f39-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f39-119">CommonParameters</span></span>
<span data-ttu-id="e6f39-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f39-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f39-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f39-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f39-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6f39-122">INPUTS</span></span>

### <span data-ttu-id="e6f39-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6f39-123">None</span></span>
<span data-ttu-id="e6f39-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e6f39-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6f39-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6f39-125">OUTPUTS</span></span>

### <span data-ttu-id="e6f39-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="e6f39-126">System.Object</span></span>

## <span data-ttu-id="e6f39-127">Note</span><span class="sxs-lookup"><span data-stu-id="e6f39-127">NOTES</span></span>

## <span data-ttu-id="e6f39-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6f39-128">RELATED LINKS</span></span>

[<span data-ttu-id="e6f39-129">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6f39-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="e6f39-130">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6f39-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="e6f39-131">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="e6f39-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


