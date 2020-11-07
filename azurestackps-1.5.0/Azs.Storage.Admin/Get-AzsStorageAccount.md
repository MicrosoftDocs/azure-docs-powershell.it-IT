---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685242"
---
# <span data-ttu-id="f9819-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9819-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="f9819-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9819-102">SYNOPSIS</span></span>
<span data-ttu-id="f9819-103">Restituisce l'account di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="f9819-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="f9819-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9819-104">SYNTAX</span></span>

### <span data-ttu-id="f9819-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9819-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f9819-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f9819-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f9819-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9819-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="f9819-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9819-108">DESCRIPTION</span></span>
<span data-ttu-id="f9819-109">Restituisce l'account di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="f9819-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="f9819-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9819-110">EXAMPLES</span></span>

### <span data-ttu-id="f9819-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9819-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="f9819-112">Ottenere un elenco di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f9819-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="f9819-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f9819-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="f9819-114">Ottenere i dettagli dell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f9819-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="f9819-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9819-115">PARAMETERS</span></span>

### <span data-ttu-id="f9819-116">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f9819-116">-FarmName</span></span>
<span data-ttu-id="f9819-117">ID farm.</span><span class="sxs-lookup"><span data-stu-id="f9819-117">Farm Id.</span></span>

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

### <span data-ttu-id="f9819-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9819-118">-Name</span></span>
<span data-ttu-id="f9819-119">ID account di archiviazione interno, che non è visibile al tenant.</span><span class="sxs-lookup"><span data-stu-id="f9819-119">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="f9819-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9819-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9819-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9819-121">Resource group name.</span></span>

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

### <span data-ttu-id="f9819-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9819-122">-ResourceId</span></span>
<span data-ttu-id="f9819-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f9819-123">The resource id.</span></span>

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

### <span data-ttu-id="f9819-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="f9819-124">-Skip</span></span>
<span data-ttu-id="f9819-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f9819-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f9819-126">-Riepilogo</span><span class="sxs-lookup"><span data-stu-id="f9819-126">-Summary</span></span>
<span data-ttu-id="f9819-127">Viene restituita l'opzione per il riepilogo di wheter o per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="f9819-127">Switch for wheter summary or detailed information is returned.</span></span>

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

### <span data-ttu-id="f9819-128">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="f9819-128">-Top</span></span>
<span data-ttu-id="f9819-129">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f9819-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f9819-130">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="f9819-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f9819-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9819-131">CommonParameters</span></span>
<span data-ttu-id="f9819-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9819-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9819-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9819-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9819-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9819-134">INPUTS</span></span>

## <span data-ttu-id="f9819-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9819-135">OUTPUTS</span></span>

### <span data-ttu-id="f9819-136">Microsoft. AzureStack. Management. storage. admin. Models. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9819-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="f9819-137">Note</span><span class="sxs-lookup"><span data-stu-id="f9819-137">NOTES</span></span>

## <span data-ttu-id="f9819-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9819-138">RELATED LINKS</span></span>

