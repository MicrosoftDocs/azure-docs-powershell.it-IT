---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859758"
---
# <span data-ttu-id="3786d-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="3786d-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="3786d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3786d-102">SYNOPSIS</span></span>
<span data-ttu-id="3786d-103">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3786d-103">Get the list of update locations.</span></span>

## <span data-ttu-id="3786d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3786d-104">SYNTAX</span></span>

### <span data-ttu-id="3786d-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3786d-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3786d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="3786d-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3786d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3786d-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3786d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3786d-108">DESCRIPTION</span></span>
<span data-ttu-id="3786d-109">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3786d-109">Get the list of update locations.</span></span> <span data-ttu-id="3786d-110">I percorsi restituiti possono essere usati per ottenere gli aggiornamenti disponibili in una determinata posizione usando Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="3786d-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="3786d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3786d-111">EXAMPLES</span></span>

### <span data-ttu-id="3786d-112">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="3786d-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="3786d-113">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3786d-113">Get the list of update locations.</span></span>

## <span data-ttu-id="3786d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3786d-114">PARAMETERS</span></span>

### <span data-ttu-id="3786d-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3786d-115">-Location</span></span>
<span data-ttu-id="3786d-116">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="3786d-116">Name of the Location.</span></span>

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

### <span data-ttu-id="3786d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3786d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3786d-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3786d-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3786d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3786d-119">-ResourceId</span></span>
<span data-ttu-id="3786d-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3786d-120">The resource id.</span></span>

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

### <span data-ttu-id="3786d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3786d-121">CommonParameters</span></span>
<span data-ttu-id="3786d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3786d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3786d-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3786d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3786d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3786d-124">INPUTS</span></span>

## <span data-ttu-id="3786d-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3786d-125">OUTPUTS</span></span>

### <span data-ttu-id="3786d-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="3786d-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="3786d-127">Note</span><span class="sxs-lookup"><span data-stu-id="3786d-127">NOTES</span></span>

## <span data-ttu-id="3786d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3786d-128">RELATED LINKS</span></span>
