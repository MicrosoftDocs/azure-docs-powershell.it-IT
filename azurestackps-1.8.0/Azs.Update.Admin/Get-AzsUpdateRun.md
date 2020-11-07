---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858830"
---
# <span data-ttu-id="ad7ac-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="ad7ac-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="ad7ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7ac-103">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-103">Get the list of update runs.</span></span>

## <span data-ttu-id="ad7ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad7ac-104">SYNTAX</span></span>

### <span data-ttu-id="ad7ac-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad7ac-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ad7ac-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ad7ac-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad7ac-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad7ac-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad7ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad7ac-108">DESCRIPTION</span></span>
<span data-ttu-id="ad7ac-109">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-109">Get the list of update runs.</span></span> <span data-ttu-id="ad7ac-110">Le istanze degli oggetti UpdateRun restituiti possono essere inviate tramite pipe a restart-AzsUpdateRun, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="ad7ac-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad7ac-111">EXAMPLES</span></span>

### <span data-ttu-id="ad7ac-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="ad7ac-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="ad7ac-113">Ottenere un elenco di tutti i tentativi di applicazione di un aggiornamento specifico.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="ad7ac-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad7ac-114">PARAMETERS</span></span>

### <span data-ttu-id="ad7ac-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad7ac-115">-Name</span></span>
<span data-ttu-id="ad7ac-116">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-116">Update run identifier.</span></span>

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

### <span data-ttu-id="ad7ac-117">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="ad7ac-117">-UpdateName</span></span>
<span data-ttu-id="ad7ac-118">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-118">Name of the update.</span></span>

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

### <span data-ttu-id="ad7ac-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ad7ac-119">-Location</span></span>
<span data-ttu-id="ad7ac-120">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-120">The name of the update location.</span></span>

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

### <span data-ttu-id="ad7ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="ad7ac-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ad7ac-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad7ac-123">-ResourceId</span></span>
<span data-ttu-id="ad7ac-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-124">The resource id.</span></span>

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

### <span data-ttu-id="ad7ac-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="ad7ac-125">-Skip</span></span>
<span data-ttu-id="ad7ac-126">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ad7ac-127">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="ad7ac-127">-Top</span></span>
<span data-ttu-id="ad7ac-128">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ad7ac-129">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ad7ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7ac-130">CommonParameters</span></span>
<span data-ttu-id="ad7ac-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad7ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7ac-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad7ac-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7ac-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad7ac-133">INPUTS</span></span>

## <span data-ttu-id="ad7ac-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad7ac-134">OUTPUTS</span></span>

### <span data-ttu-id="ad7ac-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="ad7ac-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="ad7ac-136">Note</span><span class="sxs-lookup"><span data-stu-id="ad7ac-136">NOTES</span></span>

## <span data-ttu-id="ad7ac-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad7ac-137">RELATED LINKS</span></span>
