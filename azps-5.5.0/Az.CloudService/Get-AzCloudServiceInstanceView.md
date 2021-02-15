---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: 4ad5b8a7b4369a5a0dd2b5ccc883ddc561a40af5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200751"
---
# <span data-ttu-id="b17a9-101">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="b17a9-101">Get-AzCloudServiceInstanceView</span></span>

## <span data-ttu-id="b17a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b17a9-102">SYNOPSIS</span></span>
<span data-ttu-id="b17a9-103">Ottiene lo stato di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b17a9-103">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="b17a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b17a9-104">SYNTAX</span></span>

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b17a9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b17a9-105">DESCRIPTION</span></span>
<span data-ttu-id="b17a9-106">Ottiene lo stato di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b17a9-106">Gets the status of a cloud service.</span></span>

## <span data-ttu-id="b17a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b17a9-107">EXAMPLES</span></span>

### <span data-ttu-id="b17a9-108">Esempio 1: Ottenere la visualizzazione dell'istanza del servizio cloud</span><span class="sxs-lookup"><span data-stu-id="b17a9-108">Example 1: Get cloud service instance view</span></span>
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

<span data-ttu-id="b17a9-109">Questo cmdlet ottiene la visualizzazione dell'istanza del servizio cloud denominata ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b17a9-109">This cmdlet gets the instance view of the cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b17a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b17a9-110">PARAMETERS</span></span>

### <span data-ttu-id="b17a9-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b17a9-111">-CloudServiceName</span></span>
<span data-ttu-id="b17a9-112">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b17a9-112">Name of the cloud service.</span></span>

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

### <span data-ttu-id="b17a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b17a9-113">-DefaultProfile</span></span>
<span data-ttu-id="b17a9-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b17a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b17a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b17a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="b17a9-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b17a9-116">Name of the resource group.</span></span>

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

### <span data-ttu-id="b17a9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b17a9-117">-SubscriptionId</span></span>
<span data-ttu-id="b17a9-118">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b17a9-118">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b17a9-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b17a9-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b17a9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17a9-120">CommonParameters</span></span>
<span data-ttu-id="b17a9-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b17a9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17a9-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b17a9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17a9-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="b17a9-123">INPUTS</span></span>

## <span data-ttu-id="b17a9-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b17a9-124">OUTPUTS</span></span>

### <span data-ttu-id="b17a9-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="b17a9-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView</span></span>

## <span data-ttu-id="b17a9-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="b17a9-126">NOTES</span></span>

<span data-ttu-id="b17a9-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b17a9-127">ALIASES</span></span>

## <span data-ttu-id="b17a9-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b17a9-128">RELATED LINKS</span></span>

