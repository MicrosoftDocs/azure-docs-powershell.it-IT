---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859982"
---
# <span data-ttu-id="8b9a2-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="8b9a2-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="8b9a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9a2-103">Ottenere l'elenco delle offerte come amministratore.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="8b9a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b9a2-104">SYNTAX</span></span>

### <span data-ttu-id="8b9a2-105">ListAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b9a2-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8b9a2-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8b9a2-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="8b9a2-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="8b9a2-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8b9a2-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b9a2-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8b9a2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b9a2-109">DESCRIPTION</span></span>
<span data-ttu-id="8b9a2-110">Ottenere l'elenco delle offerte.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-110">Get the list of offers.</span></span>

## <span data-ttu-id="8b9a2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b9a2-111">EXAMPLES</span></span>

### <span data-ttu-id="8b9a2-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b9a2-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="8b9a2-113">Ottenere l'elenco delle offerte come amministratore.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="8b9a2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b9a2-114">PARAMETERS</span></span>

### <span data-ttu-id="8b9a2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b9a2-115">-Name</span></span>
<span data-ttu-id="8b9a2-116">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-116">Name of an offer.</span></span>

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

### <span data-ttu-id="8b9a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b9a2-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b9a2-119">-ResourceId</span></span>
<span data-ttu-id="8b9a2-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-120">The resource id.</span></span>

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

### <span data-ttu-id="8b9a2-121">-Skip</span><span class="sxs-lookup"><span data-stu-id="8b9a2-121">-Skip</span></span>
<span data-ttu-id="8b9a2-122">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a2-123">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="8b9a2-123">-Top</span></span>
<span data-ttu-id="8b9a2-124">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8b9a2-125">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b9a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9a2-126">CommonParameters</span></span>
<span data-ttu-id="8b9a2-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b9a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9a2-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b9a2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9a2-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b9a2-129">INPUTS</span></span>

## <span data-ttu-id="8b9a2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b9a2-130">OUTPUTS</span></span>

### <span data-ttu-id="8b9a2-131">Microsoft. AzureStack. Management. subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="8b9a2-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="8b9a2-132">Note</span><span class="sxs-lookup"><span data-stu-id="8b9a2-132">NOTES</span></span>

## <span data-ttu-id="8b9a2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b9a2-133">RELATED LINKS</span></span>

