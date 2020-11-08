---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030869"
---
# <span data-ttu-id="388d0-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="388d0-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="388d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="388d0-102">SYNOPSIS</span></span>
<span data-ttu-id="388d0-103">Rimuove gli oggetti subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="388d0-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="388d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="388d0-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="388d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="388d0-105">DESCRIPTION</span></span>
<span data-ttu-id="388d0-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="388d0-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="388d0-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="388d0-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="388d0-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="388d0-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="388d0-109">Il cmdlet **Remove-WAPackVMSubnet** rimuove gli oggetti subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="388d0-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="388d0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="388d0-110">EXAMPLES</span></span>

### <span data-ttu-id="388d0-111">Esempio 1: rimuovere una subnet della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="388d0-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="388d0-112">Il primo comando ottiene la subnet della macchina virtuale denominata ContosoVMSubnet01 usando il cmdlet **Get-WAPackVMSubnet** e quindi archivia tale oggetto nella variabile $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="388d0-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="388d0-113">Il secondo comando rimuove la subnet della macchina virtuale archiviata in $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="388d0-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="388d0-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="388d0-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="388d0-115">Esempio 2: rimuovere una macchina virtuale senza conferma</span><span class="sxs-lookup"><span data-stu-id="388d0-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="388d0-116">Il primo comando ottiene il servizio cloud denominato ContosoVMSubnet02 usando il cmdlet **Get-WAPackVMSubnet** e quindi archivia tale oggetto nella variabile $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="388d0-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="388d0-117">Il secondo comando rimuove la subnet della macchina virtuale archiviata in $VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="388d0-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="388d0-118">Questo comando include il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="388d0-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="388d0-119">Il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="388d0-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="388d0-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="388d0-120">PARAMETERS</span></span>

### <span data-ttu-id="388d0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="388d0-121">-Force</span></span>
<span data-ttu-id="388d0-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="388d0-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="388d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="388d0-123">-PassThru</span></span>
<span data-ttu-id="388d0-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="388d0-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="388d0-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="388d0-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="388d0-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="388d0-126">-Profile</span></span>
<span data-ttu-id="388d0-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="388d0-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="388d0-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="388d0-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="388d0-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="388d0-129">-VMSubnet</span></span>
<span data-ttu-id="388d0-130">Specifica una subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="388d0-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="388d0-131">Per ottenere una subnet della macchina virtuale, usare il cmdlet **Get-WAPackVMSubnet** .</span><span class="sxs-lookup"><span data-stu-id="388d0-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="388d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388d0-132">CommonParameters</span></span>
<span data-ttu-id="388d0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="388d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388d0-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388d0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="388d0-135">INPUTS</span></span>

## <span data-ttu-id="388d0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="388d0-136">OUTPUTS</span></span>

## <span data-ttu-id="388d0-137">Note</span><span class="sxs-lookup"><span data-stu-id="388d0-137">NOTES</span></span>

## <span data-ttu-id="388d0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="388d0-138">RELATED LINKS</span></span>

[<span data-ttu-id="388d0-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="388d0-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="388d0-140">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="388d0-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


