---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 70e63723bd9647f003082813cd680a84ae5638c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987921"
---
# <span data-ttu-id="570e5-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="570e5-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="570e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="570e5-102">SYNOPSIS</span></span>
<span data-ttu-id="570e5-103">Ottiene le metriche di quota per un iotHub.</span><span class="sxs-lookup"><span data-stu-id="570e5-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="570e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="570e5-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="570e5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="570e5-105">DESCRIPTION</span></span>
<span data-ttu-id="570e5-106">Ottiene le metriche di quota per un iotHub.</span><span class="sxs-lookup"><span data-stu-id="570e5-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="570e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="570e5-107">EXAMPLES</span></span>

### <span data-ttu-id="570e5-108">Esempio 1: Ottenere le metriche di quota</span><span class="sxs-lookup"><span data-stu-id="570e5-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="570e5-109">Recupera le informazioni sulla metrica quota per i dati di IotHub denominati "myiothub"</span><span class="sxs-lookup"><span data-stu-id="570e5-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="570e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="570e5-110">PARAMETERS</span></span>

### <span data-ttu-id="570e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="570e5-111">-DefaultProfile</span></span>
<span data-ttu-id="570e5-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="570e5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="570e5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="570e5-113">-Name</span></span>
<span data-ttu-id="570e5-114">Nome dell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="570e5-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="570e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="570e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="570e5-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="570e5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="570e5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="570e5-117">CommonParameters</span></span>
<span data-ttu-id="570e5-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="570e5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="570e5-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="570e5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="570e5-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="570e5-120">INPUTS</span></span>

### <span data-ttu-id="570e5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="570e5-121">System.String</span></span>

## <span data-ttu-id="570e5-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="570e5-122">OUTPUTS</span></span>

### <span data-ttu-id="570e5-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="570e5-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="570e5-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="570e5-124">NOTES</span></span>

## <span data-ttu-id="570e5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="570e5-125">RELATED LINKS</span></span>
