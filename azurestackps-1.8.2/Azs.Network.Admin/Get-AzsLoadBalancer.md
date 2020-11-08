---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030413"
---
# <span data-ttu-id="d7dd1-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7dd1-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="d7dd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="d7dd1-103">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="d7dd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7dd1-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7dd1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="d7dd1-106">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="d7dd1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7dd1-107">EXAMPLES</span></span>

### <span data-ttu-id="d7dd1-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="d7dd1-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="d7dd1-109">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="d7dd1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7dd1-110">PARAMETERS</span></span>

### <span data-ttu-id="d7dd1-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d7dd1-111">-Filter</span></span>
<span data-ttu-id="d7dd1-112">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd1-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="d7dd1-113">-OrderBy</span></span>
<span data-ttu-id="d7dd1-114">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd1-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="d7dd1-115">-Skip</span></span>
<span data-ttu-id="d7dd1-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd1-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d7dd1-117">-Top</span></span>
<span data-ttu-id="d7dd1-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d7dd1-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd1-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="d7dd1-120">-InlineCount</span></span>
<span data-ttu-id="d7dd1-121">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7dd1-122">CommonParameters</span></span>
<span data-ttu-id="d7dd1-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7dd1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7dd1-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7dd1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7dd1-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7dd1-125">INPUTS</span></span>

## <span data-ttu-id="d7dd1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7dd1-126">OUTPUTS</span></span>

### <span data-ttu-id="d7dd1-127">Microsoft. AzureStack. Management. Network. admin. Models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7dd1-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="d7dd1-128">Note</span><span class="sxs-lookup"><span data-stu-id="d7dd1-128">NOTES</span></span>

## <span data-ttu-id="d7dd1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7dd1-129">RELATED LINKS</span></span>
