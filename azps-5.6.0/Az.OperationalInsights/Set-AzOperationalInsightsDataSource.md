---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4156bc414105d6d104e8315d83f92f0fb6e19ab3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989742"
---
# <span data-ttu-id="c3025-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c3025-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="c3025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3025-102">SYNOPSIS</span></span>
<span data-ttu-id="c3025-103">Aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="c3025-103">Updates a data source.</span></span>

## <span data-ttu-id="c3025-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3025-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3025-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3025-105">DESCRIPTION</span></span>
<span data-ttu-id="c3025-106">Il cmdlet **Set-AzOperationalInsightsDataSource** aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="c3025-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="c3025-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3025-107">EXAMPLES</span></span>

## <span data-ttu-id="c3025-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3025-108">PARAMETERS</span></span>

### <span data-ttu-id="c3025-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="c3025-109">-DataSource</span></span>
<span data-ttu-id="c3025-110">Specifica l'origine dati aggiornata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3025-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c3025-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3025-111">-DefaultProfile</span></span>
<span data-ttu-id="c3025-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c3025-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3025-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3025-113">CommonParameters</span></span>
<span data-ttu-id="c3025-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3025-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3025-115">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3025-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3025-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3025-116">INPUTS</span></span>

### <span data-ttu-id="c3025-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c3025-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c3025-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3025-118">OUTPUTS</span></span>

### <span data-ttu-id="c3025-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c3025-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c3025-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3025-120">NOTES</span></span>
* <span data-ttu-id="c3025-121">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="c3025-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c3025-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3025-122">RELATED LINKS</span></span>

[<span data-ttu-id="c3025-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c3025-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="c3025-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c3025-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


