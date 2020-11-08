---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030870"
---
# <span data-ttu-id="8a9be-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="8a9be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a9be-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9be-103">Rimuove gli oggetti della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a9be-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="8a9be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a9be-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a9be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a9be-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9be-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="8a9be-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8a9be-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a9be-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8a9be-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8a9be-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8a9be-109">Il cmdlet **Remove-WAPackVM** rimuove gli oggetti macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a9be-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="8a9be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a9be-110">EXAMPLES</span></span>

### <span data-ttu-id="8a9be-111">Esempio 1: rimuovere una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8a9be-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="8a9be-112">Il primo comando ottiene la macchina virtuale denominata ContosoV126 usando il cmdlet **Get-WAPackVM** e quindi archivia tale oggetto nella variabile $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="8a9be-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8a9be-113">Il secondo comando rimuove la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8a9be-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="8a9be-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="8a9be-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8a9be-115">Esempio 2: rimuovere una macchina virtuale senza conferma</span><span class="sxs-lookup"><span data-stu-id="8a9be-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="8a9be-116">Il primo comando ottiene la macchina virtuale denominata ContosoV126 usando il cmdlet **Get-WAPackVM** e quindi archivia tale oggetto nella variabile $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="8a9be-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="8a9be-117">Il secondo comando rimuove la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="8a9be-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="8a9be-118">Questo comando include il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="8a9be-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="8a9be-119">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8a9be-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8a9be-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a9be-120">PARAMETERS</span></span>

### <span data-ttu-id="8a9be-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8a9be-121">-Force</span></span>
<span data-ttu-id="8a9be-122">Indica che il cmdlet rimuove una macchina virtuale senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8a9be-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9be-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a9be-123">-PassThru</span></span>
<span data-ttu-id="8a9be-124">Indica che il cmdlet restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="8a9be-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="8a9be-125">Se l'operazione riesce, il cmdlet restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="8a9be-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="8a9be-126">In caso contrario, restituisce un valore di $False.</span><span class="sxs-lookup"><span data-stu-id="8a9be-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="8a9be-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8a9be-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9be-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="8a9be-128">-Profile</span></span>
<span data-ttu-id="8a9be-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a9be-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a9be-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8a9be-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9be-131">-VM</span><span class="sxs-lookup"><span data-stu-id="8a9be-131">-VM</span></span>
<span data-ttu-id="8a9be-132">Specifica una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8a9be-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="8a9be-133">Per ottenere una macchina virtuale, usare il cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="8a9be-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9be-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a9be-134">-Confirm</span></span>
<span data-ttu-id="8a9be-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a9be-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9be-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a9be-136">-WhatIf</span></span>
<span data-ttu-id="8a9be-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a9be-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a9be-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a9be-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9be-139">CommonParameters</span></span>
<span data-ttu-id="8a9be-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a9be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9be-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a9be-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9be-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a9be-142">INPUTS</span></span>

## <span data-ttu-id="8a9be-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a9be-143">OUTPUTS</span></span>

## <span data-ttu-id="8a9be-144">Note</span><span class="sxs-lookup"><span data-stu-id="8a9be-144">NOTES</span></span>

## <span data-ttu-id="8a9be-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a9be-145">RELATED LINKS</span></span>

[<span data-ttu-id="8a9be-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="8a9be-147">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="8a9be-148">Riavviare-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="8a9be-149">Curriculum vitae-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="8a9be-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="8a9be-151">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="8a9be-152">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="8a9be-153">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8a9be-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


