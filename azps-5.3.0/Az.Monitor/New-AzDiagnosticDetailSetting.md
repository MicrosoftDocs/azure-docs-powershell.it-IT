---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475208"
---
# <span data-ttu-id="01d54-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="01d54-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="01d54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01d54-102">SYNOPSIS</span></span>
<span data-ttu-id="01d54-103">Creare un oggetto PSDiagnosticDetailSetting, digitare può essere Metric o log</span><span class="sxs-lookup"><span data-stu-id="01d54-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="01d54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01d54-104">SYNTAX</span></span>

### <span data-ttu-id="01d54-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d54-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01d54-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="01d54-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d54-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01d54-107">DESCRIPTION</span></span>
<span data-ttu-id="01d54-108">Creare un oggetto PSMetricSettings o PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="01d54-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="01d54-109">Puoi ottenere le categorie usando `Get-AzDiagnosticSettingCategory` .</span><span class="sxs-lookup"><span data-stu-id="01d54-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="01d54-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01d54-110">EXAMPLES</span></span>

### <span data-ttu-id="01d54-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="01d54-111">Example 1</span></span>
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

<span data-ttu-id="01d54-112">Creare un oggetto PSMetricSettings.</span><span class="sxs-lookup"><span data-stu-id="01d54-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="01d54-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="01d54-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="01d54-114">Creare un oggetto PSLogSettings.</span><span class="sxs-lookup"><span data-stu-id="01d54-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="01d54-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01d54-115">PARAMETERS</span></span>

### <span data-ttu-id="01d54-116">-Categoria</span><span class="sxs-lookup"><span data-stu-id="01d54-116">-Category</span></span>
<span data-ttu-id="01d54-117">Categoria di impostazione</span><span class="sxs-lookup"><span data-stu-id="01d54-117">Category of setting</span></span>

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

### <span data-ttu-id="01d54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d54-118">-DefaultProfile</span></span>
<span data-ttu-id="01d54-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01d54-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d54-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="01d54-120">-Enabled</span></span>
<span data-ttu-id="01d54-121">Abilitare l'impostazione</span><span class="sxs-lookup"><span data-stu-id="01d54-121">Enable the setting</span></span>

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

### <span data-ttu-id="01d54-122">-Log</span><span class="sxs-lookup"><span data-stu-id="01d54-122">-Log</span></span>
<span data-ttu-id="01d54-123">Per creare l'impostazione del log</span><span class="sxs-lookup"><span data-stu-id="01d54-123">To create log setting</span></span>

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

### <span data-ttu-id="01d54-124">-Metrica</span><span class="sxs-lookup"><span data-stu-id="01d54-124">-Metric</span></span>
<span data-ttu-id="01d54-125">Per creare l'impostazione metrica</span><span class="sxs-lookup"><span data-stu-id="01d54-125">To create metric setting</span></span>

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

### <span data-ttu-id="01d54-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="01d54-126">-RetentionEnabled</span></span>
<span data-ttu-id="01d54-127">Abilitare i criteri di conservazione</span><span class="sxs-lookup"><span data-stu-id="01d54-127">Enable Retention policy</span></span>

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

### <span data-ttu-id="01d54-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="01d54-128">-RetentionInDays</span></span>
<span data-ttu-id="01d54-129">Giorni di conservazione per i criteri di conservazione</span><span class="sxs-lookup"><span data-stu-id="01d54-129">Retention days for retention policy</span></span>

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

### <span data-ttu-id="01d54-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="01d54-130">-TimeGrain</span></span>
<span data-ttu-id="01d54-131">TimeGrain per l'impostazione metrica</span><span class="sxs-lookup"><span data-stu-id="01d54-131">TimeGrain for metric setting</span></span>

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

### <span data-ttu-id="01d54-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d54-132">CommonParameters</span></span>
<span data-ttu-id="01d54-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d54-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d54-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01d54-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d54-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01d54-135">INPUTS</span></span>

### <span data-ttu-id="01d54-136">System. String</span><span class="sxs-lookup"><span data-stu-id="01d54-136">System.String</span></span>

## <span data-ttu-id="01d54-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01d54-137">OUTPUTS</span></span>

### <span data-ttu-id="01d54-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="01d54-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="01d54-139">Note</span><span class="sxs-lookup"><span data-stu-id="01d54-139">NOTES</span></span>

## <span data-ttu-id="01d54-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01d54-140">RELATED LINKS</span></span>
