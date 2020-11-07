---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677796"
---
# <span data-ttu-id="5b850-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5b850-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5b850-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b850-102">SYNOPSIS</span></span>
<span data-ttu-id="5b850-103">Aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="5b850-103">Updates a data source.</span></span>

## <span data-ttu-id="5b850-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b850-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b850-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b850-105">DESCRIPTION</span></span>
<span data-ttu-id="5b850-106">Il cmdlet **set-AzOperationalInsightsDataSource** aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="5b850-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="5b850-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b850-107">EXAMPLES</span></span>

## <span data-ttu-id="5b850-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b850-108">PARAMETERS</span></span>

### <span data-ttu-id="5b850-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="5b850-109">-DataSource</span></span>
<span data-ttu-id="5b850-110">Specifica l'origine dati aggiornata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b850-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5b850-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b850-111">-DefaultProfile</span></span>
<span data-ttu-id="5b850-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5b850-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b850-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b850-113">CommonParameters</span></span>
<span data-ttu-id="5b850-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b850-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b850-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b850-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b850-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b850-116">INPUTS</span></span>

### <span data-ttu-id="5b850-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5b850-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5b850-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b850-118">OUTPUTS</span></span>

### <span data-ttu-id="5b850-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5b850-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5b850-120">Note</span><span class="sxs-lookup"><span data-stu-id="5b850-120">NOTES</span></span>
* <span data-ttu-id="5b850-121">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="5b850-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5b850-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b850-122">RELATED LINKS</span></span>

[<span data-ttu-id="5b850-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5b850-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="5b850-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5b850-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


