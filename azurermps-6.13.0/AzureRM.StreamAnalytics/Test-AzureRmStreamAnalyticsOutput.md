---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f8bd4feab9bdcf99daf713d3a584a574f699a8b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508992"
---
# <span data-ttu-id="c9b12-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c9b12-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c9b12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9b12-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b12-103">Verifica lo stato di connessione di un output.</span><span class="sxs-lookup"><span data-stu-id="c9b12-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9b12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9b12-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9b12-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9b12-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b12-106">Il cmdlet **test-AzureRmStreamAnalyticsOutput** verifica la possibilità di una connessione di analisi dello stream a un output.</span><span class="sxs-lookup"><span data-stu-id="c9b12-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="c9b12-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9b12-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b12-108">ESEMPIO 1: verificare lo stato di connessione di un output</span><span class="sxs-lookup"><span data-stu-id="c9b12-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c9b12-109">Questo verifica lo stato di connessione dell'output di output in StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c9b12-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="c9b12-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9b12-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b12-111">-DefaultProfile</span></span>
<span data-ttu-id="c9b12-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b12-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9b12-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="c9b12-113">-JobName</span></span>
<span data-ttu-id="c9b12-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'output di analisi di Azure Stream desiderato.</span><span class="sxs-lookup"><span data-stu-id="c9b12-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c9b12-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9b12-115">-Name</span></span>
<span data-ttu-id="c9b12-116">Specifica il nome dell'output di analisi di Azure Stream da testare.</span><span class="sxs-lookup"><span data-stu-id="c9b12-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="c9b12-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b12-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9b12-118">Specifica il nome del gruppo di risorse a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="c9b12-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c9b12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b12-119">CommonParameters</span></span>
<span data-ttu-id="c9b12-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b12-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b12-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b12-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9b12-122">INPUTS</span></span>

### <span data-ttu-id="c9b12-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c9b12-123">System.String</span></span>

## <span data-ttu-id="c9b12-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9b12-124">OUTPUTS</span></span>

### <span data-ttu-id="c9b12-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9b12-125">System.Boolean</span></span>

## <span data-ttu-id="c9b12-126">Note</span><span class="sxs-lookup"><span data-stu-id="c9b12-126">NOTES</span></span>

## <span data-ttu-id="c9b12-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9b12-127">RELATED LINKS</span></span>

[<span data-ttu-id="c9b12-128">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c9b12-128">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="c9b12-129">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c9b12-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="c9b12-130">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c9b12-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


