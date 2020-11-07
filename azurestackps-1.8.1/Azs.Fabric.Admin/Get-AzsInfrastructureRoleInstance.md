---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c5fe6e28ff87cfd3f365441d0e09f09ef21dc454
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859658"
---
# <span data-ttu-id="d4b7a-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="d4b7a-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="d4b7a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b7a-103">Restituisce un elenco di tutte le istanze del ruolo dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="d4b7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4b7a-104">SYNTAX</span></span>

### <span data-ttu-id="d4b7a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4b7a-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d4b7a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d4b7a-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4b7a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b7a-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d4b7a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4b7a-108">DESCRIPTION</span></span>
<span data-ttu-id="d4b7a-109">Restituisce un elenco di tutte le istanze del ruolo dell'infrastruttura in una posizione.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="d4b7a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4b7a-110">EXAMPLES</span></span>

### <span data-ttu-id="d4b7a-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="d4b7a-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="d4b7a-112">Restituisce un elenco di tutte le istanze del ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="d4b7a-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="d4b7a-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="d4b7a-114">Restituisce una singola istanza del ruolo dell'infrastruttura in base al nome.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="d4b7a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4b7a-115">PARAMETERS</span></span>

### <span data-ttu-id="d4b7a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4b7a-116">-Name</span></span>
<span data-ttu-id="d4b7a-117">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-117">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="d4b7a-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d4b7a-118">-Location</span></span>
<span data-ttu-id="d4b7a-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="d4b7a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b7a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d4b7a-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d4b7a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b7a-122">-ResourceId</span></span>
<span data-ttu-id="d4b7a-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-123">The resource id.</span></span>

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

### <span data-ttu-id="d4b7a-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d4b7a-124">-Filter</span></span>
<span data-ttu-id="d4b7a-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="d4b7a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="d4b7a-126">-Skip</span></span>
<span data-ttu-id="d4b7a-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d4b7a-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d4b7a-128">-Top</span></span>
<span data-ttu-id="d4b7a-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d4b7a-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d4b7a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b7a-131">CommonParameters</span></span>
<span data-ttu-id="d4b7a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b7a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b7a-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b7a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b7a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4b7a-134">INPUTS</span></span>

## <span data-ttu-id="d4b7a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4b7a-135">OUTPUTS</span></span>

### <span data-ttu-id="d4b7a-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="d4b7a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="d4b7a-137">Note</span><span class="sxs-lookup"><span data-stu-id="d4b7a-137">NOTES</span></span>

## <span data-ttu-id="d4b7a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4b7a-138">RELATED LINKS</span></span>
