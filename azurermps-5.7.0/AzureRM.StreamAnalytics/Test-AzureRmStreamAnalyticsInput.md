---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 34e1c2813292801d29a93a6914abf11b2725ec14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509539"
---
# <span data-ttu-id="b790c-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b790c-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="b790c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b790c-102">SYNOPSIS</span></span>
<span data-ttu-id="b790c-103">Verifica lo stato di connessione di un input.</span><span class="sxs-lookup"><span data-stu-id="b790c-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b790c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b790c-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b790c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b790c-105">DESCRIPTION</span></span>
<span data-ttu-id="b790c-106">Il cmdlet **test-AzureRmStreamAnalyticsInput** verifica la possibilità di una connessione di analisi dello stream a un input.</span><span class="sxs-lookup"><span data-stu-id="b790c-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="b790c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b790c-107">EXAMPLES</span></span>

### <span data-ttu-id="b790c-108">ESEMPIO 1: verificare lo stato di connessione di un flusso di input</span><span class="sxs-lookup"><span data-stu-id="b790c-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="b790c-109">Questo verifica lo stato di connessione dell'input EntryStream in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b790c-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="b790c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b790c-110">PARAMETERS</span></span>

### <span data-ttu-id="b790c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b790c-111">-DefaultProfile</span></span>
<span data-ttu-id="b790c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b790c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b790c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b790c-113">-JobName</span></span>
<span data-ttu-id="b790c-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="b790c-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="b790c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b790c-115">-Name</span></span>
<span data-ttu-id="b790c-116">Specifica il nome dell'input di analisi di Azure Stream da testare.</span><span class="sxs-lookup"><span data-stu-id="b790c-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="b790c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b790c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b790c-118">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="b790c-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="b790c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b790c-119">CommonParameters</span></span>
<span data-ttu-id="b790c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b790c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b790c-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b790c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b790c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b790c-122">INPUTS</span></span>

### <span data-ttu-id="b790c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b790c-123">None</span></span>
<span data-ttu-id="b790c-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b790c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b790c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b790c-125">OUTPUTS</span></span>

### <span data-ttu-id="b790c-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="b790c-126">System.Object</span></span>

## <span data-ttu-id="b790c-127">Note</span><span class="sxs-lookup"><span data-stu-id="b790c-127">NOTES</span></span>

## <span data-ttu-id="b790c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b790c-128">RELATED LINKS</span></span>

[<span data-ttu-id="b790c-129">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b790c-129">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="b790c-130">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b790c-130">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="b790c-131">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b790c-131">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


