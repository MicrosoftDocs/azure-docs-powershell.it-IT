---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030853"
---
# <span data-ttu-id="70336-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="70336-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="70336-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70336-102">SYNOPSIS</span></span>
<span data-ttu-id="70336-103">Ottiene i modelli di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="70336-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="70336-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70336-104">SYNTAX</span></span>

### <span data-ttu-id="70336-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70336-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="70336-106">FromId</span><span class="sxs-lookup"><span data-stu-id="70336-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="70336-107">FromName</span><span class="sxs-lookup"><span data-stu-id="70336-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="70336-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70336-108">DESCRIPTION</span></span>
<span data-ttu-id="70336-109">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="70336-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="70336-110">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="70336-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="70336-111">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="70336-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="70336-112">Il cmdlet **Get-WAPackVMTemplate** ottiene i modelli di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="70336-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="70336-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70336-113">EXAMPLES</span></span>

### <span data-ttu-id="70336-114">Esempio 1: ottenere un modello di macchina virtuale usando un nome</span><span class="sxs-lookup"><span data-stu-id="70336-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="70336-115">Questo comando ottiene il modello di macchina virtuale denominato ContosoTemplate04.</span><span class="sxs-lookup"><span data-stu-id="70336-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="70336-116">Esempio 2: ottenere un modello di macchina virtuale usando un ID</span><span class="sxs-lookup"><span data-stu-id="70336-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="70336-117">Questo comando ottiene il modello di macchina virtuale con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="70336-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="70336-118">Esempio 3: ottenere tutti i modelli di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="70336-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="70336-119">Questo comando consente di ottenere tutti i modelli di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="70336-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="70336-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70336-120">PARAMETERS</span></span>

### <span data-ttu-id="70336-121">-ID</span><span class="sxs-lookup"><span data-stu-id="70336-121">-ID</span></span>
<span data-ttu-id="70336-122">Specifica l'ID univoco di un modello.</span><span class="sxs-lookup"><span data-stu-id="70336-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="70336-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="70336-123">-Name</span></span>
<span data-ttu-id="70336-124">Specifica il nome di un modello.</span><span class="sxs-lookup"><span data-stu-id="70336-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="70336-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="70336-125">-Profile</span></span>
<span data-ttu-id="70336-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70336-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70336-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="70336-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70336-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70336-128">CommonParameters</span></span>
<span data-ttu-id="70336-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70336-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70336-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70336-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70336-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70336-131">INPUTS</span></span>

## <span data-ttu-id="70336-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70336-132">OUTPUTS</span></span>

## <span data-ttu-id="70336-133">Note</span><span class="sxs-lookup"><span data-stu-id="70336-133">NOTES</span></span>

## <span data-ttu-id="70336-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70336-134">RELATED LINKS</span></span>

[<span data-ttu-id="70336-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="70336-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


