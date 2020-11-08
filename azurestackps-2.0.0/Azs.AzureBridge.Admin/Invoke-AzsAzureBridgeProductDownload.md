---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c7ca58f806f4d63f2938e3934838a40cbbb113b2
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/26/2020
ms.locfileid: "94030803"
---
# <span data-ttu-id="892de-101">Invoke-AzsAzureBridgeProductDownload</span><span class="sxs-lookup"><span data-stu-id="892de-101">Invoke-AzsAzureBridgeProductDownload</span></span>

## <span data-ttu-id="892de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="892de-102">SYNOPSIS</span></span>
<span data-ttu-id="892de-103">Scarica un prodotto da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="892de-103">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="892de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="892de-104">SYNTAX</span></span>

### <span data-ttu-id="892de-105">Products_Download (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="892de-105">Products_Download (Default)</span></span>
```
Invoke-AzsAzureBridgeProductDownload -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="892de-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="892de-106">ResourceId</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="892de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="892de-107">DESCRIPTION</span></span>
<span data-ttu-id="892de-108">Scarica un prodotto da Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="892de-108">Downloads a product from azure marketplace.</span></span>

## <span data-ttu-id="892de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="892de-109">EXAMPLES</span></span>

### <span data-ttu-id="892de-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="892de-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Invoke-AzsAzureBridgeProductDownload -ActivationName 'myActivation' -Name 'microsoft.docker-arm.1.1.0' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="892de-111">Scaricare un prodotto da Azure Marketplace</span><span class="sxs-lookup"><span data-stu-id="892de-111">Download a product from Azure Marketplace</span></span>

## <span data-ttu-id="892de-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="892de-112">PARAMETERS</span></span>

### <span data-ttu-id="892de-113">-Activationname</span><span class="sxs-lookup"><span data-stu-id="892de-113">-ActivationName</span></span>
<span data-ttu-id="892de-114">Nome dell'attivazione.</span><span class="sxs-lookup"><span data-stu-id="892de-114">Name of the activation.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892de-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="892de-115">-AsJob</span></span>
<span data-ttu-id="892de-116">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="892de-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="892de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="892de-117">-Force</span></span>
<span data-ttu-id="892de-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="892de-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="892de-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="892de-119">-Name</span></span>
<span data-ttu-id="892de-120">Nome del prodotto.</span><span class="sxs-lookup"><span data-stu-id="892de-120">Name of the product.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892de-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892de-121">-ResourceGroupName</span></span>
<span data-ttu-id="892de-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="892de-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Products_Download
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892de-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="892de-123">-ResourceId</span></span>
<span data-ttu-id="892de-124">Identificatore delle risorse per il prodotto di Azure Bridge.</span><span class="sxs-lookup"><span data-stu-id="892de-124">Resource identifier for azure bridge product.</span></span>

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

### <span data-ttu-id="892de-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="892de-125">-Confirm</span></span>
<span data-ttu-id="892de-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="892de-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="892de-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="892de-127">-WhatIf</span></span>
<span data-ttu-id="892de-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="892de-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="892de-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="892de-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="892de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892de-130">CommonParameters</span></span>
<span data-ttu-id="892de-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892de-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892de-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892de-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="892de-133">INPUTS</span></span>

## <span data-ttu-id="892de-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="892de-134">OUTPUTS</span></span>

## <span data-ttu-id="892de-135">Note</span><span class="sxs-lookup"><span data-stu-id="892de-135">NOTES</span></span>

## <span data-ttu-id="892de-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="892de-136">RELATED LINKS</span></span>

