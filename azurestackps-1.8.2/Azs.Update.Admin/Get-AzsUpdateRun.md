---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030396"
---
# <span data-ttu-id="229c6-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="229c6-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="229c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="229c6-102">SYNOPSIS</span></span>
<span data-ttu-id="229c6-103">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="229c6-103">Get the list of update runs.</span></span>

## <span data-ttu-id="229c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="229c6-104">SYNTAX</span></span>

### <span data-ttu-id="229c6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="229c6-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="229c6-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="229c6-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="229c6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="229c6-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="229c6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="229c6-108">DESCRIPTION</span></span>
<span data-ttu-id="229c6-109">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="229c6-109">Get the list of update runs.</span></span> <span data-ttu-id="229c6-110">Le istanze degli oggetti UpdateRun restituiti possono essere inviate tramite pipe a restart-AzsUpdateRun, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="229c6-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="229c6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="229c6-111">EXAMPLES</span></span>

### <span data-ttu-id="229c6-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="229c6-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="229c6-113">Ottenere un elenco di tutti i tentativi di applicazione di un aggiornamento specifico.</span><span class="sxs-lookup"><span data-stu-id="229c6-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="229c6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="229c6-114">PARAMETERS</span></span>

### <span data-ttu-id="229c6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="229c6-115">-Name</span></span>
<span data-ttu-id="229c6-116">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="229c6-116">Update run identifier.</span></span>

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

### <span data-ttu-id="229c6-117">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="229c6-117">-UpdateName</span></span>
<span data-ttu-id="229c6-118">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="229c6-118">Name of the update.</span></span>

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

### <span data-ttu-id="229c6-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="229c6-119">-Location</span></span>
<span data-ttu-id="229c6-120">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="229c6-120">The name of the update location.</span></span>

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

### <span data-ttu-id="229c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="229c6-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="229c6-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="229c6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="229c6-123">-ResourceId</span></span>
<span data-ttu-id="229c6-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="229c6-124">The resource id.</span></span>

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

### <span data-ttu-id="229c6-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="229c6-125">-Skip</span></span>
<span data-ttu-id="229c6-126">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="229c6-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="229c6-127">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="229c6-127">-Top</span></span>
<span data-ttu-id="229c6-128">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="229c6-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="229c6-129">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="229c6-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="229c6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229c6-130">CommonParameters</span></span>
<span data-ttu-id="229c6-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229c6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229c6-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229c6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229c6-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="229c6-133">INPUTS</span></span>

## <span data-ttu-id="229c6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="229c6-134">OUTPUTS</span></span>

### <span data-ttu-id="229c6-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="229c6-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="229c6-136">Note</span><span class="sxs-lookup"><span data-stu-id="229c6-136">NOTES</span></span>

## <span data-ttu-id="229c6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="229c6-137">RELATED LINKS</span></span>
