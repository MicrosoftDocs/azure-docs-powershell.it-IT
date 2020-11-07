---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93867224"
---
# <span data-ttu-id="df99e-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="df99e-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="df99e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df99e-102">SYNOPSIS</span></span>
<span data-ttu-id="df99e-103">Restituisce un elenco di prodotti disponibili per il download da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="df99e-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="df99e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df99e-104">SYNTAX</span></span>

### <span data-ttu-id="df99e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df99e-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="df99e-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="df99e-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="df99e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="df99e-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="df99e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df99e-108">DESCRIPTION</span></span>
<span data-ttu-id="df99e-109">Restituisce un elenco di prodotti disponibili per il download da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="df99e-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="df99e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df99e-110">EXAMPLES</span></span>

### <span data-ttu-id="df99e-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="df99e-111">EXAMPLE 1</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="df99e-112">Ottenere un elenco dei prodotti disponibili per il download da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="df99e-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="df99e-113">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="df99e-113">EXAMPLE 2</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="df99e-114">Ottenere le informazioni sul prodotto disponibili per il download da Azure Marketplace per nome.</span><span class="sxs-lookup"><span data-stu-id="df99e-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="df99e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df99e-115">PARAMETERS</span></span>

### <span data-ttu-id="df99e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="df99e-116">-Name</span></span>
<span data-ttu-id="df99e-117">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="df99e-117">Name of the product.</span></span>

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

### <span data-ttu-id="df99e-118">-Activationname</span><span class="sxs-lookup"><span data-stu-id="df99e-118">-ActivationName</span></span>
<span data-ttu-id="df99e-119">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="df99e-119">Name of the activation.</span></span>

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

### <span data-ttu-id="df99e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df99e-120">-ResourceGroupName</span></span>
<span data-ttu-id="df99e-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="df99e-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="df99e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df99e-122">-ResourceId</span></span>
<span data-ttu-id="df99e-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="df99e-123">The resource id.</span></span>

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

### <span data-ttu-id="df99e-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="df99e-124">-Skip</span></span>
<span data-ttu-id="df99e-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="df99e-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="df99e-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="df99e-126">-Top</span></span>
<span data-ttu-id="df99e-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="df99e-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="df99e-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="df99e-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="df99e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df99e-129">CommonParameters</span></span>
<span data-ttu-id="df99e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df99e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df99e-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df99e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df99e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df99e-132">INPUTS</span></span>

## <span data-ttu-id="df99e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df99e-133">OUTPUTS</span></span>

### <span data-ttu-id="df99e-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="df99e-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="df99e-135">Note</span><span class="sxs-lookup"><span data-stu-id="df99e-135">NOTES</span></span>

## <span data-ttu-id="df99e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df99e-136">RELATED LINKS</span></span>
