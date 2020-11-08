---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030847"
---
# <span data-ttu-id="32a4d-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-101">Set-WAPackVM</span></span>

## <span data-ttu-id="32a4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="32a4d-103">Modifica le proprietà delle dimensioni di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32a4d-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="32a4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32a4d-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="32a4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="32a4d-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="32a4d-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="32a4d-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32a4d-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="32a4d-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="32a4d-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="32a4d-109">Il cmdlet **set-WAPackVM** modifica le proprietà delle dimensioni di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32a4d-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="32a4d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32a4d-110">EXAMPLES</span></span>

### <span data-ttu-id="32a4d-111">Esempio 1: specificare le dimensioni per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="32a4d-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="32a4d-112">Il primo comando ottiene la macchina virtuale denominata ContosoV126 usando il cmdlet **Get-WAPackVM** e quindi archivia tale oggetto nella variabile $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="32a4d-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="32a4d-113">Il secondo comando ottiene il profilo di dimensione denominato MediumSizeVM usando il cmdlet **Get-WAPackVMSizeProfile** e quindi archivia tale oggetto nella variabile $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="32a4d-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="32a4d-114">Il comando finale assegna il profilo di dimensione archiviato in $SizeProfile alla macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="32a4d-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="32a4d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32a4d-115">PARAMETERS</span></span>

### <span data-ttu-id="32a4d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32a4d-116">-PassThru</span></span>
<span data-ttu-id="32a4d-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="32a4d-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32a4d-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="32a4d-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32a4d-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="32a4d-119">-Profile</span></span>
<span data-ttu-id="32a4d-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32a4d-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32a4d-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="32a4d-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32a4d-122">-VM</span><span class="sxs-lookup"><span data-stu-id="32a4d-122">-VM</span></span>
<span data-ttu-id="32a4d-123">Specifica una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="32a4d-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="32a4d-124">Per ottenere una macchina virtuale, usare il cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="32a4d-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="32a4d-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="32a4d-125">-VMSizeProfile</span></span>
<span data-ttu-id="32a4d-126">Specifica un profilo di dimensione per una macchina virtuale come oggetto **HardwareProfile** .</span><span class="sxs-lookup"><span data-stu-id="32a4d-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="32a4d-127">Per ottenere un profilo di dimensione, usare il cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="32a4d-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a4d-128">CommonParameters</span></span>
<span data-ttu-id="32a4d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a4d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a4d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a4d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32a4d-131">INPUTS</span></span>

## <span data-ttu-id="32a4d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32a4d-132">OUTPUTS</span></span>

## <span data-ttu-id="32a4d-133">Note</span><span class="sxs-lookup"><span data-stu-id="32a4d-133">NOTES</span></span>

## <span data-ttu-id="32a4d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32a4d-134">RELATED LINKS</span></span>

[<span data-ttu-id="32a4d-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="32a4d-136">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="32a4d-137">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="32a4d-138">Riavviare-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="32a4d-139">Curriculum vitae-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="32a4d-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="32a4d-141">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="32a4d-142">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="32a4d-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="32a4d-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="32a4d-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


