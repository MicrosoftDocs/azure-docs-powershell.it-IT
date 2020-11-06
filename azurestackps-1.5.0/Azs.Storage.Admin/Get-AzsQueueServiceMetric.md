---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac33f0feae7d54798753637f8f7898ab796f0939
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491457"
---
# <span data-ttu-id="8dbb0-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="8dbb0-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="8dbb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dbb0-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbb0-103">Restituisce un elenco di metriche per il servizio code.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="8dbb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dbb0-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dbb0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dbb0-105">DESCRIPTION</span></span>
<span data-ttu-id="8dbb0-106">Restituisce un elenco di metriche per il servizio code.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="8dbb0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dbb0-107">EXAMPLES</span></span>

### <span data-ttu-id="8dbb0-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8dbb0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="8dbb0-109">Ottenere l'elenco delle metriche per il servizio code.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="8dbb0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dbb0-110">PARAMETERS</span></span>

### <span data-ttu-id="8dbb0-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="8dbb0-111">-FarmName</span></span>
<span data-ttu-id="8dbb0-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-112">Farm Id.</span></span>

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

### <span data-ttu-id="8dbb0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dbb0-113">-ResourceGroupName</span></span>
<span data-ttu-id="8dbb0-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-114">Resource group name.</span></span>

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

### <span data-ttu-id="8dbb0-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="8dbb0-115">-Skip</span></span>
<span data-ttu-id="8dbb0-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8dbb0-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="8dbb0-117">-Top</span></span>
<span data-ttu-id="8dbb0-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8dbb0-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8dbb0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbb0-120">CommonParameters</span></span>
<span data-ttu-id="8dbb0-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dbb0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbb0-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dbb0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbb0-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dbb0-123">INPUTS</span></span>

## <span data-ttu-id="8dbb0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dbb0-124">OUTPUTS</span></span>

### <span data-ttu-id="8dbb0-125">Microsoft. AzureStack. Management. storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="8dbb0-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="8dbb0-126">Note</span><span class="sxs-lookup"><span data-stu-id="8dbb0-126">NOTES</span></span>

## <span data-ttu-id="8dbb0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dbb0-127">RELATED LINKS</span></span>

