---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 268a306597fe3760e8abc7e31f980da078bf2bc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673587"
---
# <span data-ttu-id="d59d9-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="d59d9-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="d59d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d59d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d59d9-103">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="d59d9-103">Get the list of update runs.</span></span>

## <span data-ttu-id="d59d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d59d9-104">SYNTAX</span></span>

### <span data-ttu-id="d59d9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d59d9-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d59d9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d59d9-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d59d9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d59d9-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d59d9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d59d9-108">DESCRIPTION</span></span>
<span data-ttu-id="d59d9-109">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="d59d9-109">Get the list of update runs.</span></span> <span data-ttu-id="d59d9-110">Le istanze degli oggetti UpdateRun restituiti possono essere inviate tramite pipe a restart-AzsUpdateRun, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="d59d9-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="d59d9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d59d9-111">EXAMPLES</span></span>

### <span data-ttu-id="d59d9-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d59d9-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="d59d9-113">Ottenere un elenco di tutti i tentativi di applicazione di un aggiornamento specifico.</span><span class="sxs-lookup"><span data-stu-id="d59d9-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="d59d9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d59d9-114">PARAMETERS</span></span>

### <span data-ttu-id="d59d9-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d59d9-115">-Location</span></span>
<span data-ttu-id="d59d9-116">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d59d9-116">The name of the update location.</span></span>

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

### <span data-ttu-id="d59d9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d59d9-117">-Name</span></span>
<span data-ttu-id="d59d9-118">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d59d9-118">Update run identifier.</span></span>

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

### <span data-ttu-id="d59d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d59d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="d59d9-120">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d59d9-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d59d9-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d59d9-121">-ResourceId</span></span>
<span data-ttu-id="d59d9-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d59d9-122">The resource id.</span></span>

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

### <span data-ttu-id="d59d9-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="d59d9-123">-Skip</span></span>
<span data-ttu-id="d59d9-124">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d59d9-124">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d59d9-125">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="d59d9-125">-Top</span></span>
<span data-ttu-id="d59d9-126">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="d59d9-126">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d59d9-127">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="d59d9-127">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d59d9-128">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="d59d9-128">-UpdateName</span></span>
<span data-ttu-id="d59d9-129">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d59d9-129">Name of the update.</span></span>

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

### <span data-ttu-id="d59d9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59d9-130">CommonParameters</span></span>
<span data-ttu-id="d59d9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59d9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59d9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59d9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59d9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d59d9-133">INPUTS</span></span>

## <span data-ttu-id="d59d9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d59d9-134">OUTPUTS</span></span>

### <span data-ttu-id="d59d9-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="d59d9-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="d59d9-136">Note</span><span class="sxs-lookup"><span data-stu-id="d59d9-136">NOTES</span></span>

## <span data-ttu-id="d59d9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d59d9-137">RELATED LINKS</span></span>

