---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030083"
---
# <span data-ttu-id="9f3f6-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f3f6-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="9f3f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3f6-103">Restituisce un elenco di tutti i pool di indirizzi MAC in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="9f3f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f3f6-104">SYNTAX</span></span>

### <span data-ttu-id="9f3f6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f3f6-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9f3f6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9f3f6-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9f3f6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f3f6-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9f3f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f3f6-108">DESCRIPTION</span></span>
<span data-ttu-id="9f3f6-109">Restituisce un elenco di tutti i pool di indirizzi MAC in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="9f3f6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f3f6-110">EXAMPLES</span></span>

### <span data-ttu-id="9f3f6-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="9f3f6-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="9f3f6-112">Ottenere tutti i pool di indirizzi MAC in una posizione.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="9f3f6-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="9f3f6-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="9f3f6-114">Ottenere uno specifico pool di indirizzi MAC in una posizione in base al nome.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="9f3f6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f3f6-115">PARAMETERS</span></span>

### <span data-ttu-id="9f3f6-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f3f6-116">-Name</span></span>
<span data-ttu-id="9f3f6-117">Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="9f3f6-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9f3f6-118">-Location</span></span>
<span data-ttu-id="9f3f6-119">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9f3f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f3f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f3f6-121">Gruppo di risorse in cui è stato registrato il provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9f3f6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f3f6-122">-ResourceId</span></span>
<span data-ttu-id="9f3f6-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-123">The resource id.</span></span>

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

### <span data-ttu-id="9f3f6-124">-Filtro</span><span class="sxs-lookup"><span data-stu-id="9f3f6-124">-Filter</span></span>
<span data-ttu-id="9f3f6-125">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="9f3f6-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="9f3f6-126">-Skip</span></span>
<span data-ttu-id="9f3f6-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9f3f6-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="9f3f6-128">-Top</span></span>
<span data-ttu-id="9f3f6-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9f3f6-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9f3f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3f6-131">CommonParameters</span></span>
<span data-ttu-id="9f3f6-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f3f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3f6-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f3f6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3f6-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f3f6-134">INPUTS</span></span>

## <span data-ttu-id="9f3f6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f3f6-135">OUTPUTS</span></span>

### <span data-ttu-id="9f3f6-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f3f6-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="9f3f6-137">Note</span><span class="sxs-lookup"><span data-stu-id="9f3f6-137">NOTES</span></span>

## <span data-ttu-id="9f3f6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f3f6-138">RELATED LINKS</span></span>
