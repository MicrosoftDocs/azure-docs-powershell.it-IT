---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486400"
---
# <span data-ttu-id="37492-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="37492-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="37492-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37492-102">SYNOPSIS</span></span>
<span data-ttu-id="37492-103">Ottenere analisi della sicurezza degli altri</span><span class="sxs-lookup"><span data-stu-id="37492-103">Get IoT security analytics</span></span>

## <span data-ttu-id="37492-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37492-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37492-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37492-105">DESCRIPTION</span></span>
<span data-ttu-id="37492-106">Il cmdlet Get-AzIotSecurityAnalytics restituisce un set di analisi della sicurezza di una soluzione di sicurezza molto specifica</span><span class="sxs-lookup"><span data-stu-id="37492-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="37492-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37492-107">EXAMPLES</span></span>

### <span data-ttu-id="37492-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="37492-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="37492-109">Ottenere gli deafult Security Analytics per la soluzione di sicurezza "soluzione" nel gruppo risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="37492-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="37492-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37492-110">PARAMETERS</span></span>

### <span data-ttu-id="37492-111">-Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="37492-111">-Default</span></span>
<span data-ttu-id="37492-112">Se presente, ottenere il set di analisi predefinito, in caso contrario, ottenere l'elenco di tutti i set di analisi.</span><span class="sxs-lookup"><span data-stu-id="37492-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

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

### <span data-ttu-id="37492-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37492-113">-DefaultProfile</span></span>
<span data-ttu-id="37492-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37492-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37492-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37492-115">-ResourceGroupName</span></span>
<span data-ttu-id="37492-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="37492-116">Resource group name.</span></span>

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

### <span data-ttu-id="37492-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="37492-117">-SolutionName</span></span>
<span data-ttu-id="37492-118">Nome soluzione</span><span class="sxs-lookup"><span data-stu-id="37492-118">Solution name</span></span>

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

### <span data-ttu-id="37492-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37492-119">CommonParameters</span></span>
<span data-ttu-id="37492-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37492-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37492-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37492-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37492-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37492-122">INPUTS</span></span>

### <span data-ttu-id="37492-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="37492-123">None</span></span>

## <span data-ttu-id="37492-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37492-124">OUTPUTS</span></span>

### <span data-ttu-id="37492-125">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="37492-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="37492-126">Note</span><span class="sxs-lookup"><span data-stu-id="37492-126">NOTES</span></span>

## <span data-ttu-id="37492-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37492-127">RELATED LINKS</span></span>
