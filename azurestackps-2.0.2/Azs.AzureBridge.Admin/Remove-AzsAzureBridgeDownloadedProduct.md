---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d75764209b56ed0cc05d80e00581de3f982e435
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/26/2020
ms.locfileid: "94030792"
---
# <span data-ttu-id="7080c-101">Remove-AzsAzureBridgeDownloadedProduct</span><span class="sxs-lookup"><span data-stu-id="7080c-101">Remove-AzsAzureBridgeDownloadedProduct</span></span>

## <span data-ttu-id="7080c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7080c-102">SYNOPSIS</span></span>
<span data-ttu-id="7080c-103">Eliminare un prodotto scaricato da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="7080c-103">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="7080c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7080c-104">SYNTAX</span></span>

### <span data-ttu-id="7080c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7080c-105">Delete (Default)</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-Force] [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7080c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7080c-106">ResourceId</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct [-Force] -ResourceId <String> [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7080c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7080c-107">DESCRIPTION</span></span>
<span data-ttu-id="7080c-108">Eliminare un prodotto scaricato da Azure MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="7080c-108">Delete a product downloaded from Azure MarketPlace.</span></span>

## <span data-ttu-id="7080c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7080c-109">EXAMPLES</span></span>

### <span data-ttu-id="7080c-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7080c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsAzureBridgeDownloadedProduct -ActivationName 'myActivation' -ProductName 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="7080c-111">Eliminare un prodotto scaricato da Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="7080c-111">Delete a product downloaded from Azure Marketplace</span></span>

## <span data-ttu-id="7080c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7080c-112">PARAMETERS</span></span>

### <span data-ttu-id="7080c-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="7080c-113">-ActivationName</span></span>
<span data-ttu-id="7080c-114">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="7080c-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7080c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7080c-115">-AsJob</span></span>
<span data-ttu-id="7080c-116">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="7080c-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7080c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7080c-117">-Force</span></span>
<span data-ttu-id="7080c-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7080c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7080c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7080c-119">-Name</span></span>
<span data-ttu-id="7080c-120">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7080c-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7080c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7080c-121">-ResourceGroupName</span></span>
<span data-ttu-id="7080c-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7080c-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7080c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7080c-123">-ResourceId</span></span>
<span data-ttu-id="7080c-124">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="7080c-124">The resource id.</span></span>

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

### <span data-ttu-id="7080c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7080c-125">-Confirm</span></span>
<span data-ttu-id="7080c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7080c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7080c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7080c-127">-WhatIf</span></span>
<span data-ttu-id="7080c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7080c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7080c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7080c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7080c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7080c-130">CommonParameters</span></span>
<span data-ttu-id="7080c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7080c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7080c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7080c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7080c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7080c-133">INPUTS</span></span>

## <span data-ttu-id="7080c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7080c-134">OUTPUTS</span></span>

### <span data-ttu-id="7080c-135">Microsoft. AzureStack. Management. AzureBridge. admin. Models. DownloadedProductResource</span><span class="sxs-lookup"><span data-stu-id="7080c-135">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.DownloadedProductResource</span></span>

## <span data-ttu-id="7080c-136">Note</span><span class="sxs-lookup"><span data-stu-id="7080c-136">NOTES</span></span>

## <span data-ttu-id="7080c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7080c-137">RELATED LINKS</span></span>

