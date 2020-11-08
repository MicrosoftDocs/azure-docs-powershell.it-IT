---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200613"
---
# <span data-ttu-id="ee1fe-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ee1fe-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="ee1fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1fe-103">Verifica lo stato di connessione di un input.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="ee1fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee1fe-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee1fe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee1fe-105">DESCRIPTION</span></span>
<span data-ttu-id="ee1fe-106">Il cmdlet **test-AzStreamAnalyticsInput** verifica la possibilità di una connessione di analisi dello stream a un input.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="ee1fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee1fe-107">EXAMPLES</span></span>

### <span data-ttu-id="ee1fe-108">Esempio 1: verificare lo stato di connessione di un flusso di input</span><span class="sxs-lookup"><span data-stu-id="ee1fe-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="ee1fe-109">Questo verifica lo stato di connessione dell'input EntryStream in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="ee1fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee1fe-110">PARAMETERS</span></span>

### <span data-ttu-id="ee1fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1fe-111">-DefaultProfile</span></span>
<span data-ttu-id="ee1fe-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee1fe-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="ee1fe-113">-JobName</span></span>
<span data-ttu-id="ee1fe-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ee1fe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee1fe-115">-Name</span></span>
<span data-ttu-id="ee1fe-116">Specifica il nome dell'input di analisi di Azure Stream da testare.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="ee1fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee1fe-118">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ee1fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1fe-119">CommonParameters</span></span>
<span data-ttu-id="ee1fe-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1fe-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1fe-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1fe-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee1fe-122">INPUTS</span></span>

### <span data-ttu-id="ee1fe-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ee1fe-123">System.String</span></span>

## <span data-ttu-id="ee1fe-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee1fe-124">OUTPUTS</span></span>

### <span data-ttu-id="ee1fe-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee1fe-125">System.Boolean</span></span>

## <span data-ttu-id="ee1fe-126">Note</span><span class="sxs-lookup"><span data-stu-id="ee1fe-126">NOTES</span></span>

## <span data-ttu-id="ee1fe-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee1fe-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee1fe-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ee1fe-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="ee1fe-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ee1fe-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="ee1fe-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ee1fe-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


