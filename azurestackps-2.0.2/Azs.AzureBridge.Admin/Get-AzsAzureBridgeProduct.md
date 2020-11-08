---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edcc9bea35e1675b42a04c2b4e804c48ba052742
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/26/2020
ms.locfileid: "94030783"
---
# <span data-ttu-id="516e8-101">Get-AzsAzureBridgeProduct</span><span class="sxs-lookup"><span data-stu-id="516e8-101">Get-AzsAzureBridgeProduct</span></span>

## <span data-ttu-id="516e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="516e8-102">SYNOPSIS</span></span>
<span data-ttu-id="516e8-103">Restituisce un elenco di prodotti disponibili per il download da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="516e8-103">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="516e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="516e8-104">SYNTAX</span></span>

### <span data-ttu-id="516e8-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="516e8-105">List (Default)</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="516e8-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="516e8-106">Get</span></span>
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### <span data-ttu-id="516e8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="516e8-107">ResourceId</span></span>
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="516e8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="516e8-108">DESCRIPTION</span></span>
<span data-ttu-id="516e8-109">Restituisce un elenco di prodotti disponibili per il download da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="516e8-109">Returns a list of products available for download from Azure Marketplace.</span></span>

## <span data-ttu-id="516e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="516e8-110">EXAMPLES</span></span>

### <span data-ttu-id="516e8-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="516e8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="516e8-112">Ottenere un elenco dei prodotti disponibili per il download da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="516e8-112">Get a list of Products available for download from Azure Marketplace.</span></span>

### <span data-ttu-id="516e8-113">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="516e8-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

<span data-ttu-id="516e8-114">Ottenere le informazioni sul prodotto disponibili per il download da Azure Marketplace per nome.</span><span class="sxs-lookup"><span data-stu-id="516e8-114">Get a product info available for download from Azure Marketplace by Name.</span></span>

## <span data-ttu-id="516e8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="516e8-115">PARAMETERS</span></span>

### <span data-ttu-id="516e8-116">-Activationname</span><span class="sxs-lookup"><span data-stu-id="516e8-116">-ActivationName</span></span>
<span data-ttu-id="516e8-117">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="516e8-117">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="516e8-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="516e8-118">-Name</span></span>
<span data-ttu-id="516e8-119">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="516e8-119">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="516e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="516e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="516e8-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="516e8-121">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="516e8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="516e8-122">-ResourceId</span></span>
<span data-ttu-id="516e8-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="516e8-123">The resource id.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="516e8-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="516e8-124">-Skip</span></span>
<span data-ttu-id="516e8-125">Ignorare i primi elementi N specificati dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="516e8-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="516e8-126">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="516e8-126">-Top</span></span>
<span data-ttu-id="516e8-127">Restituisce i primi N elementi come specificato dal valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="516e8-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="516e8-128">Si applica dopo il parametro-Skip.</span><span class="sxs-lookup"><span data-stu-id="516e8-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="516e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516e8-129">CommonParameters</span></span>
<span data-ttu-id="516e8-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516e8-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="516e8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516e8-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="516e8-132">INPUTS</span></span>

## <span data-ttu-id="516e8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="516e8-133">OUTPUTS</span></span>

### <span data-ttu-id="516e8-134">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ProductResource</span><span class="sxs-lookup"><span data-stu-id="516e8-134">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ProductResource</span></span>

## <span data-ttu-id="516e8-135">Note</span><span class="sxs-lookup"><span data-stu-id="516e8-135">NOTES</span></span>

## <span data-ttu-id="516e8-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="516e8-136">RELATED LINKS</span></span>

