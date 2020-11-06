---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc16e5ecb0a70c20f9cd8b77b16208a09ac0a023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491633"
---
# <span data-ttu-id="61b67-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="61b67-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="61b67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61b67-102">SYNOPSIS</span></span>
<span data-ttu-id="61b67-103">Ottenere l'elenco degli aggiornamenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="61b67-103">Get the list of available updates.</span></span>

## <span data-ttu-id="61b67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61b67-104">SYNTAX</span></span>

### <span data-ttu-id="61b67-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61b67-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="61b67-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="61b67-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="61b67-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="61b67-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="61b67-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61b67-108">DESCRIPTION</span></span>
<span data-ttu-id="61b67-109">Ottenere l'elenco degli aggiornamenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="61b67-109">Get the list of available updates.</span></span> <span data-ttu-id="61b67-110">Gli aggiornamenti restituiti da questo modulo possono essere inviati tramite pipe a' install-AzsUpdate ', se applicabile.</span><span class="sxs-lookup"><span data-stu-id="61b67-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="61b67-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61b67-111">EXAMPLES</span></span>

### <span data-ttu-id="61b67-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="61b67-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="61b67-113">Ottenere l'elenco degli aggiornamenti disponibili.</span><span class="sxs-lookup"><span data-stu-id="61b67-113">Get the list of available updates.</span></span>

### <span data-ttu-id="61b67-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="61b67-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="61b67-115">Ottenere l'aggiornamento specifico.</span><span class="sxs-lookup"><span data-stu-id="61b67-115">Get the specific update.</span></span>

## <span data-ttu-id="61b67-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61b67-116">PARAMETERS</span></span>

### <span data-ttu-id="61b67-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="61b67-117">-Location</span></span>
<span data-ttu-id="61b67-118">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="61b67-118">The name of the update location.</span></span>

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

### <span data-ttu-id="61b67-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="61b67-119">-Name</span></span>
<span data-ttu-id="61b67-120">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="61b67-120">Name of the update.</span></span>

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

### <span data-ttu-id="61b67-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61b67-121">-ResourceGroupName</span></span>
<span data-ttu-id="61b67-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="61b67-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="61b67-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61b67-123">-ResourceId</span></span>
<span data-ttu-id="61b67-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="61b67-124">The resource id.</span></span>

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

### <span data-ttu-id="61b67-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="61b67-125">-Skip</span></span>
<span data-ttu-id="61b67-126">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="61b67-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="61b67-127">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="61b67-127">-Top</span></span>
<span data-ttu-id="61b67-128">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="61b67-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="61b67-129">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="61b67-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="61b67-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b67-130">CommonParameters</span></span>
<span data-ttu-id="61b67-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b67-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b67-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b67-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b67-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61b67-133">INPUTS</span></span>

## <span data-ttu-id="61b67-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61b67-134">OUTPUTS</span></span>

### <span data-ttu-id="61b67-135">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="61b67-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="61b67-136">Note</span><span class="sxs-lookup"><span data-stu-id="61b67-136">NOTES</span></span>

## <span data-ttu-id="61b67-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61b67-137">RELATED LINKS</span></span>
