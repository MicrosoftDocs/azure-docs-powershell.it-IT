---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030862"
---
# <span data-ttu-id="95eec-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="95eec-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="95eec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95eec-102">SYNOPSIS</span></span>
<span data-ttu-id="95eec-103">Crea una macchina virtuale basata su un modello.</span><span class="sxs-lookup"><span data-stu-id="95eec-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="95eec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95eec-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="95eec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95eec-105">DESCRIPTION</span></span>
<span data-ttu-id="95eec-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="95eec-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="95eec-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="95eec-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95eec-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="95eec-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95eec-109">Il cmdlet **New-WAPackQuickVM** crea una macchina virtuale basata su un modello.</span><span class="sxs-lookup"><span data-stu-id="95eec-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="95eec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95eec-110">EXAMPLES</span></span>

### <span data-ttu-id="95eec-111">Esempio 1: creare una macchina virtuale basata su un modello</span><span class="sxs-lookup"><span data-stu-id="95eec-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="95eec-112">Il primo comando crea un oggetto **PSCredential** e lo archivia nella variabile $Credentials.</span><span class="sxs-lookup"><span data-stu-id="95eec-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="95eec-113">Il cmdlet richiede l'accesso a un account e una password.</span><span class="sxs-lookup"><span data-stu-id="95eec-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="95eec-114">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="95eec-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="95eec-115">Il secondo comando ottiene un modello usando il cmdlet **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="95eec-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="95eec-116">Il comando specifica l'ID di un modello.</span><span class="sxs-lookup"><span data-stu-id="95eec-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="95eec-117">Il comando Archivia l'oggetto modello nella variabile $TemplateID.</span><span class="sxs-lookup"><span data-stu-id="95eec-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="95eec-118">Il comando finale crea una macchina virtuale denominata VirtualMachine023.</span><span class="sxs-lookup"><span data-stu-id="95eec-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="95eec-119">Il comando basa la macchina virtuale nel modello archiviato in $TemplateId.</span><span class="sxs-lookup"><span data-stu-id="95eec-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="95eec-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95eec-120">PARAMETERS</span></span>

### <span data-ttu-id="95eec-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="95eec-121">-Name</span></span>
<span data-ttu-id="95eec-122">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="95eec-122">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95eec-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="95eec-123">-Profile</span></span>
<span data-ttu-id="95eec-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95eec-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95eec-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="95eec-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95eec-126">-Modello</span><span class="sxs-lookup"><span data-stu-id="95eec-126">-Template</span></span>
<span data-ttu-id="95eec-127">Specifica un modello.</span><span class="sxs-lookup"><span data-stu-id="95eec-127">Specifies a template.</span></span>
<span data-ttu-id="95eec-128">Il cmdlet crea una macchina virtuale in base al modello specificato.</span><span class="sxs-lookup"><span data-stu-id="95eec-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="95eec-129">Per ottenere un oggetto modello, usare il cmdlet **Get-WAPackVMTemplate** .</span><span class="sxs-lookup"><span data-stu-id="95eec-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95eec-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="95eec-130">-VMCredential</span></span>
<span data-ttu-id="95eec-131">Specifica le credenziali per l'account di amministratore locale.</span><span class="sxs-lookup"><span data-stu-id="95eec-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="95eec-132">Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="95eec-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="95eec-133">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="95eec-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95eec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95eec-134">CommonParameters</span></span>
<span data-ttu-id="95eec-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95eec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95eec-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95eec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95eec-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95eec-137">INPUTS</span></span>

## <span data-ttu-id="95eec-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95eec-138">OUTPUTS</span></span>

## <span data-ttu-id="95eec-139">Note</span><span class="sxs-lookup"><span data-stu-id="95eec-139">NOTES</span></span>

## <span data-ttu-id="95eec-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95eec-140">RELATED LINKS</span></span>

[<span data-ttu-id="95eec-141">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="95eec-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="95eec-142">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="95eec-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


