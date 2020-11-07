---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859106"
---
# <span data-ttu-id="c3275-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="c3275-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="c3275-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3275-102">SYNOPSIS</span></span>
<span data-ttu-id="c3275-103">Restituisce un elenco dell'integrità di ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="c3275-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="c3275-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3275-104">SYNTAX</span></span>

### <span data-ttu-id="c3275-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3275-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c3275-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c3275-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c3275-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3275-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c3275-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3275-108">DESCRIPTION</span></span>
<span data-ttu-id="c3275-109">Restituisce un elenco dell'integrità di ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="c3275-109">Returns a list of each service's health.</span></span> <span data-ttu-id="c3275-110">La proprietà AlertSummary include dettagli sui conteggi di avviso/errore.</span><span class="sxs-lookup"><span data-stu-id="c3275-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="c3275-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3275-111">EXAMPLES</span></span>

### <span data-ttu-id="c3275-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="c3275-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="c3275-113">Restituisce un elenco dell'integrità di ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="c3275-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="c3275-114">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="c3275-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="c3275-115">Restituisce l'integrità di un servizio.</span><span class="sxs-lookup"><span data-stu-id="c3275-115">Returns a service's health.</span></span>

## <span data-ttu-id="c3275-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3275-116">PARAMETERS</span></span>

### <span data-ttu-id="c3275-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3275-117">-Name</span></span>
<span data-ttu-id="c3275-118">Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="c3275-118">Service Health name.</span></span>

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

### <span data-ttu-id="c3275-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c3275-119">-Location</span></span>
<span data-ttu-id="c3275-120">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="c3275-120">Name of the region</span></span>

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

### <span data-ttu-id="c3275-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3275-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3275-122">Nome del gruppo di risorse facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c3275-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="c3275-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3275-123">-ResourceId</span></span>
<span data-ttu-id="c3275-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c3275-124">The resource id.</span></span>

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

### <span data-ttu-id="c3275-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="c3275-125">-Filter</span></span>
<span data-ttu-id="c3275-126">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="c3275-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="c3275-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="c3275-127">-Skip</span></span>
<span data-ttu-id="c3275-128">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c3275-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c3275-129">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="c3275-129">-Top</span></span>
<span data-ttu-id="c3275-130">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="c3275-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c3275-131">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="c3275-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c3275-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3275-132">CommonParameters</span></span>
<span data-ttu-id="c3275-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3275-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3275-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3275-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3275-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3275-135">INPUTS</span></span>

## <span data-ttu-id="c3275-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3275-136">OUTPUTS</span></span>

### <span data-ttu-id="c3275-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="c3275-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="c3275-138">Note</span><span class="sxs-lookup"><span data-stu-id="c3275-138">NOTES</span></span>

## <span data-ttu-id="c3275-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3275-139">RELATED LINKS</span></span>
