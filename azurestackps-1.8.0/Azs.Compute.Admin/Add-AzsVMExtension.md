---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0390c3f55c444b4a0e37e25c93536b60d10bc7b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858874"
---
# <span data-ttu-id="8be73-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="8be73-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="8be73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8be73-102">SYNOPSIS</span></span>
<span data-ttu-id="8be73-103">Creare una nuova immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8be73-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="8be73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8be73-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8be73-105">DESCRIPTION</span></span>
<span data-ttu-id="8be73-106">Creare un'immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8be73-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="8be73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8be73-107">EXAMPLES</span></span>

### <span data-ttu-id="8be73-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8be73-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="8be73-109">Aggiungere una nuova estensione di immagine della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8be73-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="8be73-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8be73-110">PARAMETERS</span></span>

### <span data-ttu-id="8be73-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8be73-111">-AsJob</span></span>
<span data-ttu-id="8be73-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="8be73-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8be73-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="8be73-113">-ComputeRole</span></span>
<span data-ttu-id="8be73-114">Il tipo di ruolo, IaaS o PaaS, supporta questa estensione.</span><span class="sxs-lookup"><span data-stu-id="8be73-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="8be73-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8be73-115">-Force</span></span>
<span data-ttu-id="8be73-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8be73-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8be73-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="8be73-117">-IsSystemExtension</span></span>
<span data-ttu-id="8be73-118">Indica se l'estensione è per il sistema.</span><span class="sxs-lookup"><span data-stu-id="8be73-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="8be73-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8be73-119">-Location</span></span>
<span data-ttu-id="8be73-120">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8be73-120">Location of the resource.</span></span>

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

### <span data-ttu-id="8be73-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8be73-121">-Publisher</span></span>
<span data-ttu-id="8be73-122">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="8be73-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="8be73-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="8be73-123">-SourceBlob</span></span>
<span data-ttu-id="8be73-124">URI nel pacchetto di estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8be73-124">URI to virtual machine extension package.</span></span>

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

### <span data-ttu-id="8be73-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="8be73-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="8be73-126">True se supporta più estensioni.</span><span class="sxs-lookup"><span data-stu-id="8be73-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="8be73-127">-Digitare</span><span class="sxs-lookup"><span data-stu-id="8be73-127">-Type</span></span>
<span data-ttu-id="8be73-128">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="8be73-128">Type of extension.</span></span>

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

### <span data-ttu-id="8be73-129">-Versione</span><span class="sxs-lookup"><span data-stu-id="8be73-129">-Version</span></span>
<span data-ttu-id="8be73-130">La versione dell'estensione dell'immagine del computer Vritual.</span><span class="sxs-lookup"><span data-stu-id="8be73-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="8be73-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="8be73-131">-VmOsType</span></span>
<span data-ttu-id="8be73-132">Tipo di sistema operativo della macchina virtuale di destinazione necessario per la distribuzione del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="8be73-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="8be73-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="8be73-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="8be73-134">Valore che indica se l'estensione è abilitata per il supporto del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8be73-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="8be73-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8be73-135">-Confirm</span></span>
<span data-ttu-id="8be73-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8be73-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be73-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be73-137">-WhatIf</span></span>
<span data-ttu-id="8be73-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8be73-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be73-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8be73-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be73-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be73-140">CommonParameters</span></span>
<span data-ttu-id="8be73-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be73-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be73-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be73-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be73-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8be73-143">INPUTS</span></span>

## <span data-ttu-id="8be73-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8be73-144">OUTPUTS</span></span>

### <span data-ttu-id="8be73-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="8be73-145">VmExtensionObject</span></span>

## <span data-ttu-id="8be73-146">Note</span><span class="sxs-lookup"><span data-stu-id="8be73-146">NOTES</span></span>

## <span data-ttu-id="8be73-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8be73-147">RELATED LINKS</span></span>

