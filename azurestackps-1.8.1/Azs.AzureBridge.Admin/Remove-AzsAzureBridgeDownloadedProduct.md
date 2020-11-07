---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1cc5311b1c26d4ae0cb9c1a7ce6ad58a818b53c6
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93867216"
---
# <span data-ttu-id="89d09-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="89d09-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="89d09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89d09-102">SYNOPSIS</span></span>
<span data-ttu-id="89d09-103">Eliminare un prodotto scaricato da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="89d09-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="89d09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89d09-104">SYNTAX</span></span>

### <span data-ttu-id="89d09-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89d09-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89d09-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89d09-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89d09-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89d09-107">DESCRIPTION</span></span>
<span data-ttu-id="89d09-108">Eliminare un prodotto scaricato da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="89d09-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="89d09-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89d09-109">EXAMPLES</span></span>

### <span data-ttu-id="89d09-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="89d09-110">EXAMPLE 1</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="89d09-111">Eliminare un prodotto scaricato da Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="89d09-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="89d09-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89d09-112">PARAMETERS</span></span>

### <span data-ttu-id="89d09-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="89d09-113">-Name</span></span>
<span data-ttu-id="89d09-114">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="89d09-114">Name of the product.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d09-115">-Activationname</span><span class="sxs-lookup"><span data-stu-id="89d09-115">-ActivationName</span></span>
<span data-ttu-id="89d09-116">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="89d09-116">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d09-117">-ResourceGroupName</span></span>
<span data-ttu-id="89d09-118">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="89d09-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d09-119">-Force</span><span class="sxs-lookup"><span data-stu-id="89d09-119">-Force</span></span>
<span data-ttu-id="89d09-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="89d09-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="89d09-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89d09-121">-ResourceId</span></span>
<span data-ttu-id="89d09-122">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="89d09-122">The resource id.</span></span>

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

### <span data-ttu-id="89d09-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89d09-123">-AsJob</span></span>
<span data-ttu-id="89d09-124">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="89d09-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="89d09-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d09-125">-WhatIf</span></span>
<span data-ttu-id="89d09-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89d09-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d09-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89d09-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d09-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89d09-128">-Confirm</span></span>
<span data-ttu-id="89d09-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89d09-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d09-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d09-130">CommonParameters</span></span>
<span data-ttu-id="89d09-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d09-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d09-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89d09-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d09-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89d09-133">INPUTS</span></span>

## <span data-ttu-id="89d09-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89d09-134">OUTPUTS</span></span>

### <span data-ttu-id="89d09-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="89d09-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="89d09-136">Note</span><span class="sxs-lookup"><span data-stu-id="89d09-136">NOTES</span></span>

## <span data-ttu-id="89d09-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89d09-137">RELATED LINKS</span></span>
