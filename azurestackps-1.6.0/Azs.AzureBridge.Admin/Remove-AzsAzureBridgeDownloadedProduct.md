---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bde5ca1c9a354e78f04ec3c9a54da72617f7ecc5
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2020
ms.locfileid: "93688701"
---
# <span data-ttu-id="68b31-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="68b31-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="68b31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68b31-102">SYNOPSIS</span></span>
<span data-ttu-id="68b31-103">Eliminare un prodotto scaricato da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="68b31-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="68b31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68b31-104">SYNTAX</span></span>

### <span data-ttu-id="68b31-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68b31-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b31-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b31-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68b31-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68b31-107">DESCRIPTION</span></span>
<span data-ttu-id="68b31-108">Eliminare un prodotto scaricato da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="68b31-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="68b31-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68b31-109">EXAMPLES</span></span>

### <span data-ttu-id="68b31-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="68b31-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="68b31-111">Eliminare un prodotto scaricato da Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="68b31-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="68b31-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68b31-112">PARAMETERS</span></span>

### <span data-ttu-id="68b31-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="68b31-113">-ActivationName</span></span>
<span data-ttu-id="68b31-114">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="68b31-114">Name of the activation.</span></span>

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

### <span data-ttu-id="68b31-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68b31-115">-AsJob</span></span>
<span data-ttu-id="68b31-116">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="68b31-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="68b31-117">-Force</span><span class="sxs-lookup"><span data-stu-id="68b31-117">-Force</span></span>
<span data-ttu-id="68b31-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="68b31-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="68b31-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="68b31-119">-Name</span></span>
<span data-ttu-id="68b31-120">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="68b31-120">Name of the product.</span></span>

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

### <span data-ttu-id="68b31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b31-121">-ResourceGroupName</span></span>
<span data-ttu-id="68b31-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="68b31-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="68b31-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b31-123">-ResourceId</span></span>
<span data-ttu-id="68b31-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="68b31-124">The resource id.</span></span>

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

### <span data-ttu-id="68b31-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68b31-125">-Confirm</span></span>
<span data-ttu-id="68b31-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68b31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b31-127">-WhatIf</span></span>
<span data-ttu-id="68b31-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68b31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b31-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68b31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b31-130">CommonParameters</span></span>
<span data-ttu-id="68b31-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b31-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b31-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b31-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68b31-133">INPUTS</span></span>

## <span data-ttu-id="68b31-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68b31-134">OUTPUTS</span></span>

### <span data-ttu-id="68b31-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="68b31-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="68b31-136">Note</span><span class="sxs-lookup"><span data-stu-id="68b31-136">NOTES</span></span>

## <span data-ttu-id="68b31-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68b31-137">RELATED LINKS</span></span>

