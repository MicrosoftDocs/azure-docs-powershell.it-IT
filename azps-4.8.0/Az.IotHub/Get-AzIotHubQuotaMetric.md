---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189920"
---
# <span data-ttu-id="e8843-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="e8843-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="e8843-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8843-102">SYNOPSIS</span></span>
<span data-ttu-id="e8843-103">Ottiene le metriche delle quote per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="e8843-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="e8843-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8843-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8843-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8843-105">DESCRIPTION</span></span>
<span data-ttu-id="e8843-106">Ottiene le metriche delle quote per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="e8843-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="e8843-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8843-107">EXAMPLES</span></span>

### <span data-ttu-id="e8843-108">Esempio 1 ottenere le metriche delle quote</span><span class="sxs-lookup"><span data-stu-id="e8843-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e8843-109">Ottiene le informazioni metriche sulle quote per il IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e8843-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e8843-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8843-110">PARAMETERS</span></span>

### <span data-ttu-id="e8843-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8843-111">-DefaultProfile</span></span>
<span data-ttu-id="e8843-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8843-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8843-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8843-113">-Name</span></span>
<span data-ttu-id="e8843-114">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="e8843-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="e8843-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8843-115">-ResourceGroupName</span></span>
<span data-ttu-id="e8843-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e8843-116">Resource Group Name</span></span>

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

### <span data-ttu-id="e8843-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8843-117">CommonParameters</span></span>
<span data-ttu-id="e8843-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8843-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8843-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8843-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8843-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8843-120">INPUTS</span></span>

### <span data-ttu-id="e8843-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e8843-121">System.String</span></span>

## <span data-ttu-id="e8843-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8843-122">OUTPUTS</span></span>

### <span data-ttu-id="e8843-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="e8843-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="e8843-124">Note</span><span class="sxs-lookup"><span data-stu-id="e8843-124">NOTES</span></span>

## <span data-ttu-id="e8843-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8843-125">RELATED LINKS</span></span>