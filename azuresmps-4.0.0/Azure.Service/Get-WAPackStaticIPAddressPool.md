---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030893"
---
# <span data-ttu-id="92bb5-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="92bb5-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="92bb5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="92bb5-103">Ottiene gli oggetti del pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="92bb5-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="92bb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92bb5-104">SYNTAX</span></span>

### <span data-ttu-id="92bb5-105">FromVMSubnetObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92bb5-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="92bb5-106">FromName</span><span class="sxs-lookup"><span data-stu-id="92bb5-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="92bb5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92bb5-107">DESCRIPTION</span></span>
<span data-ttu-id="92bb5-108">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="92bb5-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="92bb5-109">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="92bb5-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="92bb5-110">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="92bb5-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="92bb5-111">Il cmdlet **Get-WAPackStaticIPAddressPool** ottiene gli oggetti pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="92bb5-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="92bb5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92bb5-112">EXAMPLES</span></span>

### <span data-ttu-id="92bb5-113">Esempio 1: ottenere un pool di indirizzi IP statici da un VMSubnet specifico</span><span class="sxs-lookup"><span data-stu-id="92bb5-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="92bb5-114">Questo comando ottiene il pool di indirizzi IP statici denominato ContosoStaticIPAddressPool01 da un VMSubnet specificato.</span><span class="sxs-lookup"><span data-stu-id="92bb5-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="92bb5-115">Esempio 2: ottenere tutti i pool di indirizzi IP statici da un VMSubnet specifico</span><span class="sxs-lookup"><span data-stu-id="92bb5-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="92bb5-116">Questo comando recupera tutti i pool IP statici da un VMSubet specificato.</span><span class="sxs-lookup"><span data-stu-id="92bb5-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="92bb5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92bb5-117">PARAMETERS</span></span>

### <span data-ttu-id="92bb5-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="92bb5-118">-Name</span></span>
<span data-ttu-id="92bb5-119">Specifica il nome di un pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="92bb5-119">Specifies the name of a static IP address pool.</span></span>

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

### <span data-ttu-id="92bb5-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="92bb5-120">-Profile</span></span>
<span data-ttu-id="92bb5-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92bb5-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92bb5-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="92bb5-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92bb5-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="92bb5-123">-VMSubnet</span></span>
<span data-ttu-id="92bb5-124">Specifica l'oggetto **VMSubnet** associato al pool di indirizzi IP statici.</span><span class="sxs-lookup"><span data-stu-id="92bb5-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="92bb5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bb5-125">CommonParameters</span></span>
<span data-ttu-id="92bb5-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bb5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bb5-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92bb5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bb5-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92bb5-128">INPUTS</span></span>

## <span data-ttu-id="92bb5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92bb5-129">OUTPUTS</span></span>

## <span data-ttu-id="92bb5-130">Note</span><span class="sxs-lookup"><span data-stu-id="92bb5-130">NOTES</span></span>

## <span data-ttu-id="92bb5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92bb5-131">RELATED LINKS</span></span>

[<span data-ttu-id="92bb5-132">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="92bb5-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="92bb5-133">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="92bb5-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


