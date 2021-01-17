---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331564"
---
# <span data-ttu-id="36c6c-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="36c6c-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="36c6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="36c6c-103">Crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="36c6c-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="36c6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36c6c-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36c6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="36c6c-106">Il cmdlet **New-AzMetricFilter** crea un filtro di dimensione metrica che può essere usato per eseguire query sulle metriche.</span><span class="sxs-lookup"><span data-stu-id="36c6c-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="36c6c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36c6c-107">EXAMPLES</span></span>

### <span data-ttu-id="36c6c-108">Esempio 1: creare un filtro di dimensione metrica</span><span class="sxs-lookup"><span data-stu-id="36c6c-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="36c6c-109">Questo comando crea il filtro di dimensione metrica del formato "City EQ ' Seattle" o City EQ "New York".</span><span class="sxs-lookup"><span data-stu-id="36c6c-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="36c6c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36c6c-110">PARAMETERS</span></span>

### <span data-ttu-id="36c6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c6c-111">-DefaultProfile</span></span>
<span data-ttu-id="36c6c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36c6c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36c6c-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="36c6c-113">-Dimension</span></span>
<span data-ttu-id="36c6c-114">Nome della dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="36c6c-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="36c6c-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="36c6c-115">-Operator</span></span>
<span data-ttu-id="36c6c-116">Specifica l'operatore usato per selezionare la dimensione metrica.</span><span class="sxs-lookup"><span data-stu-id="36c6c-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="36c6c-117">-Valore</span><span class="sxs-lookup"><span data-stu-id="36c6c-117">-Value</span></span>
<span data-ttu-id="36c6c-118">Specifica la matrice di valori delle dimensioni metriche.</span><span class="sxs-lookup"><span data-stu-id="36c6c-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="36c6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c6c-119">CommonParameters</span></span>
<span data-ttu-id="36c6c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c6c-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36c6c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c6c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36c6c-122">INPUTS</span></span>

### <span data-ttu-id="36c6c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="36c6c-123">System.String</span></span>

### <span data-ttu-id="36c6c-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="36c6c-124">System.String[]</span></span>

## <span data-ttu-id="36c6c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36c6c-125">OUTPUTS</span></span>

### <span data-ttu-id="36c6c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="36c6c-126">System.String</span></span>

## <span data-ttu-id="36c6c-127">Note</span><span class="sxs-lookup"><span data-stu-id="36c6c-127">NOTES</span></span>

## <span data-ttu-id="36c6c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36c6c-128">RELATED LINKS</span></span>

<span data-ttu-id="36c6c-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="36c6c-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

