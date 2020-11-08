---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023844"
---
# <span data-ttu-id="e5aff-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="e5aff-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="e5aff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5aff-102">SYNOPSIS</span></span>
<span data-ttu-id="e5aff-103">Crea una subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5aff-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="e5aff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5aff-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5aff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5aff-105">DESCRIPTION</span></span>
<span data-ttu-id="e5aff-106">Il cmdlet **New-WAPackVMSubnet** crea una subnet macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5aff-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="e5aff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5aff-107">EXAMPLES</span></span>

### <span data-ttu-id="e5aff-108">Esempio 1: creare una subnet macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e5aff-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="e5aff-109">Il primo comando recupera prima di tutto la rete della macchina virtuale a cui si vuole aggiungere una nuova subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5aff-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="e5aff-110">Questa rete di macchine virtuali è denominata ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="e5aff-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="e5aff-111">Il secondo comando crea una subnet macchina virtuale usando la rete Virtual Machine di recupero in precedenza, un nome ContosoVMSubnet01 e una subnet 192.168.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="e5aff-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="e5aff-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5aff-112">PARAMETERS</span></span>

### <span data-ttu-id="e5aff-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5aff-113">-Name</span></span>
<span data-ttu-id="e5aff-114">Specifica un nome per la subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5aff-114">Specifies a name for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5aff-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e5aff-115">-Profile</span></span>
<span data-ttu-id="e5aff-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5aff-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5aff-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e5aff-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5aff-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="e5aff-118">-Subnet</span></span>
<span data-ttu-id="e5aff-119">Specifica una subnet per la subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5aff-119">Specifies a subnet for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5aff-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="e5aff-120">-VNet</span></span>
<span data-ttu-id="e5aff-121">Specifica un VNet associato alla subnet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e5aff-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

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

### <span data-ttu-id="e5aff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5aff-122">CommonParameters</span></span>
<span data-ttu-id="e5aff-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5aff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5aff-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5aff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5aff-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5aff-125">INPUTS</span></span>

## <span data-ttu-id="e5aff-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5aff-126">OUTPUTS</span></span>

## <span data-ttu-id="e5aff-127">Note</span><span class="sxs-lookup"><span data-stu-id="e5aff-127">NOTES</span></span>

## <span data-ttu-id="e5aff-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5aff-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5aff-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="e5aff-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="e5aff-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="e5aff-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="e5aff-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="e5aff-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


