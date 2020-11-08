---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030378"
---
# <span data-ttu-id="84422-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="84422-101">Get-AzsAlert</span></span>

## <span data-ttu-id="84422-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84422-102">SYNOPSIS</span></span>
<span data-ttu-id="84422-103">Restituisce l'elenco di tutti gli avvisi in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="84422-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="84422-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84422-104">SYNTAX</span></span>

### <span data-ttu-id="84422-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84422-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="84422-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="84422-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="84422-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="84422-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="84422-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84422-108">DESCRIPTION</span></span>
<span data-ttu-id="84422-109">Restituisce l'elenco di tutti gli avvisi in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="84422-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="84422-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84422-110">EXAMPLES</span></span>

### <span data-ttu-id="84422-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="84422-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="84422-112">Ottenere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="84422-112">Get an alert by Name.</span></span>

### <span data-ttu-id="84422-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="84422-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="84422-114">Ottenere tutti gli avvisi attivi e visualizzare il loro errore e il loro titolo.</span><span class="sxs-lookup"><span data-stu-id="84422-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="84422-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84422-115">PARAMETERS</span></span>

### <span data-ttu-id="84422-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="84422-116">-Name</span></span>
<span data-ttu-id="84422-117">Identificatore avviso.</span><span class="sxs-lookup"><span data-stu-id="84422-117">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84422-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="84422-118">-Location</span></span>
<span data-ttu-id="84422-119">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="84422-119">Name of the location.</span></span>

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

### <span data-ttu-id="84422-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84422-120">-ResourceGroupName</span></span>
<span data-ttu-id="84422-121">Nome del gruppo di risorse dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="84422-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="84422-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84422-122">-ResourceId</span></span>
<span data-ttu-id="84422-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="84422-123">The resource id.</span></span>

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

### <span data-ttu-id="84422-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="84422-124">-Filter</span></span>
<span data-ttu-id="84422-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="84422-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="84422-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="84422-126">-Top</span></span>
<span data-ttu-id="84422-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="84422-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="84422-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="84422-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="84422-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="84422-129">-Skip</span></span>
<span data-ttu-id="84422-130">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="84422-130">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="84422-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84422-131">CommonParameters</span></span>
<span data-ttu-id="84422-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84422-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84422-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84422-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84422-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84422-134">INPUTS</span></span>

## <span data-ttu-id="84422-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84422-135">OUTPUTS</span></span>

### <span data-ttu-id="84422-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="84422-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="84422-137">Note</span><span class="sxs-lookup"><span data-stu-id="84422-137">NOTES</span></span>

## <span data-ttu-id="84422-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84422-138">RELATED LINKS</span></span>
