---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: a7fdb0824d464f1704f46a8e8fe19705b2b160fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012909"
---
# <span data-ttu-id="70937-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="70937-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="70937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70937-102">SYNOPSIS</span></span>
<span data-ttu-id="70937-103">Crea un filtro delle dimensioni metriche che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="70937-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="70937-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70937-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70937-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70937-105">DESCRIPTION</span></span>
<span data-ttu-id="70937-106">Il cmdlet **New-AzMetricFilter crea** un filtro delle dimensioni metriche che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="70937-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="70937-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70937-107">EXAMPLES</span></span>

### <span data-ttu-id="70937-108">Esempio 1: Creare un filtro delle dimensioni metriche</span><span class="sxs-lookup"><span data-stu-id="70937-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="70937-109">Questo comando crea un filtro metrico per le dimensioni nel formato "Città eq 'Seattle' o Città eq 'Roma'".</span><span class="sxs-lookup"><span data-stu-id="70937-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="70937-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70937-110">PARAMETERS</span></span>

### <span data-ttu-id="70937-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70937-111">-DefaultProfile</span></span>
<span data-ttu-id="70937-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70937-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70937-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="70937-113">-Dimension</span></span>
<span data-ttu-id="70937-114">Nome della dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="70937-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="70937-115">-Operatore</span><span class="sxs-lookup"><span data-stu-id="70937-115">-Operator</span></span>
<span data-ttu-id="70937-116">Specifica l'operatore usato per selezionare la dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="70937-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="70937-117">-Value</span><span class="sxs-lookup"><span data-stu-id="70937-117">-Value</span></span>
<span data-ttu-id="70937-118">Specifica la matrice dei valori di dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="70937-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="70937-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70937-119">CommonParameters</span></span>
<span data-ttu-id="70937-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70937-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70937-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="70937-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70937-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="70937-122">INPUTS</span></span>

### <span data-ttu-id="70937-123">System.String</span><span class="sxs-lookup"><span data-stu-id="70937-123">System.String</span></span>

### <span data-ttu-id="70937-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="70937-124">System.String[]</span></span>

## <span data-ttu-id="70937-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70937-125">OUTPUTS</span></span>

### <span data-ttu-id="70937-126">System.String</span><span class="sxs-lookup"><span data-stu-id="70937-126">System.String</span></span>

## <span data-ttu-id="70937-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="70937-127">NOTES</span></span>

## <span data-ttu-id="70937-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70937-128">RELATED LINKS</span></span>

<span data-ttu-id="70937-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="70937-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

