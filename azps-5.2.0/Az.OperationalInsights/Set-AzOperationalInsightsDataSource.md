---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372091"
---
# <span data-ttu-id="f1b12-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f1b12-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="f1b12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1b12-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b12-103">Aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="f1b12-103">Updates a data source.</span></span>

## <span data-ttu-id="f1b12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1b12-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1b12-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1b12-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b12-106">Il cmdlet **set-AzOperationalInsightsDataSource** aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="f1b12-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="f1b12-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1b12-107">EXAMPLES</span></span>

## <span data-ttu-id="f1b12-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1b12-108">PARAMETERS</span></span>

### <span data-ttu-id="f1b12-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="f1b12-109">-DataSource</span></span>
<span data-ttu-id="f1b12-110">Specifica l'origine dati aggiornata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b12-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f1b12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b12-111">-DefaultProfile</span></span>
<span data-ttu-id="f1b12-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f1b12-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1b12-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b12-113">CommonParameters</span></span>
<span data-ttu-id="f1b12-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b12-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b12-115">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b12-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b12-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1b12-116">INPUTS</span></span>

### <span data-ttu-id="f1b12-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f1b12-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f1b12-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1b12-118">OUTPUTS</span></span>

### <span data-ttu-id="f1b12-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f1b12-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f1b12-120">Note</span><span class="sxs-lookup"><span data-stu-id="f1b12-120">NOTES</span></span>
* <span data-ttu-id="f1b12-121">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="f1b12-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f1b12-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1b12-122">RELATED LINKS</span></span>

[<span data-ttu-id="f1b12-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f1b12-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="f1b12-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f1b12-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


