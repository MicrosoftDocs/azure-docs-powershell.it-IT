---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507115"
---
# <span data-ttu-id="fa6df-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="fa6df-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="fa6df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa6df-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6df-103">Restituisce un elenco di quote di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="fa6df-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="fa6df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa6df-104">SYNTAX</span></span>

### <span data-ttu-id="fa6df-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa6df-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fa6df-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="fa6df-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="fa6df-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa6df-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fa6df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa6df-108">DESCRIPTION</span></span>
<span data-ttu-id="fa6df-109">Restituisce un elenco di quote di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="fa6df-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="fa6df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa6df-110">EXAMPLES</span></span>

### <span data-ttu-id="fa6df-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fa6df-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="fa6df-112">Ottenere l'elenco delle quote di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fa6df-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="fa6df-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fa6df-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="fa6df-114">Ottenere i dettagli della quota di archiviazione specificata per nome.</span><span class="sxs-lookup"><span data-stu-id="fa6df-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="fa6df-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa6df-115">PARAMETERS</span></span>

### <span data-ttu-id="fa6df-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fa6df-116">-Location</span></span>
<span data-ttu-id="fa6df-117">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fa6df-117">Resource location.</span></span>

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

### <span data-ttu-id="fa6df-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa6df-118">-Name</span></span>
<span data-ttu-id="fa6df-119">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fa6df-119">The name of the storage quota.</span></span>

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

### <span data-ttu-id="fa6df-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa6df-120">-ResourceId</span></span>
<span data-ttu-id="fa6df-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="fa6df-121">The resource id.</span></span>

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

### <span data-ttu-id="fa6df-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="fa6df-122">-Skip</span></span>
<span data-ttu-id="fa6df-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="fa6df-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="fa6df-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="fa6df-124">-Top</span></span>
<span data-ttu-id="fa6df-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="fa6df-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fa6df-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="fa6df-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="fa6df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6df-127">CommonParameters</span></span>
<span data-ttu-id="fa6df-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa6df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6df-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa6df-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6df-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa6df-130">INPUTS</span></span>

## <span data-ttu-id="fa6df-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa6df-131">OUTPUTS</span></span>

### <span data-ttu-id="fa6df-132">Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente</span><span class="sxs-lookup"><span data-stu-id="fa6df-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="fa6df-133">Note</span><span class="sxs-lookup"><span data-stu-id="fa6df-133">NOTES</span></span>

## <span data-ttu-id="fa6df-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa6df-134">RELATED LINKS</span></span>

