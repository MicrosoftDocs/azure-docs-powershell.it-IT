---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: 203044deb41ae21591b33ea6e306bcd98905e540
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854077"
---
# <span data-ttu-id="9438e-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="9438e-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="9438e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9438e-102">SYNOPSIS</span></span>
<span data-ttu-id="9438e-103">Crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="9438e-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="9438e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9438e-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9438e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9438e-105">DESCRIPTION</span></span>
<span data-ttu-id="9438e-106">Il cmdlet **New-AzMetricFilter** crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="9438e-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="9438e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9438e-107">EXAMPLES</span></span>

### <span data-ttu-id="9438e-108">Esempio 1: creare un filtro di dimensione metrica</span><span class="sxs-lookup"><span data-stu-id="9438e-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="9438e-109">Questo comando crea il filtro di dimensione metrica del formato "City EQ ' Seattle" o City EQ "New York".</span><span class="sxs-lookup"><span data-stu-id="9438e-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="9438e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9438e-110">PARAMETERS</span></span>

### <span data-ttu-id="9438e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9438e-111">-DefaultProfile</span></span>
<span data-ttu-id="9438e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9438e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9438e-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="9438e-113">-Dimension</span></span>
<span data-ttu-id="9438e-114">Nome della dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="9438e-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="9438e-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="9438e-115">-Operator</span></span>
<span data-ttu-id="9438e-116">Specifica l'operatore usato per selezionare la dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="9438e-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="9438e-117">-Valore</span><span class="sxs-lookup"><span data-stu-id="9438e-117">-Value</span></span>
<span data-ttu-id="9438e-118">Specifica la matrice di valori delle dimensioni metriche.</span><span class="sxs-lookup"><span data-stu-id="9438e-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="9438e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9438e-119">CommonParameters</span></span>
<span data-ttu-id="9438e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9438e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9438e-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9438e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9438e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9438e-122">INPUTS</span></span>

### <span data-ttu-id="9438e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9438e-123">System.String</span></span>

### <span data-ttu-id="9438e-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="9438e-124">System.String[]</span></span>

## <span data-ttu-id="9438e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9438e-125">OUTPUTS</span></span>

### <span data-ttu-id="9438e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9438e-126">System.String</span></span>

## <span data-ttu-id="9438e-127">Note</span><span class="sxs-lookup"><span data-stu-id="9438e-127">NOTES</span></span>

## <span data-ttu-id="9438e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9438e-128">RELATED LINKS</span></span>

<span data-ttu-id="9438e-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="9438e-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

