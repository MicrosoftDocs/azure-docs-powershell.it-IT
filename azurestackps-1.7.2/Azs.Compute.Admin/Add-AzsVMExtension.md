---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42181271e9295212f256cfc519e8ecc32eeae048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857565"
---
# <span data-ttu-id="e403e-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="e403e-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="e403e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e403e-102">SYNOPSIS</span></span>
<span data-ttu-id="e403e-103">Creare una nuova immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e403e-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="e403e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e403e-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e403e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e403e-105">DESCRIPTION</span></span>
<span data-ttu-id="e403e-106">Creare un'immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e403e-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="e403e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e403e-107">EXAMPLES</span></span>

### <span data-ttu-id="e403e-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e403e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="e403e-109">Aggiungere una nuova estensione di immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e403e-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="e403e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e403e-110">PARAMETERS</span></span>

### <span data-ttu-id="e403e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e403e-111">-AsJob</span></span>
<span data-ttu-id="e403e-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="e403e-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e403e-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="e403e-113">-ComputeRole</span></span>
<span data-ttu-id="e403e-114">Il tipo di ruolo, IaaS o PaaS, supporta questa estensione.</span><span class="sxs-lookup"><span data-stu-id="e403e-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e403e-115">-Force</span></span>
<span data-ttu-id="e403e-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e403e-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e403e-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="e403e-117">-IsSystemExtension</span></span>
<span data-ttu-id="e403e-118">Indica se l'estensione è per il sistema.</span><span class="sxs-lookup"><span data-stu-id="e403e-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="e403e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e403e-119">-Location</span></span>
<span data-ttu-id="e403e-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e403e-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403e-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e403e-121">-Publisher</span></span>
<span data-ttu-id="e403e-122">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="e403e-122">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403e-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="e403e-123">-SourceBlob</span></span>
<span data-ttu-id="e403e-124">URI nel pacchetto di estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e403e-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403e-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="e403e-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="e403e-126">True se supporta più estensioni.</span><span class="sxs-lookup"><span data-stu-id="e403e-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="e403e-127">-Digitare</span><span class="sxs-lookup"><span data-stu-id="e403e-127">-Type</span></span>
<span data-ttu-id="e403e-128">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="e403e-128">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403e-129">-Versione</span><span class="sxs-lookup"><span data-stu-id="e403e-129">-Version</span></span>
<span data-ttu-id="e403e-130">La versione dell'estensione dell'immagine del computer Vritual.</span><span class="sxs-lookup"><span data-stu-id="e403e-130">The version of the vritual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403e-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="e403e-131">-VmOsType</span></span>
<span data-ttu-id="e403e-132">Tipo di sistema operativo della macchina virtuale di destinazione necessario per la distribuzione del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="e403e-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403e-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="e403e-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="e403e-134">Valore che indica se l'estensione è abilitata per il supporto del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e403e-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="e403e-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e403e-135">-Confirm</span></span>
<span data-ttu-id="e403e-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e403e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e403e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e403e-137">-WhatIf</span></span>
<span data-ttu-id="e403e-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e403e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e403e-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e403e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e403e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e403e-140">CommonParameters</span></span>
<span data-ttu-id="e403e-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e403e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e403e-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e403e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e403e-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e403e-143">INPUTS</span></span>

## <span data-ttu-id="e403e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e403e-144">OUTPUTS</span></span>

### <span data-ttu-id="e403e-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="e403e-145">VmExtensionObject</span></span>

## <span data-ttu-id="e403e-146">Note</span><span class="sxs-lookup"><span data-stu-id="e403e-146">NOTES</span></span>

## <span data-ttu-id="e403e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e403e-147">RELATED LINKS</span></span>

