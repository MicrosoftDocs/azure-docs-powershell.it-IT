---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8A6B4C8C-B990-443B-9157-B5C35824269A
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2d87c92f18c3aeb25aad210922dea0c93287fa6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030886"
---
# <span data-ttu-id="f1b14-101">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-101">Start-WAPackVM</span></span>

## <span data-ttu-id="f1b14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1b14-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b14-103">Avvia una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1b14-103">Starts a virtual machine.</span></span>

## <span data-ttu-id="f1b14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1b14-104">SYNTAX</span></span>

```
Start-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f1b14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1b14-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b14-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="f1b14-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f1b14-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b14-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f1b14-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f1b14-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f1b14-109">Il cmdlet **Start-WAPackVM** avvia una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1b14-109">The **Start-WAPackVM** cmdlet starts a virtual machine.</span></span>

## <span data-ttu-id="f1b14-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1b14-110">EXAMPLES</span></span>

### <span data-ttu-id="f1b14-111">Esempio 1: avviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="f1b14-111">Example 1: Start a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Start-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="f1b14-112">Il primo comando ottiene la macchina virtuale denominata ContosoV126 usando il cmdlet **Get-WAPackVM** e quindi archivia tale oggetto nella variabile $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="f1b14-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="f1b14-113">Il secondo comando avvia la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f1b14-113">The second command starts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="f1b14-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1b14-114">PARAMETERS</span></span>

### <span data-ttu-id="f1b14-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1b14-115">-PassThru</span></span>
<span data-ttu-id="f1b14-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f1b14-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1b14-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f1b14-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1b14-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="f1b14-118">-Profile</span></span>
<span data-ttu-id="f1b14-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b14-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1b14-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f1b14-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1b14-121">-VM</span><span class="sxs-lookup"><span data-stu-id="f1b14-121">-VM</span></span>
<span data-ttu-id="f1b14-122">Specifica una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f1b14-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="f1b14-123">Per ottenere una macchina virtuale, usare il cmdlet **Get-WAPackVM** .</span><span class="sxs-lookup"><span data-stu-id="f1b14-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="f1b14-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b14-124">CommonParameters</span></span>
<span data-ttu-id="f1b14-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b14-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b14-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b14-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b14-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1b14-127">INPUTS</span></span>

## <span data-ttu-id="f1b14-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1b14-128">OUTPUTS</span></span>

## <span data-ttu-id="f1b14-129">Note</span><span class="sxs-lookup"><span data-stu-id="f1b14-129">NOTES</span></span>

## <span data-ttu-id="f1b14-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1b14-130">RELATED LINKS</span></span>

[<span data-ttu-id="f1b14-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="f1b14-132">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="f1b14-133">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="f1b14-134">Riavviare-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="f1b14-135">Curriculum vitae-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="f1b14-136">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="f1b14-137">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="f1b14-138">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="f1b14-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


