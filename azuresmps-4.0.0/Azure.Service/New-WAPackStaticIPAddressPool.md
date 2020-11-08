---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030843"
---
# <span data-ttu-id="2f774-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="2f774-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="2f774-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f774-102">SYNOPSIS</span></span>
<span data-ttu-id="2f774-103">Crea un pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="2f774-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f774-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f774-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f774-105">DESCRIPTION</span></span>
<span data-ttu-id="2f774-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="2f774-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="2f774-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2f774-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2f774-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2f774-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2f774-109">Il cmdlet **New-WAPackStaticIPAddressPool** crea un pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="2f774-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f774-110">EXAMPLES</span></span>

### <span data-ttu-id="2f774-111">Esempio 1: creare un pool di indirizzi IP statici</span><span class="sxs-lookup"><span data-stu-id="2f774-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="2f774-112">Il primo comando recupera prima di tutto la rete della macchina virtuale a cui si vuole aggiungere il pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="2f774-113">Questa rete di macchine virtuali è denominata ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="2f774-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="2f774-114">Il secondo comando usa la rete Virtual Machine recuperata in precedenza per ottenere la subnet della macchina virtuale denominata ContosoVMSubnet01 a cui si vuole aggiungere il pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="2f774-115">L'ultimo comando crea un nuovo pool di indirizzi IP statici con un nome ContosoStaticIpAddressPool01 e un intervallo di inizio 192.168.1.0 e un intervallo di fine 192.168.1.10.</span><span class="sxs-lookup"><span data-stu-id="2f774-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="2f774-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f774-116">PARAMETERS</span></span>

### <span data-ttu-id="2f774-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="2f774-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="2f774-118">Specifica una fine dell'intervallo di indirizzi IP per il pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-118">Specifies an IP address range end for the static IP address pool.</span></span>

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

### <span data-ttu-id="2f774-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="2f774-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="2f774-120">Specifica l'inizio di un intervallo di indirizzi IP per il pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-120">Specifies an IP address range start for the static IP address pool.</span></span>

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

### <span data-ttu-id="2f774-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f774-121">-Name</span></span>
<span data-ttu-id="2f774-122">Specifica un nome per il pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-122">Specifies a name for the static IP address pool.</span></span>

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

### <span data-ttu-id="2f774-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="2f774-123">-Profile</span></span>
<span data-ttu-id="2f774-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f774-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f774-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2f774-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f774-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="2f774-126">-VMSubnet</span></span>
<span data-ttu-id="2f774-127">Specifica un VMSubnet associato al pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="2f774-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

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

### <span data-ttu-id="2f774-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f774-128">CommonParameters</span></span>
<span data-ttu-id="2f774-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f774-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f774-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f774-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f774-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f774-131">INPUTS</span></span>

## <span data-ttu-id="2f774-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f774-132">OUTPUTS</span></span>

## <span data-ttu-id="2f774-133">Note</span><span class="sxs-lookup"><span data-stu-id="2f774-133">NOTES</span></span>

## <span data-ttu-id="2f774-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f774-134">RELATED LINKS</span></span>

[<span data-ttu-id="2f774-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="2f774-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="2f774-136">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="2f774-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


