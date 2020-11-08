---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030817"
---
# <span data-ttu-id="10ebf-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="10ebf-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="10ebf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="10ebf-103">Ottiene gli oggetti subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10ebf-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="10ebf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10ebf-104">SYNTAX</span></span>

### <span data-ttu-id="10ebf-105">FromVMNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10ebf-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="10ebf-106">FromName</span><span class="sxs-lookup"><span data-stu-id="10ebf-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="10ebf-107">FromId</span><span class="sxs-lookup"><span data-stu-id="10ebf-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10ebf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10ebf-108">DESCRIPTION</span></span>
<span data-ttu-id="10ebf-109">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="10ebf-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="10ebf-110">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="10ebf-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="10ebf-111">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="10ebf-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="10ebf-112">Il cmdlet **Get-WAPackVMSubnet** ottiene gli oggetti subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10ebf-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="10ebf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10ebf-113">EXAMPLES</span></span>

### <span data-ttu-id="10ebf-114">Esempio 1: ottenere una subnet della macchina virtuale usando un nome</span><span class="sxs-lookup"><span data-stu-id="10ebf-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="10ebf-115">Questo comando consente di ottenere la subnet della macchina virtuale denominata ContosoSubnet01.</span><span class="sxs-lookup"><span data-stu-id="10ebf-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="10ebf-116">Esempio 2: ottenere una subnet della macchina virtuale usando un ID</span><span class="sxs-lookup"><span data-stu-id="10ebf-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="10ebf-117">Questo comando consente di ottenere la subnet della macchina virtuale con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="10ebf-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="10ebf-118">Esempio 3: ottenere tutte le subnet della macchina virtuale da una determinata rete virtualizzata</span><span class="sxs-lookup"><span data-stu-id="10ebf-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="10ebf-119">Questo comando consente di ottenere tutte le subnet della macchina virtuale da una determinata rete virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="10ebf-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="10ebf-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10ebf-120">PARAMETERS</span></span>

### <span data-ttu-id="10ebf-121">-ID</span><span class="sxs-lookup"><span data-stu-id="10ebf-121">-ID</span></span>
<span data-ttu-id="10ebf-122">Specifica l'ID univoco di una subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10ebf-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ebf-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="10ebf-123">-Name</span></span>
<span data-ttu-id="10ebf-124">Specifica il nome di una subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10ebf-124">Specifies the name of a virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10ebf-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="10ebf-125">-Profile</span></span>
<span data-ttu-id="10ebf-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10ebf-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10ebf-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="10ebf-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10ebf-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="10ebf-128">-VNet</span></span>
<span data-ttu-id="10ebf-129">Specifica il VNet associato a una subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10ebf-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10ebf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ebf-130">CommonParameters</span></span>
<span data-ttu-id="10ebf-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ebf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ebf-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ebf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ebf-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10ebf-133">INPUTS</span></span>

## <span data-ttu-id="10ebf-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10ebf-134">OUTPUTS</span></span>

## <span data-ttu-id="10ebf-135">Note</span><span class="sxs-lookup"><span data-stu-id="10ebf-135">NOTES</span></span>

## <span data-ttu-id="10ebf-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10ebf-136">RELATED LINKS</span></span>

[<span data-ttu-id="10ebf-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="10ebf-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="10ebf-138">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="10ebf-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="10ebf-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="10ebf-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


