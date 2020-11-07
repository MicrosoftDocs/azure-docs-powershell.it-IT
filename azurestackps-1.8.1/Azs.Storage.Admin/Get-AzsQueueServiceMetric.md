---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2776c768f49dabdea8483ff601f129e80bfc2dc
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859845"
---
# <span data-ttu-id="9497f-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="9497f-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="9497f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9497f-102">SYNOPSIS</span></span>
<span data-ttu-id="9497f-103">Restituisce un elenco di metriche per il servizio code.</span><span class="sxs-lookup"><span data-stu-id="9497f-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="9497f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9497f-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="9497f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9497f-105">DESCRIPTION</span></span>
<span data-ttu-id="9497f-106">Restituisce un elenco di metriche per il servizio code.</span><span class="sxs-lookup"><span data-stu-id="9497f-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="9497f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9497f-107">EXAMPLES</span></span>

### <span data-ttu-id="9497f-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="9497f-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="9497f-109">Ottenere l'elenco delle metriche per il servizio code.</span><span class="sxs-lookup"><span data-stu-id="9497f-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="9497f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9497f-110">PARAMETERS</span></span>

### <span data-ttu-id="9497f-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="9497f-111">-FarmName</span></span>
<span data-ttu-id="9497f-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="9497f-112">Farm Id.</span></span>

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

### <span data-ttu-id="9497f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9497f-113">-ResourceGroupName</span></span>
<span data-ttu-id="9497f-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9497f-114">Resource group name.</span></span>

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

### <span data-ttu-id="9497f-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="9497f-115">-Skip</span></span>
<span data-ttu-id="9497f-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9497f-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9497f-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="9497f-117">-Top</span></span>
<span data-ttu-id="9497f-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9497f-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9497f-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="9497f-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9497f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9497f-120">CommonParameters</span></span>
<span data-ttu-id="9497f-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9497f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9497f-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9497f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9497f-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9497f-123">INPUTS</span></span>

## <span data-ttu-id="9497f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9497f-124">OUTPUTS</span></span>

### <span data-ttu-id="9497f-125">Microsoft. AzureStack. Management. storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="9497f-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="9497f-126">Note</span><span class="sxs-lookup"><span data-stu-id="9497f-126">NOTES</span></span>

## <span data-ttu-id="9497f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9497f-127">RELATED LINKS</span></span>
