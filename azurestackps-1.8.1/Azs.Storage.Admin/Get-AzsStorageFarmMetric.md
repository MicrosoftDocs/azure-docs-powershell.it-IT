---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ce903ba229942386f53d7cd3559c1b4c9ac835f
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859809"
---
# <span data-ttu-id="9f320-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="9f320-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="9f320-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f320-102">SYNOPSIS</span></span>
<span data-ttu-id="9f320-103">Restituisce un elenco di metriche della farm di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9f320-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="9f320-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f320-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f320-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f320-105">DESCRIPTION</span></span>
<span data-ttu-id="9f320-106">Restituisce un elenco di metriche della farm di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9f320-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="9f320-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f320-107">EXAMPLES</span></span>

### <span data-ttu-id="9f320-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="9f320-108">EXAMPLE 1</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="9f320-109">Ottenere l'elenco delle metriche della farm di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9f320-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="9f320-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f320-110">PARAMETERS</span></span>

### <span data-ttu-id="9f320-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="9f320-111">-FarmName</span></span>
<span data-ttu-id="9f320-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="9f320-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f320-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f320-113">-ResourceGroupName</span></span>
<span data-ttu-id="9f320-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f320-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f320-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="9f320-115">-Skip</span></span>
<span data-ttu-id="9f320-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9f320-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f320-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="9f320-117">-Top</span></span>
<span data-ttu-id="9f320-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9f320-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9f320-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="9f320-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f320-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f320-120">CommonParameters</span></span>
<span data-ttu-id="9f320-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f320-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f320-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f320-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f320-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f320-123">INPUTS</span></span>

## <span data-ttu-id="9f320-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f320-124">OUTPUTS</span></span>

### <span data-ttu-id="9f320-125">Microsoft. AzureStack. Management. storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="9f320-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="9f320-126">Note</span><span class="sxs-lookup"><span data-stu-id="9f320-126">NOTES</span></span>

## <span data-ttu-id="9f320-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f320-127">RELATED LINKS</span></span>
