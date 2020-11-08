---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022483"
---
# <span data-ttu-id="5eefc-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5eefc-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5eefc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5eefc-102">SYNOPSIS</span></span>
<span data-ttu-id="5eefc-103">Aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="5eefc-103">Updates a data source.</span></span>

## <span data-ttu-id="5eefc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5eefc-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5eefc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eefc-105">DESCRIPTION</span></span>
<span data-ttu-id="5eefc-106">Il cmdlet **set-AzOperationalInsightsDataSource** aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="5eefc-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="5eefc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5eefc-107">EXAMPLES</span></span>

## <span data-ttu-id="5eefc-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5eefc-108">PARAMETERS</span></span>

### <span data-ttu-id="5eefc-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="5eefc-109">-DataSource</span></span>
<span data-ttu-id="5eefc-110">Specifica l'origine dati aggiornata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eefc-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5eefc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eefc-111">-DefaultProfile</span></span>
<span data-ttu-id="5eefc-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5eefc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5eefc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eefc-113">CommonParameters</span></span>
<span data-ttu-id="5eefc-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eefc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eefc-115">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eefc-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eefc-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5eefc-116">INPUTS</span></span>

### <span data-ttu-id="5eefc-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5eefc-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5eefc-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5eefc-118">OUTPUTS</span></span>

### <span data-ttu-id="5eefc-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5eefc-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5eefc-120">Note</span><span class="sxs-lookup"><span data-stu-id="5eefc-120">NOTES</span></span>
* <span data-ttu-id="5eefc-121">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="5eefc-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5eefc-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5eefc-122">RELATED LINKS</span></span>

[<span data-ttu-id="5eefc-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5eefc-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="5eefc-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5eefc-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


