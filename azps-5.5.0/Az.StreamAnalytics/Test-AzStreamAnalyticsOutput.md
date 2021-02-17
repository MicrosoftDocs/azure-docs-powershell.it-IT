---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69e9d06a790fa473a278e50e79ad90be93f0527c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182887"
---
# <span data-ttu-id="ce0bb-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ce0bb-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="ce0bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0bb-103">Verifica lo stato di connessione di un output.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="ce0bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce0bb-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce0bb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce0bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ce0bb-106">Il **cmdlet Test-AzStreamAnalyticsOutput** verifica la capacità di Stream Analytics di connettersi a un output.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="ce0bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce0bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ce0bb-108">Esempio 1: Verificare lo stato di connessione di un output</span><span class="sxs-lookup"><span data-stu-id="ce0bb-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="ce0bb-109">Questo test consente di testare lo stato di connessione dell'output in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="ce0bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce0bb-110">PARAMETERS</span></span>

### <span data-ttu-id="ce0bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0bb-111">-DefaultProfile</span></span>
<span data-ttu-id="ce0bb-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce0bb-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="ce0bb-113">-JobName</span></span>
<span data-ttu-id="ce0bb-114">Specifica il nome del processo di Analisi di flusso di Azure a cui appartiene l'output di Analisi di flusso di Azure desiderato.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="ce0bb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ce0bb-115">-Name</span></span>
<span data-ttu-id="ce0bb-116">Specifica il nome dell'output di Analisi di flusso di Azure da testare.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="ce0bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="ce0bb-118">Specifica il nome del gruppo di risorse a cui appartiene l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="ce0bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0bb-119">CommonParameters</span></span>
<span data-ttu-id="ce0bb-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0bb-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0bb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0bb-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce0bb-122">INPUTS</span></span>

### <span data-ttu-id="ce0bb-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ce0bb-123">System.String</span></span>

## <span data-ttu-id="ce0bb-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce0bb-124">OUTPUTS</span></span>

### <span data-ttu-id="ce0bb-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce0bb-125">System.Boolean</span></span>

## <span data-ttu-id="ce0bb-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce0bb-126">NOTES</span></span>

## <span data-ttu-id="ce0bb-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce0bb-127">RELATED LINKS</span></span>

[<span data-ttu-id="ce0bb-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ce0bb-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="ce0bb-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ce0bb-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="ce0bb-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="ce0bb-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


