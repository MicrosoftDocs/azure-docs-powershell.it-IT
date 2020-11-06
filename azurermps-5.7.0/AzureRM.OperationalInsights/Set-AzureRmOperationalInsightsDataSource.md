---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e45dcbfad9b4b92695f310d7d2c56fc46fc57bd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508108"
---
# <span data-ttu-id="f036a-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f036a-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="f036a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f036a-102">SYNOPSIS</span></span>
<span data-ttu-id="f036a-103">Aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="f036a-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f036a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f036a-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f036a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f036a-105">DESCRIPTION</span></span>
<span data-ttu-id="f036a-106">Il cmdlet **set-AzureRmOperationalInsightsDataSource** aggiorna un'origine dati.</span><span class="sxs-lookup"><span data-stu-id="f036a-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="f036a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f036a-107">EXAMPLES</span></span>

## <span data-ttu-id="f036a-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f036a-108">PARAMETERS</span></span>

### <span data-ttu-id="f036a-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="f036a-109">-DataSource</span></span>
<span data-ttu-id="f036a-110">Specifica l'origine dati aggiornata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f036a-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: PSDataSource
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f036a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f036a-111">-DefaultProfile</span></span>
<span data-ttu-id="f036a-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f036a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f036a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f036a-113">CommonParameters</span></span>
<span data-ttu-id="f036a-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f036a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f036a-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f036a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f036a-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f036a-116">INPUTS</span></span>

### <span data-ttu-id="f036a-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f036a-117">PSDataSource</span></span>
<span data-ttu-id="f036a-118">Il parametro "DataSource" accetta il valore di tipo "PSDataSource" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f036a-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="f036a-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f036a-119">OUTPUTS</span></span>

### <span data-ttu-id="f036a-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f036a-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f036a-121">Note</span><span class="sxs-lookup"><span data-stu-id="f036a-121">NOTES</span></span>
* <span data-ttu-id="f036a-122">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="f036a-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f036a-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f036a-123">RELATED LINKS</span></span>

[<span data-ttu-id="f036a-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f036a-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="f036a-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f036a-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


