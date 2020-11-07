---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673589"
---
# <span data-ttu-id="28983-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="28983-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="28983-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28983-102">SYNOPSIS</span></span>
<span data-ttu-id="28983-103">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="28983-103">Get the list of update locations.</span></span>

## <span data-ttu-id="28983-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28983-104">SYNTAX</span></span>

### <span data-ttu-id="28983-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28983-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="28983-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="28983-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="28983-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="28983-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="28983-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28983-108">DESCRIPTION</span></span>
<span data-ttu-id="28983-109">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="28983-109">Get the list of update locations.</span></span> <span data-ttu-id="28983-110">I percorsi restituiti possono essere usati per ottenere gli aggiornamenti disponibili in una determinata posizione usando Get-AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="28983-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="28983-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28983-111">EXAMPLES</span></span>

### <span data-ttu-id="28983-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="28983-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="28983-113">Ottenere l'elenco delle posizioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="28983-113">Get the list of update locations.</span></span>

## <span data-ttu-id="28983-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28983-114">PARAMETERS</span></span>

### <span data-ttu-id="28983-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="28983-115">-Name</span></span>
<span data-ttu-id="28983-116">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="28983-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28983-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28983-117">-ResourceGroupName</span></span>
<span data-ttu-id="28983-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="28983-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="28983-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28983-119">-ResourceId</span></span>
<span data-ttu-id="28983-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="28983-120">The resource id.</span></span>

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

### <span data-ttu-id="28983-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28983-121">CommonParameters</span></span>
<span data-ttu-id="28983-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28983-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28983-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28983-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28983-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28983-124">INPUTS</span></span>

## <span data-ttu-id="28983-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28983-125">OUTPUTS</span></span>

### <span data-ttu-id="28983-126">Microsoft. AzureStack. Management. Update. admin. Models. UpdateLocation</span><span class="sxs-lookup"><span data-stu-id="28983-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="28983-127">Note</span><span class="sxs-lookup"><span data-stu-id="28983-127">NOTES</span></span>

## <span data-ttu-id="28983-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28983-128">RELATED LINKS</span></span>

