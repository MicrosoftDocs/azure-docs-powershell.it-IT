---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859878"
---
# <span data-ttu-id="70cec-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="70cec-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="70cec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70cec-102">SYNOPSIS</span></span>
<span data-ttu-id="70cec-103">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="70cec-103">List of public IP addresses.</span></span>

## <span data-ttu-id="70cec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70cec-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="70cec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70cec-105">DESCRIPTION</span></span>
<span data-ttu-id="70cec-106">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="70cec-106">List of public IP addresses.</span></span>

## <span data-ttu-id="70cec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70cec-107">EXAMPLES</span></span>

### <span data-ttu-id="70cec-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="70cec-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="70cec-109">Ottenere l'elenco degli indirizzi IP pubblici, assegnati o non assegnati.</span><span class="sxs-lookup"><span data-stu-id="70cec-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="70cec-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70cec-110">PARAMETERS</span></span>

### <span data-ttu-id="70cec-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="70cec-111">-Filter</span></span>
<span data-ttu-id="70cec-112">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="70cec-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="70cec-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="70cec-113">-OrderBy</span></span>
<span data-ttu-id="70cec-114">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="70cec-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="70cec-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="70cec-115">-Skip</span></span>
<span data-ttu-id="70cec-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="70cec-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="70cec-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="70cec-117">-Top</span></span>
<span data-ttu-id="70cec-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="70cec-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="70cec-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="70cec-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="70cec-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="70cec-120">-InlineCount</span></span>
<span data-ttu-id="70cec-121">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="70cec-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="70cec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70cec-122">CommonParameters</span></span>
<span data-ttu-id="70cec-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70cec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70cec-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70cec-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70cec-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70cec-125">INPUTS</span></span>

## <span data-ttu-id="70cec-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70cec-126">OUTPUTS</span></span>

### <span data-ttu-id="70cec-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="70cec-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="70cec-128">Note</span><span class="sxs-lookup"><span data-stu-id="70cec-128">NOTES</span></span>

## <span data-ttu-id="70cec-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70cec-129">RELATED LINKS</span></span>
