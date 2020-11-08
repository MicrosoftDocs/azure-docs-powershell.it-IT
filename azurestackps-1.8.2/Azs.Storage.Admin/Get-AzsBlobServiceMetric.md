---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 822452c1c6b83669759bae2c861ee3456a13a0dc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030222"
---
# <span data-ttu-id="084d7-101">Get-AzsBlobServiceMetric</span><span class="sxs-lookup"><span data-stu-id="084d7-101">Get-AzsBlobServiceMetric</span></span>

## <span data-ttu-id="084d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="084d7-102">SYNOPSIS</span></span>
<span data-ttu-id="084d7-103">Restituisce un elenco di metriche per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="084d7-103">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="084d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="084d7-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="084d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084d7-105">DESCRIPTION</span></span>
<span data-ttu-id="084d7-106">Restituisce un elenco di metriche per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="084d7-106">Returns a list of metrics for blob service.</span></span>

## <span data-ttu-id="084d7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="084d7-107">EXAMPLES</span></span>

### <span data-ttu-id="084d7-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="084d7-108">EXAMPLE 1</span></span>
```
Get-AzsBlobServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="084d7-109">Ottenere un elenco di metriche per il servizio BLOB.</span><span class="sxs-lookup"><span data-stu-id="084d7-109">Get a list of metrics for blob service.</span></span>

## <span data-ttu-id="084d7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="084d7-110">PARAMETERS</span></span>

### <span data-ttu-id="084d7-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="084d7-111">-FarmName</span></span>
<span data-ttu-id="084d7-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="084d7-112">Farm Id.</span></span>

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

### <span data-ttu-id="084d7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084d7-113">-ResourceGroupName</span></span>
<span data-ttu-id="084d7-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="084d7-114">Resource group name.</span></span>

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

### <span data-ttu-id="084d7-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="084d7-115">-Skip</span></span>
<span data-ttu-id="084d7-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="084d7-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="084d7-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="084d7-117">-Top</span></span>
<span data-ttu-id="084d7-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="084d7-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="084d7-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="084d7-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="084d7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084d7-120">CommonParameters</span></span>
<span data-ttu-id="084d7-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="084d7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084d7-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="084d7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084d7-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="084d7-123">INPUTS</span></span>

## <span data-ttu-id="084d7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="084d7-124">OUTPUTS</span></span>

### <span data-ttu-id="084d7-125">Microsoft. AzureStack. Management. storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="084d7-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="084d7-126">Note</span><span class="sxs-lookup"><span data-stu-id="084d7-126">NOTES</span></span>

## <span data-ttu-id="084d7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="084d7-127">RELATED LINKS</span></span>
