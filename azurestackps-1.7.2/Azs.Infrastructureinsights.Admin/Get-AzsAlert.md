---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858602"
---
# <span data-ttu-id="5091d-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="5091d-101">Get-AzsAlert</span></span>

## <span data-ttu-id="5091d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5091d-102">SYNOPSIS</span></span>
<span data-ttu-id="5091d-103">Restituisce l'elenco di tutti gli avvisi in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="5091d-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="5091d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5091d-104">SYNTAX</span></span>

### <span data-ttu-id="5091d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5091d-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5091d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5091d-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5091d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5091d-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5091d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5091d-108">DESCRIPTION</span></span>
<span data-ttu-id="5091d-109">Restituisce l'elenco di tutti gli avvisi in una determinata posizione.</span><span class="sxs-lookup"><span data-stu-id="5091d-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="5091d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5091d-110">EXAMPLES</span></span>

### <span data-ttu-id="5091d-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5091d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="5091d-112">Ottenere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="5091d-112">Get an alert by Name.</span></span>

### <span data-ttu-id="5091d-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5091d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="5091d-114">Ottenere tutti gli avvisi attivi e visualizzare il loro errore e il loro titolo.</span><span class="sxs-lookup"><span data-stu-id="5091d-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="5091d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5091d-115">PARAMETERS</span></span>

### <span data-ttu-id="5091d-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="5091d-116">-Filter</span></span>
<span data-ttu-id="5091d-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="5091d-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="5091d-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5091d-118">-Location</span></span>
<span data-ttu-id="5091d-119">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="5091d-119">Name of the location.</span></span>

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

### <span data-ttu-id="5091d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5091d-120">-Name</span></span>
<span data-ttu-id="5091d-121">Identificatore avviso.</span><span class="sxs-lookup"><span data-stu-id="5091d-121">The alert identifier.</span></span>

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

### <span data-ttu-id="5091d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5091d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5091d-123">Nome del gruppo di risorse che la risorsa risiede.</span><span class="sxs-lookup"><span data-stu-id="5091d-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="5091d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5091d-124">-ResourceId</span></span>
<span data-ttu-id="5091d-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5091d-125">The resource id.</span></span>

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

### <span data-ttu-id="5091d-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="5091d-126">-Skip</span></span>
<span data-ttu-id="5091d-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="5091d-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5091d-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="5091d-128">-Top</span></span>
<span data-ttu-id="5091d-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="5091d-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5091d-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="5091d-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5091d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5091d-131">CommonParameters</span></span>
<span data-ttu-id="5091d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5091d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5091d-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5091d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5091d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5091d-134">INPUTS</span></span>

## <span data-ttu-id="5091d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5091d-135">OUTPUTS</span></span>

### <span data-ttu-id="5091d-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. Alert</span><span class="sxs-lookup"><span data-stu-id="5091d-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="5091d-137">Note</span><span class="sxs-lookup"><span data-stu-id="5091d-137">NOTES</span></span>

## <span data-ttu-id="5091d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5091d-138">RELATED LINKS</span></span>

