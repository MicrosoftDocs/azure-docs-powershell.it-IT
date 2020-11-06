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
ms.locfileid: "93491550"
---
# <span data-ttu-id="61442-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="61442-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="61442-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61442-102">SYNOPSIS</span></span>
<span data-ttu-id="61442-103">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="61442-103">Get the list of update runs.</span></span>

## <span data-ttu-id="61442-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61442-104">SYNTAX</span></span>

### <span data-ttu-id="61442-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="61442-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="61442-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="61442-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="61442-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="61442-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="61442-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61442-108">DESCRIPTION</span></span>
<span data-ttu-id="61442-109">Ottenere l'elenco delle esecuzioni degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="61442-109">Get the list of update runs.</span></span> <span data-ttu-id="61442-110">Le istanze degli oggetti UpdateRun restituiti possono essere inviate tramite pipe a restart-AzsUpdateRun, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="61442-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="61442-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61442-111">EXAMPLES</span></span>

### <span data-ttu-id="61442-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="61442-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="61442-113">Ottenere un elenco di tutti i tentativi di applicazione di un aggiornamento specifico.</span><span class="sxs-lookup"><span data-stu-id="61442-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="61442-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61442-114">PARAMETERS</span></span>

### <span data-ttu-id="61442-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="61442-115">-Location</span></span>
<span data-ttu-id="61442-116">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="61442-116">The name of the update location.</span></span>

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

### <span data-ttu-id="61442-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="61442-117">-Name</span></span>
<span data-ttu-id="61442-118">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="61442-118">Update run identifier.</span></span>

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

### <span data-ttu-id="61442-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61442-119">-ResourceGroupName</span></span>
<span data-ttu-id="61442-120">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="61442-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="61442-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61442-121">-ResourceId</span></span>
<span data-ttu-id="61442-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="61442-122">The resource id.</span></span>

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

### <span data-ttu-id="61442-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="61442-123">-Skip</span></span>
<span data-ttu-id="61442-124">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="61442-124">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="61442-125">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="61442-125">-Top</span></span>
<span data-ttu-id="61442-126">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="61442-126">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="61442-127">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="61442-127">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="61442-128">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="61442-128">-UpdateName</span></span>
<span data-ttu-id="61442-129">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="61442-129">Name of the update.</span></span>

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

### <span data-ttu-id="61442-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61442-130">CommonParameters</span></span>
<span data-ttu-id="61442-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61442-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61442-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61442-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61442-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61442-133">INPUTS</span></span>

## <span data-ttu-id="61442-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61442-134">OUTPUTS</span></span>

### <span data-ttu-id="61442-135">Microsoft. AzureStack. Management. Update. admin. Models. UpdateRun</span><span class="sxs-lookup"><span data-stu-id="61442-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="61442-136">Note</span><span class="sxs-lookup"><span data-stu-id="61442-136">NOTES</span></span>

## <span data-ttu-id="61442-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61442-137">RELATED LINKS</span></span>
