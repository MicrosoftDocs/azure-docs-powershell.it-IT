---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491125"
---
# <span data-ttu-id="21267-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="21267-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="21267-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21267-102">SYNOPSIS</span></span>
<span data-ttu-id="21267-103">Restituisce un elenco dell'integrità di ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="21267-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="21267-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21267-104">SYNTAX</span></span>

### <span data-ttu-id="21267-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21267-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="21267-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="21267-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="21267-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="21267-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="21267-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21267-108">DESCRIPTION</span></span>
<span data-ttu-id="21267-109">Restituisce un elenco dell'integrità di ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="21267-109">Returns a list of each service's health.</span></span> <span data-ttu-id="21267-110">La proprietà AlertSummary include dettagli sui conteggi di avviso/errore.</span><span class="sxs-lookup"><span data-stu-id="21267-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="21267-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21267-111">EXAMPLES</span></span>

### <span data-ttu-id="21267-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="21267-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="21267-113">Restituisce un elenco dell'integrità di ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="21267-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="21267-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="21267-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="21267-115">Restituisce l'integrità di un servizio.</span><span class="sxs-lookup"><span data-stu-id="21267-115">Returns a service's health.</span></span>

## <span data-ttu-id="21267-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21267-116">PARAMETERS</span></span>

### <span data-ttu-id="21267-117">-Filtro</span><span class="sxs-lookup"><span data-stu-id="21267-117">-Filter</span></span>
<span data-ttu-id="21267-118">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="21267-118">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21267-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="21267-119">-Location</span></span>
<span data-ttu-id="21267-120">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="21267-120">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21267-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="21267-121">-Name</span></span>
<span data-ttu-id="21267-122">Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="21267-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21267-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21267-123">-ResourceGroupName</span></span>
<span data-ttu-id="21267-124">Nome del gruppo di risorse che la risorsa risiede.</span><span class="sxs-lookup"><span data-stu-id="21267-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21267-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21267-125">-ResourceId</span></span>
<span data-ttu-id="21267-126">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="21267-126">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21267-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="21267-127">-Skip</span></span>
<span data-ttu-id="21267-128">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="21267-128">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21267-129">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="21267-129">-Top</span></span>
<span data-ttu-id="21267-130">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="21267-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="21267-131">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="21267-131">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21267-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21267-132">CommonParameters</span></span>
<span data-ttu-id="21267-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21267-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21267-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21267-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21267-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21267-135">INPUTS</span></span>

## <span data-ttu-id="21267-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21267-136">OUTPUTS</span></span>

### <span data-ttu-id="21267-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="21267-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="21267-138">Note</span><span class="sxs-lookup"><span data-stu-id="21267-138">NOTES</span></span>

## <span data-ttu-id="21267-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21267-139">RELATED LINKS</span></span>

