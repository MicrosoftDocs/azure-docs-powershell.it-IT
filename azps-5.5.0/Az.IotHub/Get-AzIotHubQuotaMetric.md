---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185663"
---
# <span data-ttu-id="6d5aa-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="6d5aa-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="6d5aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5aa-103">Ottiene le metriche di quota per un iotHub.</span><span class="sxs-lookup"><span data-stu-id="6d5aa-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="6d5aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d5aa-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d5aa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d5aa-105">DESCRIPTION</span></span>
<span data-ttu-id="6d5aa-106">Ottiene le metriche di quota per un iotHub.</span><span class="sxs-lookup"><span data-stu-id="6d5aa-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="6d5aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d5aa-107">EXAMPLES</span></span>

### <span data-ttu-id="6d5aa-108">Esempio 1: Ottenere le metriche di quota</span><span class="sxs-lookup"><span data-stu-id="6d5aa-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="6d5aa-109">Recupera le informazioni relative alla metrica delle quote per IotHub denominate "myiothub"</span><span class="sxs-lookup"><span data-stu-id="6d5aa-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="6d5aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d5aa-110">PARAMETERS</span></span>

### <span data-ttu-id="6d5aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5aa-111">-DefaultProfile</span></span>
<span data-ttu-id="6d5aa-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="6d5aa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d5aa-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6d5aa-113">-Name</span></span>
<span data-ttu-id="6d5aa-114">Nome dell'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="6d5aa-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="6d5aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d5aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d5aa-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6d5aa-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6d5aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5aa-117">CommonParameters</span></span>
<span data-ttu-id="6d5aa-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d5aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5aa-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d5aa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5aa-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d5aa-120">INPUTS</span></span>

### <span data-ttu-id="6d5aa-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6d5aa-121">System.String</span></span>

## <span data-ttu-id="6d5aa-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d5aa-122">OUTPUTS</span></span>

### <span data-ttu-id="6d5aa-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="6d5aa-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="6d5aa-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d5aa-124">NOTES</span></span>

## <span data-ttu-id="6d5aa-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d5aa-125">RELATED LINKS</span></span>
