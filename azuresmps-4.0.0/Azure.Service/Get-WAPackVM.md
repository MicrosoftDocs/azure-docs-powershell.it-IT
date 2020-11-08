---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030818"
---
# <span data-ttu-id="74c1c-101">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-101">Get-WAPackVM</span></span>

## <span data-ttu-id="74c1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="74c1c-103">Ottiene oggetti macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="74c1c-103">Gets virtual machine objects.</span></span>

## <span data-ttu-id="74c1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74c1c-104">SYNTAX</span></span>

### <span data-ttu-id="74c1c-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="74c1c-105">Empty (Default)</span></span>
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="74c1c-106">FromName</span><span class="sxs-lookup"><span data-stu-id="74c1c-106">FromName</span></span>
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="74c1c-107">FromId</span><span class="sxs-lookup"><span data-stu-id="74c1c-107">FromId</span></span>
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74c1c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="74c1c-109">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="74c1c-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="74c1c-110">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="74c1c-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="74c1c-111">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="74c1c-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="74c1c-112">Il cmdlet **Get-WAPackVM** ottiene oggetti macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="74c1c-112">The **Get-WAPackVM** cmdlet gets virtual machine objects.</span></span>

## <span data-ttu-id="74c1c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74c1c-113">EXAMPLES</span></span>

### <span data-ttu-id="74c1c-114">Esempio 1: ottenere una macchina virtuale usando un nome</span><span class="sxs-lookup"><span data-stu-id="74c1c-114">Example 1: Get a virtual machine by using a name</span></span>
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

<span data-ttu-id="74c1c-115">Questo comando consente di ottenere la macchina virtuale denominata ContosoV126.</span><span class="sxs-lookup"><span data-stu-id="74c1c-115">This command gets the virtual machine named ContosoV126.</span></span>

### <span data-ttu-id="74c1c-116">Esempio 2: ottenere una macchina virtuale usando un ID</span><span class="sxs-lookup"><span data-stu-id="74c1c-116">Example 2: Get a virtual machine by using an ID</span></span>
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="74c1c-117">Questo comando consente di ottenere la macchina virtuale con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="74c1c-117">This command gets the virtual machine that has the specified ID.</span></span>

### <span data-ttu-id="74c1c-118">Esempio 3: ottenere tutte le macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="74c1c-118">Example 3: Get all virtual machines</span></span>
```
PS C:\> Get-WAPackVM
```

<span data-ttu-id="74c1c-119">Questo comando consente di ottenere tutte le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="74c1c-119">This command gets all virtual machines.</span></span>

## <span data-ttu-id="74c1c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74c1c-120">PARAMETERS</span></span>

### <span data-ttu-id="74c1c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="74c1c-121">-ID</span></span>
<span data-ttu-id="74c1c-122">Specifica l'ID univoco di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="74c1c-122">Specifies the unique ID of a virtual machine.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c1c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="74c1c-123">-Name</span></span>
<span data-ttu-id="74c1c-124">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="74c1c-124">Specifies the name of a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c1c-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="74c1c-125">-Profile</span></span>
<span data-ttu-id="74c1c-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74c1c-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74c1c-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="74c1c-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74c1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c1c-128">CommonParameters</span></span>
<span data-ttu-id="74c1c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c1c-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c1c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74c1c-131">INPUTS</span></span>

## <span data-ttu-id="74c1c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74c1c-132">OUTPUTS</span></span>

## <span data-ttu-id="74c1c-133">Note</span><span class="sxs-lookup"><span data-stu-id="74c1c-133">NOTES</span></span>

## <span data-ttu-id="74c1c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74c1c-134">RELATED LINKS</span></span>

[<span data-ttu-id="74c1c-135">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-135">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="74c1c-136">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-136">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="74c1c-137">Riavviare-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-137">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="74c1c-138">Curriculum vitae-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-138">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="74c1c-139">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-139">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="74c1c-140">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="74c1c-141">Stop-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="74c1c-142">Suspend-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="74c1c-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="74c1c-143">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="74c1c-143">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


