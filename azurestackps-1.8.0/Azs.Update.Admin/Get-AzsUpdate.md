---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858833"
---
# <span data-ttu-id="41149-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="41149-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="41149-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41149-102">SYNOPSIS</span></span>
<span data-ttu-id="41149-103">Ottenere l'elenco degli aggiornamenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="41149-103">Get the list of available updates.</span></span>

## <span data-ttu-id="41149-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41149-104">SYNTAX</span></span>

### <span data-ttu-id="41149-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41149-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="41149-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="41149-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="41149-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="41149-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="41149-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41149-108">DESCRIPTION</span></span>
<span data-ttu-id="41149-109">Ottenere l'elenco degli aggiornamenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="41149-109">Get the list of available updates.</span></span> <span data-ttu-id="41149-110">Gli aggiornamenti restituiti da questo modulo possono essere inviati tramite pipe a' install-AzsUpdate ', se applicabile.</span><span class="sxs-lookup"><span data-stu-id="41149-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="41149-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41149-111">EXAMPLES</span></span>

### <span data-ttu-id="41149-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="41149-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="41149-113">Ottenere l'elenco degli aggiornamenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="41149-113">Get the list of available updates.</span></span>

### <span data-ttu-id="41149-114">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="41149-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="41149-115">Ottenere l'aggiornamento specifico.</span><span class="sxs-lookup"><span data-stu-id="41149-115">Get the specific update.</span></span>

## <span data-ttu-id="41149-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41149-116">PARAMETERS</span></span>

### <span data-ttu-id="41149-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="41149-117">-Name</span></span>
<span data-ttu-id="41149-118">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="41149-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41149-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="41149-119">-Location</span></span>
<span data-ttu-id="41149-120">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="41149-120">The name of the update location.</span></span>

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

### <span data-ttu-id="41149-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41149-121">-ResourceGroupName</span></span>
<span data-ttu-id="41149-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="41149-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="41149-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41149-123">-ResourceId</span></span>
<span data-ttu-id="41149-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="41149-124">The resource id.</span></span>

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

### <span data-ttu-id="41149-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="41149-125">-Skip</span></span>
<span data-ttu-id="41149-126">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="41149-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="41149-127">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="41149-127">-Top</span></span>
<span data-ttu-id="41149-128">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="41149-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="41149-129">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="41149-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="41149-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41149-130">CommonParameters</span></span>
<span data-ttu-id="41149-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41149-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41149-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41149-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41149-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41149-133">INPUTS</span></span>

## <span data-ttu-id="41149-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41149-134">OUTPUTS</span></span>

### <span data-ttu-id="41149-135">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="41149-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="41149-136">Note</span><span class="sxs-lookup"><span data-stu-id="41149-136">NOTES</span></span>

## <span data-ttu-id="41149-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41149-137">RELATED LINKS</span></span>
