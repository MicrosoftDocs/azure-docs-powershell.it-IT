---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43691cfa3299fc0534ce2d44fd2a2f6ed1043d04
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491109"
---
# <span data-ttu-id="7c45a-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c45a-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="7c45a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c45a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c45a-103">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="7c45a-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="7c45a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c45a-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c45a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c45a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c45a-106">Ottenere un elenco di tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="7c45a-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="7c45a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c45a-107">EXAMPLES</span></span>

### <span data-ttu-id="7c45a-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c45a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVirtualNetwork
```

<span data-ttu-id="7c45a-109">Restituisce un elenco di reti virtuali per l'indicatore dello stack di Azure.</span><span class="sxs-lookup"><span data-stu-id="7c45a-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="7c45a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c45a-110">PARAMETERS</span></span>

### <span data-ttu-id="7c45a-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="7c45a-111">-Filter</span></span>
<span data-ttu-id="7c45a-112">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="7c45a-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="7c45a-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="7c45a-113">-InlineCount</span></span>
<span data-ttu-id="7c45a-114">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="7c45a-114">OData inline count parameter.</span></span>

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

### <span data-ttu-id="7c45a-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="7c45a-115">-OrderBy</span></span>
<span data-ttu-id="7c45a-116">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="7c45a-116">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="7c45a-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="7c45a-117">-Skip</span></span>
<span data-ttu-id="7c45a-118">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="7c45a-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7c45a-119">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="7c45a-119">-Top</span></span>
<span data-ttu-id="7c45a-120">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="7c45a-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7c45a-121">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="7c45a-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7c45a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c45a-122">CommonParameters</span></span>
<span data-ttu-id="7c45a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c45a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c45a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c45a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c45a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c45a-125">INPUTS</span></span>

## <span data-ttu-id="7c45a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c45a-126">OUTPUTS</span></span>

### <span data-ttu-id="7c45a-127">Microsoft. AzureStack. Management. Network. admin. Models. VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c45a-127">Microsoft.AzureStack.Management.Network.Admin.Models.VirtualNetwork</span></span>

## <span data-ttu-id="7c45a-128">Note</span><span class="sxs-lookup"><span data-stu-id="7c45a-128">NOTES</span></span>

## <span data-ttu-id="7c45a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c45a-129">RELATED LINKS</span></span>
