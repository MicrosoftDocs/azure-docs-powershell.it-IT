---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ebe9c71560f18ba9e4d7fb52514a4f5b7007bfb
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93867232"
---
# <span data-ttu-id="5ed9d-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="5ed9d-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="5ed9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ed9d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed9d-103">Scarica un prodotto da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="5ed9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ed9d-104">SYNTAX</span></span>

### <span data-ttu-id="5ed9d-105">Products_Download (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ed9d-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ed9d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ed9d-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ed9d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ed9d-107">DESCRIPTION</span></span>
<span data-ttu-id="5ed9d-108">Scarica un prodotto da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="5ed9d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ed9d-109">EXAMPLES</span></span>

### <span data-ttu-id="5ed9d-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5ed9d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="5ed9d-111">Scaricare un prodotto da Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="5ed9d-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="5ed9d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ed9d-112">PARAMETERS</span></span>

### <span data-ttu-id="5ed9d-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="5ed9d-113">-ActivationName</span></span>
<span data-ttu-id="5ed9d-114">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-114">Name of the activation.</span></span>

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

### <span data-ttu-id="5ed9d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ed9d-115">-AsJob</span></span>
<span data-ttu-id="5ed9d-116">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5ed9d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ed9d-117">-Force</span></span>
<span data-ttu-id="5ed9d-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5ed9d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ed9d-119">-Name</span></span>
<span data-ttu-id="5ed9d-120">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-120">Name of the product.</span></span>

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

### <span data-ttu-id="5ed9d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed9d-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ed9d-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="5ed9d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ed9d-123">-ResourceId</span></span>
<span data-ttu-id="5ed9d-124">Identificatore delle risorse per il prodotto di Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="5ed9d-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ed9d-125">-Confirm</span></span>
<span data-ttu-id="5ed9d-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed9d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed9d-127">-WhatIf</span></span>
<span data-ttu-id="5ed9d-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ed9d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed9d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed9d-130">CommonParameters</span></span>
<span data-ttu-id="5ed9d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed9d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed9d-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed9d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed9d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ed9d-133">INPUTS</span></span>

## <span data-ttu-id="5ed9d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ed9d-134">OUTPUTS</span></span>

## <span data-ttu-id="5ed9d-135">Note</span><span class="sxs-lookup"><span data-stu-id="5ed9d-135">NOTES</span></span>

## <span data-ttu-id="5ed9d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ed9d-136">RELATED LINKS</span></span>

