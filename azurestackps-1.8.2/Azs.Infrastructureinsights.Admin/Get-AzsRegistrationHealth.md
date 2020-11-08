---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030571"
---
# <span data-ttu-id="eea4c-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="eea4c-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="eea4c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eea4c-102">SYNOPSIS</span></span>
<span data-ttu-id="eea4c-103">Restituisce un elenco dell'integrità di ogni risorsa in un servizio.</span><span class="sxs-lookup"><span data-stu-id="eea4c-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="eea4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eea4c-104">SYNTAX</span></span>

### <span data-ttu-id="eea4c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eea4c-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eea4c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="eea4c-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="eea4c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea4c-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="eea4c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eea4c-108">DESCRIPTION</span></span>
<span data-ttu-id="eea4c-109">Restituisce un elenco dell'integrità di ogni risorsa in un servizio.</span><span class="sxs-lookup"><span data-stu-id="eea4c-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="eea4c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eea4c-110">EXAMPLES</span></span>

### <span data-ttu-id="eea4c-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="eea4c-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="eea4c-112">Restituisce un elenco dell'integrità di ogni risorsa in un servizio.</span><span class="sxs-lookup"><span data-stu-id="eea4c-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="eea4c-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="eea4c-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="eea4c-114">Restituisce lo stato di integrità in un oggetto for Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="eea4c-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="eea4c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eea4c-115">PARAMETERS</span></span>

### <span data-ttu-id="eea4c-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="eea4c-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="eea4c-117">ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="eea4c-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea4c-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="eea4c-118">-ResourceRegistrationId</span></span>


```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea4c-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="eea4c-119">-Location</span></span>
<span data-ttu-id="eea4c-120">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="eea4c-120">Name of the region</span></span>

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

### <span data-ttu-id="eea4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="eea4c-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eea4c-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="eea4c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eea4c-123">-ResourceId</span></span>
<span data-ttu-id="eea4c-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="eea4c-124">The resource id.</span></span>

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

### <span data-ttu-id="eea4c-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="eea4c-125">-Filter</span></span>
<span data-ttu-id="eea4c-126">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="eea4c-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="eea4c-127">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="eea4c-127">-Top</span></span>
<span data-ttu-id="eea4c-128">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="eea4c-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eea4c-129">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="eea4c-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="eea4c-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="eea4c-130">-Skip</span></span>
<span data-ttu-id="eea4c-131">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="eea4c-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="eea4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea4c-132">CommonParameters</span></span>
<span data-ttu-id="eea4c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eea4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea4c-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea4c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea4c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eea4c-135">INPUTS</span></span>

## <span data-ttu-id="eea4c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eea4c-136">OUTPUTS</span></span>

### <span data-ttu-id="eea4c-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="eea4c-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="eea4c-138">Note</span><span class="sxs-lookup"><span data-stu-id="eea4c-138">NOTES</span></span>

## <span data-ttu-id="eea4c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eea4c-139">RELATED LINKS</span></span>
