---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688424"
---
# <span data-ttu-id="effb3-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="effb3-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="effb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="effb3-102">SYNOPSIS</span></span>
<span data-ttu-id="effb3-103">Crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="effb3-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="effb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="effb3-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="effb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="effb3-105">DESCRIPTION</span></span>
<span data-ttu-id="effb3-106">Il cmdlet **New-AzureRmMetricFilter** crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="effb3-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="effb3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="effb3-107">EXAMPLES</span></span>

### <span data-ttu-id="effb3-108">Esempio 1: creare un filtro di dimensione metrica</span><span class="sxs-lookup"><span data-stu-id="effb3-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="effb3-109">Questo comando crea il filtro di dimensione metrica del formato "City EQ ' Seattle" o City EQ "New York".</span><span class="sxs-lookup"><span data-stu-id="effb3-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="effb3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="effb3-110">PARAMETERS</span></span>

### <span data-ttu-id="effb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="effb3-111">-DefaultProfile</span></span>
<span data-ttu-id="effb3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="effb3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="effb3-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="effb3-113">-Dimension</span></span>
<span data-ttu-id="effb3-114">Nome della dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="effb3-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="effb3-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="effb3-115">-Operator</span></span>
<span data-ttu-id="effb3-116">Specifica l'operatore usato per selezionare la dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="effb3-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="effb3-117">-Valore</span><span class="sxs-lookup"><span data-stu-id="effb3-117">-Value</span></span>
<span data-ttu-id="effb3-118">Specifica la matrice di valori delle dimensioni metriche.</span><span class="sxs-lookup"><span data-stu-id="effb3-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="effb3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="effb3-119">CommonParameters</span></span>
<span data-ttu-id="effb3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="effb3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="effb3-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="effb3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="effb3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="effb3-122">INPUTS</span></span>

### <span data-ttu-id="effb3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="effb3-123">System.String</span></span>

### <span data-ttu-id="effb3-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="effb3-124">System.String[]</span></span>

## <span data-ttu-id="effb3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="effb3-125">OUTPUTS</span></span>

### <span data-ttu-id="effb3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="effb3-126">System.String</span></span>

## <span data-ttu-id="effb3-127">Note</span><span class="sxs-lookup"><span data-stu-id="effb3-127">NOTES</span></span>

## <span data-ttu-id="effb3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="effb3-128">RELATED LINKS</span></span>

<span data-ttu-id="effb3-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="effb3-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

