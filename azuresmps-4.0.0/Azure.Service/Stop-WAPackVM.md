---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4FB7096E-DDA1-474C-BF0C-D910681BE58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4ef4660761ab29e738050c0445534602accda6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030858"
---
# <span data-ttu-id="7e9fc-101">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-101">Stop-WAPackVM</span></span>

## <span data-ttu-id="7e9fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9fc-103">Arresta una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-103">Stops a virtual machine.</span></span>

## <span data-ttu-id="7e9fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e9fc-104">SYNTAX</span></span>

```
Stop-WAPackVM [-Shutdown] -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7e9fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e9fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7e9fc-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7e9fc-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7e9fc-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7e9fc-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7e9fc-109">Il cmdlet **Stop-WAPackVM** arresta una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-109">The **Stop-WAPackVM** cmdlet stops a virtual machine.</span></span>

## <span data-ttu-id="7e9fc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e9fc-110">EXAMPLES</span></span>

### <span data-ttu-id="7e9fc-111">Esempio 1: arrestare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7e9fc-111">Example 1: Stop a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Stop-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="7e9fc-112">Il primo comando ottiene la macchina virtuale denominata ContosoV126 usando il cmdlet **Get-WAPackVM** e quindi archivia tale oggetto nella variabile $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7e9fc-113">Il secondo comando interrompe la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-113">The second command stops the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="7e9fc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e9fc-114">PARAMETERS</span></span>

### <span data-ttu-id="7e9fc-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e9fc-115">-PassThru</span></span>
<span data-ttu-id="7e9fc-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e9fc-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e9fc-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="7e9fc-118">-Profile</span></span>
<span data-ttu-id="7e9fc-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e9fc-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e9fc-121">-Arresto</span><span class="sxs-lookup"><span data-stu-id="7e9fc-121">-Shutdown</span></span>
<span data-ttu-id="7e9fc-122">Indica che il cmdlet chiude il sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-122">Indicates that the cmdlet shuts down the operating system of the virtual machine.</span></span>

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

### <span data-ttu-id="7e9fc-123">-VM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-123">-VM</span></span>
<span data-ttu-id="7e9fc-124">Specifica una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-124">Specifies a virtual machine.</span></span>
<span data-ttu-id="7e9fc-125">Per ottenere una macchina virtuale, usare il cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="7e9fc-125">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="7e9fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9fc-126">CommonParameters</span></span>
<span data-ttu-id="7e9fc-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e9fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9fc-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9fc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9fc-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e9fc-129">INPUTS</span></span>

## <span data-ttu-id="7e9fc-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e9fc-130">OUTPUTS</span></span>

## <span data-ttu-id="7e9fc-131">Note</span><span class="sxs-lookup"><span data-stu-id="7e9fc-131">NOTES</span></span>

## <span data-ttu-id="7e9fc-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e9fc-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e9fc-133">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-133">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="7e9fc-134">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-134">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="7e9fc-135">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-135">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="7e9fc-136">Riavviare-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-136">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="7e9fc-137">Curriculum vitae-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-137">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="7e9fc-138">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-138">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="7e9fc-139">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-139">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="7e9fc-140">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7e9fc-140">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


