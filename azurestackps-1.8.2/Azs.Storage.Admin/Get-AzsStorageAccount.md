---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4ec0639e31df3766550d6f7acc655cd3b5608bf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030355"
---
# <span data-ttu-id="a369e-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a369e-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="a369e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a369e-102">SYNOPSIS</span></span>
<span data-ttu-id="a369e-103">Restituisce l'account di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="a369e-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="a369e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a369e-104">SYNTAX</span></span>

### <span data-ttu-id="a369e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a369e-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a369e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="a369e-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a369e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a369e-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a369e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a369e-108">DESCRIPTION</span></span>
<span data-ttu-id="a369e-109">Restituisce l'account di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="a369e-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="a369e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a369e-110">EXAMPLES</span></span>

### <span data-ttu-id="a369e-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="a369e-111">EXAMPLE 1</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="a369e-112">Ottenere un elenco di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a369e-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="a369e-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="a369e-113">EXAMPLE 2</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="a369e-114">Ottenere i dettagli dell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a369e-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="a369e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a369e-115">PARAMETERS</span></span>

### <span data-ttu-id="a369e-116">-Farmname</span><span class="sxs-lookup"><span data-stu-id="a369e-116">-FarmName</span></span>
<span data-ttu-id="a369e-117">ID farm.</span><span class="sxs-lookup"><span data-stu-id="a369e-117">Farm Id.</span></span>

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

### <span data-ttu-id="a369e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a369e-118">-Name</span></span>
<span data-ttu-id="a369e-119">ID account di archiviazione interno, che non è visibile al tenant.</span><span class="sxs-lookup"><span data-stu-id="a369e-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a369e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a369e-120">-ResourceGroupName</span></span>
<span data-ttu-id="a369e-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a369e-121">Resource group name.</span></span>

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

### <span data-ttu-id="a369e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a369e-122">-ResourceId</span></span>
<span data-ttu-id="a369e-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a369e-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a369e-124">-Riepilogo</span><span class="sxs-lookup"><span data-stu-id="a369e-124">-Summary</span></span>
<span data-ttu-id="a369e-125">Viene restituita l'opzione per il riepilogo di wheter o per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="a369e-125">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a369e-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="a369e-126">-Skip</span></span>
<span data-ttu-id="a369e-127">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a369e-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a369e-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="a369e-128">-Top</span></span>
<span data-ttu-id="a369e-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="a369e-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a369e-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="a369e-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a369e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a369e-131">CommonParameters</span></span>
<span data-ttu-id="a369e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a369e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a369e-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a369e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a369e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a369e-134">INPUTS</span></span>

## <span data-ttu-id="a369e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a369e-135">OUTPUTS</span></span>

### <span data-ttu-id="a369e-136">Microsoft. AzureStack. Management. storage. admin. Models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a369e-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="a369e-137">Note</span><span class="sxs-lookup"><span data-stu-id="a369e-137">NOTES</span></span>

## <span data-ttu-id="a369e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a369e-138">RELATED LINKS</span></span>
