---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350872"
---
# <span data-ttu-id="88955-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="88955-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="88955-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88955-102">SYNOPSIS</span></span>
<span data-ttu-id="88955-103">Creare un oggetto PSDiagnosticDetailSetting, digitare può essere Metric o log</span><span class="sxs-lookup"><span data-stu-id="88955-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="88955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88955-104">SYNTAX</span></span>

### <span data-ttu-id="88955-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="88955-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88955-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="88955-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88955-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88955-107">DESCRIPTION</span></span>
<span data-ttu-id="88955-108">Creare un oggetto PSMetricSettings o PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="88955-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="88955-109">Puoi ottenere le categorie usando `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="88955-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="88955-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88955-110">EXAMPLES</span></span>

### <span data-ttu-id="88955-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88955-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="88955-112">Creare un oggetto PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="88955-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="88955-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="88955-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="88955-114">Creare un oggetto PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="88955-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="88955-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88955-115">PARAMETERS</span></span>

### <span data-ttu-id="88955-116">-Categoria</span><span class="sxs-lookup"><span data-stu-id="88955-116">-Category</span></span>
<span data-ttu-id="88955-117">Categoria di impostazione</span><span class="sxs-lookup"><span data-stu-id="88955-117">Category of setting</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88955-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88955-118">-DefaultProfile</span></span>
<span data-ttu-id="88955-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88955-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88955-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="88955-120">-Enabled</span></span>
<span data-ttu-id="88955-121">Abilitare l'impostazione</span><span class="sxs-lookup"><span data-stu-id="88955-121">Enable the setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88955-122">-Log</span><span class="sxs-lookup"><span data-stu-id="88955-122">-Log</span></span>
<span data-ttu-id="88955-123">Per creare l'impostazione del log</span><span class="sxs-lookup"><span data-stu-id="88955-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88955-124">-Metrica</span><span class="sxs-lookup"><span data-stu-id="88955-124">-Metric</span></span>
<span data-ttu-id="88955-125">Per creare l'impostazione metrica</span><span class="sxs-lookup"><span data-stu-id="88955-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88955-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="88955-126">-RetentionEnabled</span></span>
<span data-ttu-id="88955-127">Abilitare i criteri di conservazione</span><span class="sxs-lookup"><span data-stu-id="88955-127">Enable Retention policy</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88955-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="88955-128">-RetentionInDays</span></span>
<span data-ttu-id="88955-129">Giorni di conservazione per i criteri di conservazione</span><span class="sxs-lookup"><span data-stu-id="88955-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88955-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="88955-130">-TimeGrain</span></span>
<span data-ttu-id="88955-131">TimeGrain per l'impostazione metrica</span><span class="sxs-lookup"><span data-stu-id="88955-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88955-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88955-132">CommonParameters</span></span>
<span data-ttu-id="88955-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88955-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88955-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88955-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88955-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88955-135">INPUTS</span></span>

### <span data-ttu-id="88955-136">System. String</span><span class="sxs-lookup"><span data-stu-id="88955-136">System.String</span></span>

## <span data-ttu-id="88955-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88955-137">OUTPUTS</span></span>

### <span data-ttu-id="88955-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="88955-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="88955-139">Note</span><span class="sxs-lookup"><span data-stu-id="88955-139">NOTES</span></span>

## <span data-ttu-id="88955-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88955-140">RELATED LINKS</span></span>
