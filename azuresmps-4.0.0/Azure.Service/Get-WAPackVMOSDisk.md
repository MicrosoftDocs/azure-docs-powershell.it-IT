---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030814"
---
# <span data-ttu-id="5a4ac-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="5a4ac-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="5a4ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a4ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4ac-103">Ottiene gli oggetti disco del sistema operativo per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="5a4ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a4ac-104">SYNTAX</span></span>

### <span data-ttu-id="5a4ac-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a4ac-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a4ac-106">FromId</span><span class="sxs-lookup"><span data-stu-id="5a4ac-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5a4ac-107">FromName</span><span class="sxs-lookup"><span data-stu-id="5a4ac-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a4ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a4ac-108">DESCRIPTION</span></span>
<span data-ttu-id="5a4ac-109">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5a4ac-110">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5a4ac-111">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5a4ac-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5a4ac-112">Il cmdlet **Get-WAPackVMOSDisk** ottiene gli oggetti disco del sistema operativo per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="5a4ac-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a4ac-113">EXAMPLES</span></span>

### <span data-ttu-id="5a4ac-114">Esempio 1: ottenere un disco del sistema operativo usando un nome</span><span class="sxs-lookup"><span data-stu-id="5a4ac-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="5a4ac-115">Questo comando consente di ottenere un disco del sistema operativo denominato ContosoOSDisk.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="5a4ac-116">Esempio 2: ottenere un disco del sistema operativo usando un ID</span><span class="sxs-lookup"><span data-stu-id="5a4ac-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="5a4ac-117">Questo comando consente di ottenere il disco del sistema operativo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="5a4ac-118">Esempio 3: ottenere tutti i dischi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5a4ac-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="5a4ac-119">Questo comando consente di ottenere tutti i dischi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="5a4ac-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a4ac-120">PARAMETERS</span></span>

### <span data-ttu-id="5a4ac-121">-ID</span><span class="sxs-lookup"><span data-stu-id="5a4ac-121">-ID</span></span>
<span data-ttu-id="5a4ac-122">Specifica l'ID univoco di un disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-122">Specifies the unique ID of an operating system disk.</span></span>

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

### <span data-ttu-id="5a4ac-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a4ac-123">-Name</span></span>
<span data-ttu-id="5a4ac-124">Specifica il nome di un disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-124">Specifies the name of an operating system disk.</span></span>

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

### <span data-ttu-id="5a4ac-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="5a4ac-125">-Profile</span></span>
<span data-ttu-id="5a4ac-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5a4ac-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a4ac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4ac-128">CommonParameters</span></span>
<span data-ttu-id="5a4ac-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4ac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4ac-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a4ac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4ac-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a4ac-131">INPUTS</span></span>

## <span data-ttu-id="5a4ac-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a4ac-132">OUTPUTS</span></span>

## <span data-ttu-id="5a4ac-133">Note</span><span class="sxs-lookup"><span data-stu-id="5a4ac-133">NOTES</span></span>

## <span data-ttu-id="5a4ac-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a4ac-134">RELATED LINKS</span></span>

[<span data-ttu-id="5a4ac-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5a4ac-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


