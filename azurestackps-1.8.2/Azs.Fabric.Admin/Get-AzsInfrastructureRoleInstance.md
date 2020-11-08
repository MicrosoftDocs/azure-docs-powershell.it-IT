---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030559"
---
# <span data-ttu-id="97534-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="97534-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="97534-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97534-102">SYNOPSIS</span></span>
<span data-ttu-id="97534-103">Restituisce un elenco di tutte le istanze del ruolo dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="97534-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="97534-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97534-104">SYNTAX</span></span>

### <span data-ttu-id="97534-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97534-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="97534-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="97534-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="97534-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="97534-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="97534-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97534-108">DESCRIPTION</span></span>
<span data-ttu-id="97534-109">Restituisce un elenco di tutte le istanze del ruolo dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="97534-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="97534-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97534-110">EXAMPLES</span></span>

### <span data-ttu-id="97534-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="97534-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="97534-112">Restituisce un elenco di tutte le istanze del ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="97534-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="97534-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="97534-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="97534-114">Restituisce una singola istanza del ruolo dell'infrastruttura in base al nome.</span><span class="sxs-lookup"><span data-stu-id="97534-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="97534-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97534-115">PARAMETERS</span></span>

### <span data-ttu-id="97534-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="97534-116">-Name</span></span>
<span data-ttu-id="97534-117">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="97534-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="97534-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="97534-118">-Location</span></span>
<span data-ttu-id="97534-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="97534-119">Location of the resource.</span></span>

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

### <span data-ttu-id="97534-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97534-120">-ResourceGroupName</span></span>
<span data-ttu-id="97534-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="97534-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="97534-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97534-122">-ResourceId</span></span>
<span data-ttu-id="97534-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="97534-123">The resource id.</span></span>

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

### <span data-ttu-id="97534-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="97534-124">-Filter</span></span>
<span data-ttu-id="97534-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="97534-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="97534-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="97534-126">-Skip</span></span>
<span data-ttu-id="97534-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="97534-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="97534-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="97534-128">-Top</span></span>
<span data-ttu-id="97534-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="97534-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="97534-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="97534-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="97534-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97534-131">CommonParameters</span></span>
<span data-ttu-id="97534-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97534-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97534-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97534-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97534-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97534-134">INPUTS</span></span>

## <span data-ttu-id="97534-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97534-135">OUTPUTS</span></span>

### <span data-ttu-id="97534-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="97534-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="97534-137">Note</span><span class="sxs-lookup"><span data-stu-id="97534-137">NOTES</span></span>

## <span data-ttu-id="97534-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97534-138">RELATED LINKS</span></span>
