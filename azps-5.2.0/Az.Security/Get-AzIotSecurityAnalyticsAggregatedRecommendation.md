---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369722"
---
# <span data-ttu-id="3681c-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="3681c-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="3681c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3681c-102">SYNOPSIS</span></span>
<span data-ttu-id="3681c-103">Suggerimenti per la sicurezza aggregati</span><span class="sxs-lookup"><span data-stu-id="3681c-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="3681c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3681c-104">SYNTAX</span></span>

### <span data-ttu-id="3681c-105">SolutionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3681c-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3681c-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3681c-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3681c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3681c-107">DESCRIPTION</span></span>
<span data-ttu-id="3681c-108">Il cmdlet Get-AzIotSecurityAnalyticsAggregatedAlert restituisce uno o più suggerimenti aggregati nei dispositivi di hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="3681c-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="3681c-109">Il nome di una raccomandazione aggregata è il tipo</span><span class="sxs-lookup"><span data-stu-id="3681c-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="3681c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3681c-110">EXAMPLES</span></span>

### <span data-ttu-id="3681c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3681c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="3681c-112">Ottenere la raccomandazione aggregata "IoT_OpenPorts" in soluzione di sicurezza "soluzione" e gruppo risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="3681c-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="3681c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3681c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="3681c-114">Ottenere un elenco di suggerimenti aggregati nella soluzione di sicurezza "soluzione" e il gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="3681c-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="3681c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3681c-115">PARAMETERS</span></span>

### <span data-ttu-id="3681c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3681c-116">-DefaultProfile</span></span>
<span data-ttu-id="3681c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3681c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3681c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3681c-118">-Name</span></span>
<span data-ttu-id="3681c-119">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="3681c-119">Resource name.</span></span>

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

### <span data-ttu-id="3681c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3681c-120">-ResourceGroupName</span></span>
<span data-ttu-id="3681c-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3681c-121">Resource group name.</span></span>

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

### <span data-ttu-id="3681c-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="3681c-122">-SolutionName</span></span>
<span data-ttu-id="3681c-123">Nome soluzione</span><span class="sxs-lookup"><span data-stu-id="3681c-123">Solution name</span></span>

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

### <span data-ttu-id="3681c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3681c-124">CommonParameters</span></span>
<span data-ttu-id="3681c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3681c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3681c-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3681c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3681c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3681c-127">INPUTS</span></span>

### <span data-ttu-id="3681c-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3681c-128">None</span></span>

## <span data-ttu-id="3681c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3681c-129">OUTPUTS</span></span>

### <span data-ttu-id="3681c-130">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="3681c-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="3681c-131">Note</span><span class="sxs-lookup"><span data-stu-id="3681c-131">NOTES</span></span>

## <span data-ttu-id="3681c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3681c-132">RELATED LINKS</span></span>
