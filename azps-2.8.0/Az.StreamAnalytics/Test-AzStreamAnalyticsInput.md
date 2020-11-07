---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: b19a8359f3267d848d475028fe0cee2123949f7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856006"
---
# <span data-ttu-id="3afad-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3afad-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="3afad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3afad-102">SYNOPSIS</span></span>
<span data-ttu-id="3afad-103">Verifica lo stato di connessione di un input.</span><span class="sxs-lookup"><span data-stu-id="3afad-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="3afad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3afad-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3afad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3afad-105">DESCRIPTION</span></span>
<span data-ttu-id="3afad-106">Il cmdlet **test-AzStreamAnalyticsInput** verifica la possibilità di una connessione di analisi dello stream a un input.</span><span class="sxs-lookup"><span data-stu-id="3afad-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="3afad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3afad-107">EXAMPLES</span></span>

### <span data-ttu-id="3afad-108">ESEMPIO 1: verificare lo stato di connessione di un flusso di input</span><span class="sxs-lookup"><span data-stu-id="3afad-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="3afad-109">Questo verifica lo stato di connessione dell'input EntryStream in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="3afad-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="3afad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3afad-110">PARAMETERS</span></span>

### <span data-ttu-id="3afad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3afad-111">-DefaultProfile</span></span>
<span data-ttu-id="3afad-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3afad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3afad-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="3afad-113">-JobName</span></span>
<span data-ttu-id="3afad-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="3afad-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="3afad-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3afad-115">-Name</span></span>
<span data-ttu-id="3afad-116">Specifica il nome dell'input di analisi di Azure Stream da testare.</span><span class="sxs-lookup"><span data-stu-id="3afad-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="3afad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3afad-117">-ResourceGroupName</span></span>
<span data-ttu-id="3afad-118">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="3afad-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="3afad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3afad-119">CommonParameters</span></span>
<span data-ttu-id="3afad-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3afad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3afad-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3afad-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3afad-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3afad-122">INPUTS</span></span>

### <span data-ttu-id="3afad-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3afad-123">System.String</span></span>

## <span data-ttu-id="3afad-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3afad-124">OUTPUTS</span></span>

### <span data-ttu-id="3afad-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3afad-125">System.Boolean</span></span>

## <span data-ttu-id="3afad-126">Note</span><span class="sxs-lookup"><span data-stu-id="3afad-126">NOTES</span></span>

## <span data-ttu-id="3afad-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3afad-127">RELATED LINKS</span></span>

[<span data-ttu-id="3afad-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3afad-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3afad-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3afad-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3afad-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3afad-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


