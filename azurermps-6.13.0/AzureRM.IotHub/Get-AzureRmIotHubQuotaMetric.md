---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubQuotaMetric.md
ms.openlocfilehash: 1de2d49d6e914635f8fc0d38ffa81755cc622481
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687854"
---
# <span data-ttu-id="c2ccb-101">Get-AzureRmIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="c2ccb-101">Get-AzureRmIotHubQuotaMetric</span></span>

## <span data-ttu-id="c2ccb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ccb-103">Ottiene le metriche delle quote per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="c2ccb-103">Gets the Quota Metrics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2ccb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2ccb-104">SYNTAX</span></span>

```
Get-AzureRmIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2ccb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ccb-106">Ottiene le metriche delle quote per un IotHub.</span><span class="sxs-lookup"><span data-stu-id="c2ccb-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="c2ccb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="c2ccb-108">Esempio 1 ottenere le metriche delle quote</span><span class="sxs-lookup"><span data-stu-id="c2ccb-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzureRmIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c2ccb-109">Ottiene le informazioni metriche sulle quote per il IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c2ccb-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c2ccb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="c2ccb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ccb-111">-DefaultProfile</span></span>
<span data-ttu-id="c2ccb-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c2ccb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ccb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2ccb-113">-Name</span></span>
<span data-ttu-id="c2ccb-114">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="c2ccb-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="c2ccb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ccb-115">-ResourceGroupName</span></span>
<span data-ttu-id="c2ccb-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c2ccb-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c2ccb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ccb-117">CommonParameters</span></span>
<span data-ttu-id="c2ccb-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ccb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ccb-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ccb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ccb-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2ccb-120">INPUTS</span></span>

### <span data-ttu-id="c2ccb-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c2ccb-121">System.String</span></span>

## <span data-ttu-id="c2ccb-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2ccb-122">OUTPUTS</span></span>

### <span data-ttu-id="c2ccb-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="c2ccb-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="c2ccb-124">Note</span><span class="sxs-lookup"><span data-stu-id="c2ccb-124">NOTES</span></span>

## <span data-ttu-id="c2ccb-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2ccb-125">RELATED LINKS</span></span>
