---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5bf4f178ee3343b5100dad87836c3215fba4cfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520156"
---
# <span data-ttu-id="7a272-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7a272-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="7a272-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a272-102">SYNOPSIS</span></span>
<span data-ttu-id="7a272-103">Aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="7a272-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a272-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a272-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a272-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a272-105">DESCRIPTION</span></span>
<span data-ttu-id="7a272-106">Il cmdlet **set-AzureRmOperationalInsightsDataSource** aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="7a272-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="7a272-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a272-107">EXAMPLES</span></span>

## <span data-ttu-id="7a272-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a272-108">PARAMETERS</span></span>

### <span data-ttu-id="7a272-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="7a272-109">-DataSource</span></span>
<span data-ttu-id="7a272-110">Specifica l'origine dati aggiornata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a272-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a272-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a272-111">-DefaultProfile</span></span>
<span data-ttu-id="7a272-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7a272-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a272-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a272-113">CommonParameters</span></span>
<span data-ttu-id="7a272-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a272-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a272-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a272-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a272-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a272-116">INPUTS</span></span>

### <span data-ttu-id="7a272-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7a272-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>
<span data-ttu-id="7a272-118">Parametri: DataSource (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a272-118">Parameters: DataSource (ByValue)</span></span>

## <span data-ttu-id="7a272-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a272-119">OUTPUTS</span></span>

### <span data-ttu-id="7a272-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7a272-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7a272-121">Note</span><span class="sxs-lookup"><span data-stu-id="7a272-121">NOTES</span></span>
* <span data-ttu-id="7a272-122">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="7a272-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7a272-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a272-123">RELATED LINKS</span></span>

[<span data-ttu-id="7a272-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7a272-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="7a272-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7a272-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


