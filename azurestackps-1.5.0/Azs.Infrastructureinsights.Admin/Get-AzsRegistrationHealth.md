---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685187"
---
# <span data-ttu-id="45e04-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="45e04-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="45e04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45e04-102">SYNOPSIS</span></span>
<span data-ttu-id="45e04-103">Restituisce un elenco dell'integrità di ogni risorsa in un servizio.</span><span class="sxs-lookup"><span data-stu-id="45e04-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="45e04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45e04-104">SYNTAX</span></span>

### <span data-ttu-id="45e04-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45e04-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="45e04-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="45e04-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="45e04-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="45e04-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="45e04-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45e04-108">DESCRIPTION</span></span>
<span data-ttu-id="45e04-109">Restituisce un elenco dell'integrità di ogni risorsa in un servizio.</span><span class="sxs-lookup"><span data-stu-id="45e04-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="45e04-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45e04-110">EXAMPLES</span></span>

### <span data-ttu-id="45e04-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="45e04-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="45e04-112">Restituisce un elenco dell'integrità di ogni risorsa in un servizio.</span><span class="sxs-lookup"><span data-stu-id="45e04-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="45e04-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="45e04-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="45e04-114">Restituisce lo stato di integrità in un oggetto for Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="45e04-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="45e04-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45e04-115">PARAMETERS</span></span>

### <span data-ttu-id="45e04-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="45e04-116">-Filter</span></span>
<span data-ttu-id="45e04-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="45e04-117">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e04-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="45e04-118">-Location</span></span>
<span data-ttu-id="45e04-119">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="45e04-119">Name of the region</span></span>

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

### <span data-ttu-id="45e04-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="45e04-120">-Name</span></span>
<span data-ttu-id="45e04-121">Nome della risorsa dell'oggetto integrità che corrisponde all'ID di registrazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="45e04-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e04-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e04-122">-ResourceGroupName</span></span>
<span data-ttu-id="45e04-123">Nome del gruppo di risorse che la risorsa risiede.</span><span class="sxs-lookup"><span data-stu-id="45e04-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="45e04-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45e04-124">-ResourceId</span></span>
<span data-ttu-id="45e04-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="45e04-125">The resource id.</span></span>

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

### <span data-ttu-id="45e04-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="45e04-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="45e04-127">ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="45e04-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e04-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="45e04-128">-Skip</span></span>
<span data-ttu-id="45e04-129">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="45e04-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="45e04-130">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="45e04-130">-Top</span></span>
<span data-ttu-id="45e04-131">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="45e04-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45e04-132">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="45e04-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="45e04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e04-133">CommonParameters</span></span>
<span data-ttu-id="45e04-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e04-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e04-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e04-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45e04-136">INPUTS</span></span>

## <span data-ttu-id="45e04-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45e04-137">OUTPUTS</span></span>

### <span data-ttu-id="45e04-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="45e04-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="45e04-139">Note</span><span class="sxs-lookup"><span data-stu-id="45e04-139">NOTES</span></span>

## <span data-ttu-id="45e04-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45e04-140">RELATED LINKS</span></span>

