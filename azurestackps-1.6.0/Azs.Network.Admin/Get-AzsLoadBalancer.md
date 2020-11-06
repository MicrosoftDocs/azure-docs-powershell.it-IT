---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87966f8ac96ab70f7617f857d9f1d83945b5e639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491361"
---
# <span data-ttu-id="eea38-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eea38-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="eea38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eea38-102">SYNOPSIS</span></span>
<span data-ttu-id="eea38-103">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="eea38-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="eea38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eea38-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="eea38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eea38-105">DESCRIPTION</span></span>
<span data-ttu-id="eea38-106">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="eea38-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="eea38-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eea38-107">EXAMPLES</span></span>

### <span data-ttu-id="eea38-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eea38-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="eea38-109">Ottenere un elenco di tutti i bilanciatori di carico.</span><span class="sxs-lookup"><span data-stu-id="eea38-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="eea38-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eea38-110">PARAMETERS</span></span>

### <span data-ttu-id="eea38-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="eea38-111">-Filter</span></span>
<span data-ttu-id="eea38-112">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="eea38-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="eea38-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="eea38-113">-InlineCount</span></span>
<span data-ttu-id="eea38-114">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="eea38-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="eea38-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="eea38-115">-OrderBy</span></span>
<span data-ttu-id="eea38-116">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="eea38-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="eea38-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="eea38-117">-Skip</span></span>
<span data-ttu-id="eea38-118">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="eea38-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="eea38-119">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="eea38-119">-Top</span></span>
<span data-ttu-id="eea38-120">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="eea38-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eea38-121">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="eea38-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="eea38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea38-122">CommonParameters</span></span>
<span data-ttu-id="eea38-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea38-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea38-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea38-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eea38-125">INPUTS</span></span>

## <span data-ttu-id="eea38-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eea38-126">OUTPUTS</span></span>

### <span data-ttu-id="eea38-127">Microsoft. AzureStack. Management. Network. admin. Models. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eea38-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="eea38-128">Note</span><span class="sxs-lookup"><span data-stu-id="eea38-128">NOTES</span></span>

## <span data-ttu-id="eea38-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eea38-129">RELATED LINKS</span></span>
