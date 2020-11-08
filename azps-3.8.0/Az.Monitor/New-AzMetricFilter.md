---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018354"
---
# <span data-ttu-id="be606-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="be606-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="be606-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be606-102">SYNOPSIS</span></span>
<span data-ttu-id="be606-103">Crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="be606-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="be606-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be606-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be606-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be606-105">DESCRIPTION</span></span>
<span data-ttu-id="be606-106">Il cmdlet **New-AzMetricFilter** crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="be606-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="be606-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be606-107">EXAMPLES</span></span>

### <span data-ttu-id="be606-108">Esempio 1: creare un filtro di dimensione metrica</span><span class="sxs-lookup"><span data-stu-id="be606-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="be606-109">Questo comando crea il filtro di dimensione metrica del formato "City EQ ' Seattle" o City EQ "New York".</span><span class="sxs-lookup"><span data-stu-id="be606-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="be606-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be606-110">PARAMETERS</span></span>

### <span data-ttu-id="be606-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be606-111">-DefaultProfile</span></span>
<span data-ttu-id="be606-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be606-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be606-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="be606-113">-Dimension</span></span>
<span data-ttu-id="be606-114">Nome della dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="be606-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="be606-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="be606-115">-Operator</span></span>
<span data-ttu-id="be606-116">Specifica l'operatore usato per selezionare la dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="be606-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="be606-117">-Valore</span><span class="sxs-lookup"><span data-stu-id="be606-117">-Value</span></span>
<span data-ttu-id="be606-118">Specifica la matrice di valori delle dimensioni metriche.</span><span class="sxs-lookup"><span data-stu-id="be606-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="be606-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be606-119">CommonParameters</span></span>
<span data-ttu-id="be606-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be606-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be606-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be606-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be606-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be606-122">INPUTS</span></span>

### <span data-ttu-id="be606-123">System. String</span><span class="sxs-lookup"><span data-stu-id="be606-123">System.String</span></span>

### <span data-ttu-id="be606-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="be606-124">System.String[]</span></span>

## <span data-ttu-id="be606-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be606-125">OUTPUTS</span></span>

### <span data-ttu-id="be606-126">System. String</span><span class="sxs-lookup"><span data-stu-id="be606-126">System.String</span></span>

## <span data-ttu-id="be606-127">Note</span><span class="sxs-lookup"><span data-stu-id="be606-127">NOTES</span></span>

## <span data-ttu-id="be606-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be606-128">RELATED LINKS</span></span>

<span data-ttu-id="be606-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="be606-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

