---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: 8fa796b9b8940662c091e160cea55235816a29d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476079"
---
# <span data-ttu-id="2a290-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="2a290-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="2a290-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a290-102">SYNOPSIS</span></span>
<span data-ttu-id="2a290-103">Creare un oggetto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="2a290-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="2a290-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a290-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a290-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a290-105">DESCRIPTION</span></span>
<span data-ttu-id="2a290-106">Creare un oggetto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="2a290-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="2a290-107">Può essere usato come parametro `-InputObject` per `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="2a290-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="2a290-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a290-108">EXAMPLES</span></span>

### <span data-ttu-id="2a290-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a290-109">Example 1</span></span>
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

<span data-ttu-id="2a290-110">Creare un oggetto PSServiceDiagnosticSettings.</span><span class="sxs-lookup"><span data-stu-id="2a290-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="2a290-111">E crea l'impostazione di diagnostica per la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2a290-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="2a290-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a290-112">PARAMETERS</span></span>

### <span data-ttu-id="2a290-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="2a290-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="2a290-114">Valore che indica se esportare (in ODS) in specifiche delle risorse (se presenti) o in AzureDiagnostics (impostazione predefinita, non presente)</span><span class="sxs-lookup"><span data-stu-id="2a290-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

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

### <span data-ttu-id="2a290-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a290-115">-DefaultProfile</span></span>
<span data-ttu-id="2a290-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a290-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a290-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="2a290-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="2a290-118">ID regola dell'hub eventi</span><span class="sxs-lookup"><span data-stu-id="2a290-118">The event hub rule id</span></span>

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

### <span data-ttu-id="2a290-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="2a290-119">-EventHubName</span></span>
<span data-ttu-id="2a290-120">ID regola del bus di servizio</span><span class="sxs-lookup"><span data-stu-id="2a290-120">The service bus rule id</span></span>

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

### <span data-ttu-id="2a290-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a290-121">-Name</span></span>
<span data-ttu-id="2a290-122">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="2a290-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="2a290-123">Il valore predefinito è "servizio"</span><span class="sxs-lookup"><span data-stu-id="2a290-123">Defaults to 'service'</span></span>

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

### <span data-ttu-id="2a290-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="2a290-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="2a290-125">ID regola del bus di servizio</span><span class="sxs-lookup"><span data-stu-id="2a290-125">The service bus rule id</span></span>

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

### <span data-ttu-id="2a290-126">-Impostazione</span><span class="sxs-lookup"><span data-stu-id="2a290-126">-Setting</span></span>
<span data-ttu-id="2a290-127">Impostazioni metriche o Impostazioni log</span><span class="sxs-lookup"><span data-stu-id="2a290-127">Metric settings or Log settings</span></span>

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

### <span data-ttu-id="2a290-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2a290-128">-StorageAccountId</span></span>
<span data-ttu-id="2a290-129">ID account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2a290-129">The storage account id</span></span>

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

### <span data-ttu-id="2a290-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2a290-130">-TargetResourceId</span></span>
<span data-ttu-id="2a290-131">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="2a290-131">The resource id</span></span>

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

### <span data-ttu-id="2a290-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="2a290-132">-WorkspaceId</span></span>
<span data-ttu-id="2a290-133">ID risorsa dell'area di lavoro analisi log per l'invio di registri/metriche a</span><span class="sxs-lookup"><span data-stu-id="2a290-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="2a290-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a290-134">CommonParameters</span></span>
<span data-ttu-id="2a290-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a290-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a290-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a290-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a290-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a290-137">INPUTS</span></span>

### <span data-ttu-id="2a290-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2a290-138">System.String</span></span>

### <span data-ttu-id="2a290-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a290-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2a290-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings []</span><span class="sxs-lookup"><span data-stu-id="2a290-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="2a290-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a290-141">OUTPUTS</span></span>

### <span data-ttu-id="2a290-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="2a290-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="2a290-143">Note</span><span class="sxs-lookup"><span data-stu-id="2a290-143">NOTES</span></span>

## <span data-ttu-id="2a290-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a290-144">RELATED LINKS</span></span>
