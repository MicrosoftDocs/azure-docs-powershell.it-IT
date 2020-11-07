---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dac95eced72f70d3471019136d302fcdfe95f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858670"
---
# <span data-ttu-id="bddf6-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="bddf6-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="bddf6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bddf6-102">SYNOPSIS</span></span>
<span data-ttu-id="bddf6-103">Restituisce un elenco di tutti i ruoli dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="bddf6-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="bddf6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bddf6-104">SYNTAX</span></span>

### <span data-ttu-id="bddf6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bddf6-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bddf6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bddf6-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bddf6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bddf6-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bddf6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bddf6-108">DESCRIPTION</span></span>
<span data-ttu-id="bddf6-109">Restituisce un elenco di tutti i ruoli dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="bddf6-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="bddf6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bddf6-110">EXAMPLES</span></span>

### <span data-ttu-id="bddf6-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bddf6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="bddf6-112">Ottenere un elenco di tutti i ruoli dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="bddf6-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="bddf6-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="bddf6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="bddf6-114">Ottenere un ruolo di infrastruttura basato sul nome.</span><span class="sxs-lookup"><span data-stu-id="bddf6-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="bddf6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bddf6-115">PARAMETERS</span></span>

### <span data-ttu-id="bddf6-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bddf6-116">-Filter</span></span>
<span data-ttu-id="bddf6-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="bddf6-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="bddf6-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bddf6-118">-Location</span></span>
<span data-ttu-id="bddf6-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bddf6-119">Location of the resource.</span></span>

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

### <span data-ttu-id="bddf6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bddf6-120">-Name</span></span>
<span data-ttu-id="bddf6-121">Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="bddf6-121">Infrastructure role name.</span></span>

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

### <span data-ttu-id="bddf6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bddf6-122">-ResourceGroupName</span></span>
<span data-ttu-id="bddf6-123">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="bddf6-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bddf6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bddf6-124">-ResourceId</span></span>
<span data-ttu-id="bddf6-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="bddf6-125">The resource id.</span></span>

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

### <span data-ttu-id="bddf6-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="bddf6-126">-Skip</span></span>
<span data-ttu-id="bddf6-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="bddf6-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bddf6-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="bddf6-128">-Top</span></span>
<span data-ttu-id="bddf6-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="bddf6-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bddf6-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="bddf6-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bddf6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bddf6-131">CommonParameters</span></span>
<span data-ttu-id="bddf6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bddf6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bddf6-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bddf6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bddf6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bddf6-134">INPUTS</span></span>

## <span data-ttu-id="bddf6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bddf6-135">OUTPUTS</span></span>

### <span data-ttu-id="bddf6-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="bddf6-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="bddf6-137">Note</span><span class="sxs-lookup"><span data-stu-id="bddf6-137">NOTES</span></span>

## <span data-ttu-id="bddf6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bddf6-138">RELATED LINKS</span></span>

