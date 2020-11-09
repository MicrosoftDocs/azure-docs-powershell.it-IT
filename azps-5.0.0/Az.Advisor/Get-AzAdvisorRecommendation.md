---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorRecommendation.md
ms.openlocfilehash: 631e471af79ab5ac567afeafa8103e22ae885ed7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311659"
---
# <span data-ttu-id="e970e-101">Get-AzAdvisorRecommendation</span><span class="sxs-lookup"><span data-stu-id="e970e-101">Get-AzAdvisorRecommendation</span></span>

## <span data-ttu-id="e970e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e970e-102">SYNOPSIS</span></span>
<span data-ttu-id="e970e-103">Ottiene un elenco di suggerimenti di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="e970e-103">Gets a list of Azure Advisor recommendations.</span></span>

## <span data-ttu-id="e970e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e970e-104">SYNTAX</span></span>

### <span data-ttu-id="e970e-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e970e-105">NameParameterSet (Default)</span></span>
```
Get-AzAdvisorRecommendation [-Category <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e970e-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e970e-106">IdParameterSet</span></span>
```
Get-AzAdvisorRecommendation [-ResourceId] <String> [-Category <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e970e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e970e-107">DESCRIPTION</span></span>
<span data-ttu-id="e970e-108">Ottiene l'elenco di suggerimenti di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="e970e-108">Obtains the list of Azure Advisor recommendations.</span></span> <span data-ttu-id="e970e-109">Può essere filtrato per categoria, ID risorsa, nome e così via.</span><span class="sxs-lookup"><span data-stu-id="e970e-109">Can be filtered by Category, resource-ID, name etc.</span></span>

## <span data-ttu-id="e970e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e970e-110">EXAMPLES</span></span>

### <span data-ttu-id="e970e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e970e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="e970e-112">Ottiene l'elenco di tutti i suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="e970e-112">Gets the list of all recommendations.</span></span>

### <span data-ttu-id="e970e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e970e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAdvisorRecommendation -Category Performance
ResourceId                   : /subscriptions/{user_subscription}/resourceGroups/{resourceGroupName}/providers/Microsoft.Cache/Redis/xyz/providers/Microsoft.Advisor/recommen
                       dations/{recommendation-Id}
Category             : Performance
ExtendedProperties   : {}
Impact               : Medium
ImpactedField        : Microsoft.Cache/Redis
ImpactedValue        : azacache
LastUpdated          : 12/5/2018 4:45:55 PM
Metadata             : {}
RecommendationTypeId : 905a0026-8010-45b2-ab46-a92c3e4a5131
Risk                 : None
ShortDescription     : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsRecommendationBaseShortDescription
SuppressionIds       : {}
Name                 : {recommendation-Id}
Type                 : Microsoft.Advisor/recommendations
```
<span data-ttu-id="e970e-114">Ottiene l'elenco di tutti i suggerimenti filtrati in base alle prestazioni delle categorie.</span><span class="sxs-lookup"><span data-stu-id="e970e-114">Gets the list of all recommendations filtered by category Performance.</span></span>

## <span data-ttu-id="e970e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e970e-115">PARAMETERS</span></span>

### <span data-ttu-id="e970e-116">-Categoria</span><span class="sxs-lookup"><span data-stu-id="e970e-116">-Category</span></span>
<span data-ttu-id="e970e-117">Categoria della raccomandazione</span><span class="sxs-lookup"><span data-stu-id="e970e-117">Category of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, HighAvailability, Performance, Security, OperationalExcellence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e970e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e970e-118">-DefaultProfile</span></span>
<span data-ttu-id="e970e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e970e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e970e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e970e-120">-ResourceGroupName</span></span>
<span data-ttu-id="e970e-121">ResourceGroup il nome della raccomandazione</span><span class="sxs-lookup"><span data-stu-id="e970e-121">ResourceGroup name of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e970e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e970e-122">-ResourceId</span></span>
<span data-ttu-id="e970e-123">ResourceId della raccomandazione</span><span class="sxs-lookup"><span data-stu-id="e970e-123">ResourceId of the recommendation</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e970e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e970e-124">CommonParameters</span></span>
<span data-ttu-id="e970e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e970e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e970e-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e970e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e970e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e970e-127">INPUTS</span></span>

### <span data-ttu-id="e970e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e970e-128">System.String</span></span>

## <span data-ttu-id="e970e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e970e-129">OUTPUTS</span></span>

### <span data-ttu-id="e970e-130">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorResourceRecommendationBase</span><span class="sxs-lookup"><span data-stu-id="e970e-130">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorResourceRecommendationBase</span></span>

## <span data-ttu-id="e970e-131">Note</span><span class="sxs-lookup"><span data-stu-id="e970e-131">NOTES</span></span>

## <span data-ttu-id="e970e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e970e-132">RELATED LINKS</span></span>
