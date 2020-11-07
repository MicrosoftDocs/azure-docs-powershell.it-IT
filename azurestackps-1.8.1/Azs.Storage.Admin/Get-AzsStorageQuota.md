---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 687838573459c09ceaf08c0d1c3335caa4a99769
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859753"
---
# <span data-ttu-id="cec4b-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="cec4b-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="cec4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cec4b-102">SYNOPSIS</span></span>
<span data-ttu-id="cec4b-103">Restituisce un elenco di quote di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="cec4b-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="cec4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cec4b-104">SYNTAX</span></span>

### <span data-ttu-id="cec4b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cec4b-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cec4b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cec4b-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="cec4b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cec4b-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cec4b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cec4b-108">DESCRIPTION</span></span>
<span data-ttu-id="cec4b-109">Restituisce un elenco di quote di archiviazione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="cec4b-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="cec4b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cec4b-110">EXAMPLES</span></span>

### <span data-ttu-id="cec4b-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="cec4b-111">EXAMPLE 1</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="cec4b-112">Ottenere l'elenco delle quote di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cec4b-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="cec4b-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="cec4b-113">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="cec4b-114">Ottenere i dettagli della quota di archiviazione specificata per nome.</span><span class="sxs-lookup"><span data-stu-id="cec4b-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="cec4b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cec4b-115">PARAMETERS</span></span>

### <span data-ttu-id="cec4b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="cec4b-116">-Name</span></span>
<span data-ttu-id="cec4b-117">Nome della quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cec4b-117">The name of the storage quota.</span></span>

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

### <span data-ttu-id="cec4b-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cec4b-118">-Location</span></span>
<span data-ttu-id="cec4b-119">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="cec4b-119">Resource location.</span></span>

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

### <span data-ttu-id="cec4b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cec4b-120">-ResourceId</span></span>
<span data-ttu-id="cec4b-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="cec4b-121">The resource id.</span></span>

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

### <span data-ttu-id="cec4b-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="cec4b-122">-Skip</span></span>
<span data-ttu-id="cec4b-123">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="cec4b-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cec4b-124">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="cec4b-124">-Top</span></span>
<span data-ttu-id="cec4b-125">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="cec4b-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cec4b-126">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="cec4b-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cec4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec4b-127">CommonParameters</span></span>
<span data-ttu-id="cec4b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cec4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec4b-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cec4b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec4b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cec4b-130">INPUTS</span></span>

## <span data-ttu-id="cec4b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cec4b-131">OUTPUTS</span></span>

### <span data-ttu-id="cec4b-132">Microsoft. AzureStack. Management. storage. admin. Models. StorageQuota consente</span><span class="sxs-lookup"><span data-stu-id="cec4b-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="cec4b-133">Note</span><span class="sxs-lookup"><span data-stu-id="cec4b-133">NOTES</span></span>

## <span data-ttu-id="cec4b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cec4b-134">RELATED LINKS</span></span>
