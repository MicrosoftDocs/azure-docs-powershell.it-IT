---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 107709fa7431e8c37f156f1304f560e42c08ed60
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93867250"
---
# <span data-ttu-id="bc301-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="bc301-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="bc301-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc301-102">SYNOPSIS</span></span>
<span data-ttu-id="bc301-103">Scarica un prodotto da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="bc301-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="bc301-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc301-104">SYNTAX</span></span>

### <span data-ttu-id="bc301-105">Products_Download (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc301-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc301-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc301-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc301-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc301-107">DESCRIPTION</span></span>
<span data-ttu-id="bc301-108">Scarica un prodotto da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="bc301-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="bc301-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc301-109">EXAMPLES</span></span>

### <span data-ttu-id="bc301-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="bc301-110">EXAMPLE 1</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="bc301-111">Scaricare un prodotto da Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="bc301-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="bc301-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc301-112">PARAMETERS</span></span>

### <span data-ttu-id="bc301-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc301-113">-Name</span></span>
<span data-ttu-id="bc301-114">Nome del prodotto</span><span class="sxs-lookup"><span data-stu-id="bc301-114">Name of the product</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc301-115">-Activationname</span><span class="sxs-lookup"><span data-stu-id="bc301-115">-ActivationName</span></span>
<span data-ttu-id="bc301-116">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="bc301-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc301-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc301-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc301-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="bc301-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Products_Download
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc301-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc301-119">-ResourceId</span></span>
<span data-ttu-id="bc301-120">Identificatore delle risorse per il prodotto di Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="bc301-120">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="bc301-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc301-121">-AsJob</span></span>
<span data-ttu-id="bc301-122">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="bc301-122">Run asynchronous as a job and return the job object.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc301-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bc301-123">-Force</span></span>
<span data-ttu-id="bc301-124">Parametro switch per non richiedere la conferma</span><span class="sxs-lookup"><span data-stu-id="bc301-124">Switch parameter not to ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc301-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc301-125">-WhatIf</span></span>
<span data-ttu-id="bc301-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc301-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc301-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc301-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc301-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc301-128">-Confirm</span></span>
<span data-ttu-id="bc301-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc301-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc301-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc301-130">CommonParameters</span></span>
<span data-ttu-id="bc301-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc301-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc301-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc301-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc301-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc301-133">INPUTS</span></span>

## <span data-ttu-id="bc301-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc301-134">OUTPUTS</span></span>

## <span data-ttu-id="bc301-135">Note</span><span class="sxs-lookup"><span data-stu-id="bc301-135">NOTES</span></span>

## <span data-ttu-id="bc301-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc301-136">RELATED LINKS</span></span>
