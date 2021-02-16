---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180150"
---
# <span data-ttu-id="71d6c-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="71d6c-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="71d6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="71d6c-103">Creare l'oggetto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="71d6c-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="71d6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71d6c-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d6c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71d6c-105">DESCRIPTION</span></span>
<span data-ttu-id="71d6c-106">Creare l'oggetto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="71d6c-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="71d6c-107">Può essere usato come parametro `-InputObject` per `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="71d6c-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="71d6c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71d6c-108">EXAMPLES</span></span>

### <span data-ttu-id="71d6c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71d6c-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="71d6c-110">Creare l'oggetto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="71d6c-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="71d6c-111">E crea un'impostazione diagnostica per la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71d6c-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="71d6c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71d6c-112">PARAMETERS</span></span>

### <span data-ttu-id="71d6c-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="71d6c-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="71d6c-114">Valore che indica se esportare (in ODS) in specifiche delle risorse (se presenti) o in Diagnostica Diagnostica Azure (impostazione predefinita, non presente)</span><span class="sxs-lookup"><span data-stu-id="71d6c-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d6c-115">-DefaultProfile</span></span>
<span data-ttu-id="71d6c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71d6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="71d6c-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="71d6c-118">ID regola dell'hub eventi</span><span class="sxs-lookup"><span data-stu-id="71d6c-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="71d6c-119">-EventHubName</span></span>
<span data-ttu-id="71d6c-120">ID regola bus di servizio</span><span class="sxs-lookup"><span data-stu-id="71d6c-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="71d6c-121">-Name</span></span>
<span data-ttu-id="71d6c-122">Nome dell'impostazione diagnostica.</span><span class="sxs-lookup"><span data-stu-id="71d6c-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="71d6c-123">L'impostazione predefinita è "servizio"</span><span class="sxs-lookup"><span data-stu-id="71d6c-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="71d6c-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="71d6c-125">ID regola bus di servizio</span><span class="sxs-lookup"><span data-stu-id="71d6c-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-126">-Setting</span><span class="sxs-lookup"><span data-stu-id="71d6c-126">-Setting</span></span>
<span data-ttu-id="71d6c-127">Impostazioni metriche o impostazioni del log</span><span class="sxs-lookup"><span data-stu-id="71d6c-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71d6c-128">-StorageAccountId</span></span>
<span data-ttu-id="71d6c-129">ID account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="71d6c-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="71d6c-130">-TargetResourceId</span></span>
<span data-ttu-id="71d6c-131">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="71d6c-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="71d6c-132">-WorkspaceId</span></span>
<span data-ttu-id="71d6c-133">ID della risorsa dell'area di lavoro Analisi log a cui inviare log/metriche</span><span class="sxs-lookup"><span data-stu-id="71d6c-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71d6c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d6c-134">CommonParameters</span></span>
<span data-ttu-id="71d6c-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d6c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d6c-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71d6c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d6c-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="71d6c-137">INPUTS</span></span>

### <span data-ttu-id="71d6c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="71d6c-138">System.String</span></span>

### <span data-ttu-id="71d6c-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71d6c-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="71d6c-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDimpostazioni iagnosticDetailSettings[]</span><span class="sxs-lookup"><span data-stu-id="71d6c-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="71d6c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71d6c-141">OUTPUTS</span></span>

### <span data-ttu-id="71d6c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="71d6c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="71d6c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="71d6c-143">NOTES</span></span>

## <span data-ttu-id="71d6c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71d6c-144">RELATED LINKS</span></span>
