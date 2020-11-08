---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030845"
---
# <span data-ttu-id="e9b9f-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e9b9f-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="e9b9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b9f-103">Modifica la proprietà conteggio istanze di un ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="e9b9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9b9f-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b9f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9b9f-105">DESCRIPTION</span></span>
<span data-ttu-id="e9b9f-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e9b9f-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e9b9f-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e9b9f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e9b9f-109">Il cmdlet **set-WAPackVMRole** modifica la proprietà conteggio istanze di un ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="e9b9f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9b9f-110">EXAMPLES</span></span>

### <span data-ttu-id="e9b9f-111">Esempio 1: specificare il conteggio delle istanze per un ruolo macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e9b9f-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="e9b9f-112">Il primo comando ottiene il ruolo della macchina virtuale denominato ContosoVMRole01 usando il cmdlet **Get-WAPackVMRole** e quindi archivia tale oggetto nella variabile $VMRole.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="e9b9f-113">Il secondo e ultimo comando imposta il nuovo conteggio delle istanze del ruolo della macchina virtuale archiviato in $VMRole su 3.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="e9b9f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9b9f-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b9f-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e9b9f-115">-InstanceCount</span></span>
<span data-ttu-id="e9b9f-116">Specifica il conteggio delle istanze per un ruolo di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b9f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9b9f-117">-PassThru</span></span>
<span data-ttu-id="e9b9f-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e9b9f-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e9b9f-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="e9b9f-120">-Profile</span></span>
<span data-ttu-id="e9b9f-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9b9f-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9b9f-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="e9b9f-123">-VMRole</span></span>
<span data-ttu-id="e9b9f-124">Specifica un ruolo macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="e9b9f-125">Per ottenere un ruolo di macchina virtuale, usare il cmdlet **Get-WAPackVMRole** .</span><span class="sxs-lookup"><span data-stu-id="e9b9f-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b9f-126">CommonParameters</span></span>
<span data-ttu-id="e9b9f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b9f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b9f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b9f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9b9f-129">INPUTS</span></span>

## <span data-ttu-id="e9b9f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9b9f-130">OUTPUTS</span></span>

## <span data-ttu-id="e9b9f-131">Note</span><span class="sxs-lookup"><span data-stu-id="e9b9f-131">NOTES</span></span>

## <span data-ttu-id="e9b9f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9b9f-132">RELATED LINKS</span></span>

[<span data-ttu-id="e9b9f-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e9b9f-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="e9b9f-134">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e9b9f-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="e9b9f-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="e9b9f-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


