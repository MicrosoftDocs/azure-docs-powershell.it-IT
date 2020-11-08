---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af3edc04e7db61fa43aa4b192d4bc29d0ec47640
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030452"
---
# <span data-ttu-id="103ce-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="103ce-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="103ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="103ce-102">SYNOPSIS</span></span>
<span data-ttu-id="103ce-103">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="103ce-103">List of public IP addresses.</span></span>

## <span data-ttu-id="103ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="103ce-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="103ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="103ce-105">DESCRIPTION</span></span>
<span data-ttu-id="103ce-106">Elenco di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="103ce-106">List of public IP addresses.</span></span>

## <span data-ttu-id="103ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="103ce-107">EXAMPLES</span></span>

### <span data-ttu-id="103ce-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="103ce-108">EXAMPLE 1</span></span>
```
Get-AzsPublicIPAddress
```

<span data-ttu-id="103ce-109">Ottenere l'elenco degli indirizzi IP pubblici, assegnati o non assegnati.</span><span class="sxs-lookup"><span data-stu-id="103ce-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="103ce-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="103ce-110">PARAMETERS</span></span>

### <span data-ttu-id="103ce-111">-Filtro</span><span class="sxs-lookup"><span data-stu-id="103ce-111">-Filter</span></span>
<span data-ttu-id="103ce-112">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="103ce-112">OData filter parameter.</span></span>

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

### <span data-ttu-id="103ce-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="103ce-113">-OrderBy</span></span>
<span data-ttu-id="103ce-114">Parametro orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="103ce-114">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="103ce-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="103ce-115">-Skip</span></span>
<span data-ttu-id="103ce-116">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="103ce-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="103ce-117">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="103ce-117">-Top</span></span>
<span data-ttu-id="103ce-118">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="103ce-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="103ce-119">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="103ce-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="103ce-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="103ce-120">-InlineCount</span></span>
<span data-ttu-id="103ce-121">Parametro conteggio inline OData.</span><span class="sxs-lookup"><span data-stu-id="103ce-121">OData inline count parameter.</span></span>

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

### <span data-ttu-id="103ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103ce-122">CommonParameters</span></span>
<span data-ttu-id="103ce-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103ce-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="103ce-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103ce-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="103ce-125">INPUTS</span></span>

## <span data-ttu-id="103ce-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="103ce-126">OUTPUTS</span></span>

### <span data-ttu-id="103ce-127">Microsoft. AzureStack. Management. Network. admin. Models. PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="103ce-127">Microsoft.AzureStack.Management.Network.Admin.Models.PublicIpAddress</span></span>

## <span data-ttu-id="103ce-128">Note</span><span class="sxs-lookup"><span data-stu-id="103ce-128">NOTES</span></span>

## <span data-ttu-id="103ce-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="103ce-129">RELATED LINKS</span></span>
