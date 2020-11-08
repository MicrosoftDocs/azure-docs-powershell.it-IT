---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030397"
---
# <span data-ttu-id="9da34-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="9da34-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="9da34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9da34-102">SYNOPSIS</span></span>
<span data-ttu-id="9da34-103">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9da34-103">Get the list of update locations.</span></span>

## <span data-ttu-id="9da34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9da34-104">SYNTAX</span></span>

### <span data-ttu-id="9da34-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9da34-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9da34-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9da34-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9da34-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9da34-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9da34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9da34-108">DESCRIPTION</span></span>
<span data-ttu-id="9da34-109">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9da34-109">Get the list of update locations.</span></span> <span data-ttu-id="9da34-110">I percorsi restituiti possono essere usati per ottenere gli aggiornamenti disponibili in una determinata posizione usando Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="9da34-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="9da34-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9da34-111">EXAMPLES</span></span>

### <span data-ttu-id="9da34-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="9da34-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="9da34-113">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9da34-113">Get the list of update locations.</span></span>

## <span data-ttu-id="9da34-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9da34-114">PARAMETERS</span></span>

### <span data-ttu-id="9da34-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9da34-115">-Location</span></span>
<span data-ttu-id="9da34-116">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="9da34-116">Name of the Location.</span></span>

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

### <span data-ttu-id="9da34-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da34-117">-ResourceGroupName</span></span>
<span data-ttu-id="9da34-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9da34-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9da34-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9da34-119">-ResourceId</span></span>
<span data-ttu-id="9da34-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9da34-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da34-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da34-121">CommonParameters</span></span>
<span data-ttu-id="9da34-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da34-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da34-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9da34-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da34-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9da34-124">INPUTS</span></span>

## <span data-ttu-id="9da34-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9da34-125">OUTPUTS</span></span>

### <span data-ttu-id="9da34-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="9da34-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="9da34-127">Note</span><span class="sxs-lookup"><span data-stu-id="9da34-127">NOTES</span></span>

## <span data-ttu-id="9da34-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9da34-128">RELATED LINKS</span></span>
