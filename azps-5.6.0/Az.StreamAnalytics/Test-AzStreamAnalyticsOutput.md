---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 28a595b3e63a01439417ed07f6fd47c1cfc40a79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981965"
---
# <span data-ttu-id="91e21-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="91e21-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="91e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e21-102">SYNOPSIS</span></span>
<span data-ttu-id="91e21-103">Verifica lo stato di connessione di un output.</span><span class="sxs-lookup"><span data-stu-id="91e21-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="91e21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91e21-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91e21-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="91e21-105">DESCRIPTION</span></span>
<span data-ttu-id="91e21-106">Il **cmdlet Test-AzStreamAnalyticsOutput** verifica la capacità di Stream Analytics di connettersi a un output.</span><span class="sxs-lookup"><span data-stu-id="91e21-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="91e21-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91e21-107">EXAMPLES</span></span>

### <span data-ttu-id="91e21-108">Esempio 1: Verificare lo stato di connessione di un output</span><span class="sxs-lookup"><span data-stu-id="91e21-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="91e21-109">Questo test consente di testare lo stato di connessione dell'output in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="91e21-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="91e21-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91e21-110">PARAMETERS</span></span>

### <span data-ttu-id="91e21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e21-111">-DefaultProfile</span></span>
<span data-ttu-id="91e21-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91e21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91e21-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="91e21-113">-JobName</span></span>
<span data-ttu-id="91e21-114">Specifica il nome del processo di Analisi di flusso di Azure a cui appartiene l'output di Analisi di flusso di Azure desiderato.</span><span class="sxs-lookup"><span data-stu-id="91e21-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="91e21-115">-Name</span><span class="sxs-lookup"><span data-stu-id="91e21-115">-Name</span></span>
<span data-ttu-id="91e21-116">Specifica il nome dell'output di Analisi di flusso di Azure da testare.</span><span class="sxs-lookup"><span data-stu-id="91e21-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="91e21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e21-117">-ResourceGroupName</span></span>
<span data-ttu-id="91e21-118">Specifica il nome del gruppo di risorse a cui appartiene l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="91e21-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="91e21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e21-119">CommonParameters</span></span>
<span data-ttu-id="91e21-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e21-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91e21-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e21-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="91e21-122">INPUTS</span></span>

### <span data-ttu-id="91e21-123">System.String</span><span class="sxs-lookup"><span data-stu-id="91e21-123">System.String</span></span>

## <span data-ttu-id="91e21-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91e21-124">OUTPUTS</span></span>

### <span data-ttu-id="91e21-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91e21-125">System.Boolean</span></span>

## <span data-ttu-id="91e21-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="91e21-126">NOTES</span></span>

## <span data-ttu-id="91e21-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91e21-127">RELATED LINKS</span></span>

[<span data-ttu-id="91e21-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="91e21-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="91e21-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="91e21-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="91e21-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="91e21-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


