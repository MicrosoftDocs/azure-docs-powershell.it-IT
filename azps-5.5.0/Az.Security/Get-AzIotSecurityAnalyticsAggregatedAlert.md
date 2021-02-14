---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176358"
---
# <span data-ttu-id="e3d71-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e3d71-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="e3d71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d71-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d71-103">Ricevere un avviso di sicurezza aggregato IoT</span><span class="sxs-lookup"><span data-stu-id="e3d71-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="e3d71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3d71-104">SYNTAX</span></span>

### <span data-ttu-id="e3d71-105">SolutionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3d71-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3d71-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e3d71-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3d71-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3d71-107">DESCRIPTION</span></span>
<span data-ttu-id="e3d71-108">Il Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet restituisce uno o più avvisi aggregati nei dispositivi dell'hub iot.</span><span class="sxs-lookup"><span data-stu-id="e3d71-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="e3d71-109">Il nome degli avvisi aggregati è una combinazione del tipo di avviso e della data dell'avviso, separati da "/".</span><span class="sxs-lookup"><span data-stu-id="e3d71-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="e3d71-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3d71-110">EXAMPLES</span></span>

### <span data-ttu-id="e3d71-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3d71-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="e3d71-112">Ottenere l'avviso aggregato "IoT_Bruteforce_Fail/2019-02-02" (il nome combinato dal tipo di avviso e dalla data aggregata) nella soluzione "MySolution" e nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e3d71-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e3d71-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e3d71-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="e3d71-114">Ottenere un elenco di tutti gli avvisi aggregati nella soluzione "MySolution" e nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="e3d71-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e3d71-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3d71-115">PARAMETERS</span></span>

### <span data-ttu-id="e3d71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d71-116">-DefaultProfile</span></span>
<span data-ttu-id="e3d71-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d71-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d71-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3d71-118">-Name</span></span>
<span data-ttu-id="e3d71-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3d71-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d71-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3d71-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3d71-121">Resource group name.</span></span>

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

### <span data-ttu-id="e3d71-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="e3d71-122">-SolutionName</span></span>
<span data-ttu-id="e3d71-123">Nome della soluzione</span><span class="sxs-lookup"><span data-stu-id="e3d71-123">Solution name</span></span>

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

### <span data-ttu-id="e3d71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d71-124">CommonParameters</span></span>
<span data-ttu-id="e3d71-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d71-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3d71-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d71-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3d71-127">INPUTS</span></span>

### <span data-ttu-id="e3d71-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3d71-128">None</span></span>

## <span data-ttu-id="e3d71-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3d71-129">OUTPUTS</span></span>

### <span data-ttu-id="e3d71-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e3d71-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="e3d71-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3d71-131">NOTES</span></span>

## <span data-ttu-id="e3d71-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3d71-132">RELATED LINKS</span></span>
