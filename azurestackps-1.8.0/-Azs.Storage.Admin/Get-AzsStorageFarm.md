---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 419bddaaa121e052b486bf4bb5408fcae6160fd4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859377"
---
# <span data-ttu-id="6a88e-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="6a88e-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="6a88e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a88e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a88e-103">Restituisce un elenco di tutte le farm di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a88e-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="6a88e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a88e-104">SYNTAX</span></span>

### <span data-ttu-id="6a88e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a88e-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6a88e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="6a88e-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6a88e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a88e-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6a88e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a88e-108">DESCRIPTION</span></span>
<span data-ttu-id="6a88e-109">Restituisce un elenco di tutte le farm di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a88e-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="6a88e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a88e-110">EXAMPLES</span></span>

### <span data-ttu-id="6a88e-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a88e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="6a88e-112">Ottenere l'elenco di tutte le farm di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a88e-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="6a88e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a88e-113">PARAMETERS</span></span>

### <span data-ttu-id="6a88e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a88e-114">-Name</span></span>
<span data-ttu-id="6a88e-115">ID farm.</span><span class="sxs-lookup"><span data-stu-id="6a88e-115">Farm Id.</span></span>

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

### <span data-ttu-id="6a88e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a88e-116">-ResourceGroupName</span></span>
<span data-ttu-id="6a88e-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a88e-117">Resource group name.</span></span>

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

### <span data-ttu-id="6a88e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a88e-118">-ResourceId</span></span>
<span data-ttu-id="6a88e-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a88e-119">The resource id.</span></span>

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

### <span data-ttu-id="6a88e-120">-Skip</span><span class="sxs-lookup"><span data-stu-id="6a88e-120">-Skip</span></span>
<span data-ttu-id="6a88e-121">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6a88e-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6a88e-122">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="6a88e-122">-Top</span></span>
<span data-ttu-id="6a88e-123">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="6a88e-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6a88e-124">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="6a88e-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6a88e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a88e-125">CommonParameters</span></span>
<span data-ttu-id="6a88e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a88e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a88e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a88e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a88e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a88e-128">INPUTS</span></span>

## <span data-ttu-id="6a88e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a88e-129">OUTPUTS</span></span>

### <span data-ttu-id="6a88e-130">Microsoft. AzureStack. Management. storage. admin. Models. farm</span><span class="sxs-lookup"><span data-stu-id="6a88e-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="6a88e-131">Note</span><span class="sxs-lookup"><span data-stu-id="6a88e-131">NOTES</span></span>

## <span data-ttu-id="6a88e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a88e-132">RELATED LINKS</span></span>

