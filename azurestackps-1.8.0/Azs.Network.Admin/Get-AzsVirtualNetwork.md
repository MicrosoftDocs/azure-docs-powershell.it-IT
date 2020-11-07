---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af35419f3e0b28be9782e7bbe5d4eaaf1cdf0807
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859298"
---
# <span data-ttu-id="08970-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08970-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="08970-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08970-102">SYNOPSIS</span></span>
<span data-ttu-id="08970-103">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="08970-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="08970-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08970-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="08970-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08970-105">DESCRIPTION</span></span>
<span data-ttu-id="08970-106">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="08970-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="08970-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08970-107">EXAMPLES</span></span>

### <span data-ttu-id="08970-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="08970-108">EXAMPLE 1</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="08970-109">Restituisce un elenco di reti virtuali per l'indicatore dello stack di Azure.</span><span class="sxs-lookup"><span data-stu-id="08970-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="08970-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08970-110">PARAMETERS</span></span>

### <span data-ttu-id="08970-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="08970-111">-Filter</span></span>
<span data-ttu-id="08970-112">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="08970-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="08970-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="08970-113">-OrderBy</span></span>
<span data-ttu-id="08970-114">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="08970-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="08970-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="08970-115">-Skip</span></span>
<span data-ttu-id="08970-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="08970-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="08970-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="08970-117">-Top</span></span>
<span data-ttu-id="08970-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="08970-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="08970-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="08970-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="08970-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="08970-120">-InlineCount</span></span>
<span data-ttu-id="08970-121">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="08970-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="08970-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08970-122">CommonParameters</span></span>
<span data-ttu-id="08970-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08970-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08970-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08970-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08970-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08970-125">INPUTS</span></span>

## <span data-ttu-id="08970-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08970-126">OUTPUTS</span></span>

### <span data-ttu-id="08970-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="08970-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="08970-128">Note</span><span class="sxs-lookup"><span data-stu-id="08970-128">NOTES</span></span>

## <span data-ttu-id="08970-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08970-129">RELATED LINKS</span></span>
