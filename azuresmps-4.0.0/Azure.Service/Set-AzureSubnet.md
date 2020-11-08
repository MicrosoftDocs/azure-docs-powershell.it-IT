---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023909"
---
# <span data-ttu-id="02721-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="02721-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="02721-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02721-102">SYNOPSIS</span></span>
<span data-ttu-id="02721-103">Definisce l'elenco subnet per una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="02721-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="02721-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02721-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="02721-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02721-105">DESCRIPTION</span></span>
<span data-ttu-id="02721-106">Il cmdlet **set-AzureSubnet** imposta l'elenco subnet per una configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="02721-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="02721-107">Usare con **New-AzureVM** per impostare le subnet per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="02721-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="02721-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02721-108">EXAMPLES</span></span>

### <span data-ttu-id="02721-109">Esempio 1: aggiungere una subnet a una configurazione di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="02721-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="02721-110">Questo comando aggiunge una subnet alla configurazione della macchina virtuale e quindi crea la macchina virtuale denominata VirtualMachine04.</span><span class="sxs-lookup"><span data-stu-id="02721-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="02721-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02721-111">PARAMETERS</span></span>

### <span data-ttu-id="02721-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="02721-112">-InformationAction</span></span>
<span data-ttu-id="02721-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="02721-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="02721-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="02721-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="02721-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="02721-115">Continue</span></span>
- <span data-ttu-id="02721-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="02721-116">Ignore</span></span>
- <span data-ttu-id="02721-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="02721-117">Inquire</span></span>
- <span data-ttu-id="02721-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="02721-118">SilentlyContinue</span></span>
- <span data-ttu-id="02721-119">Stop</span><span class="sxs-lookup"><span data-stu-id="02721-119">Stop</span></span>
- <span data-ttu-id="02721-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="02721-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02721-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="02721-121">-InformationVariable</span></span>
<span data-ttu-id="02721-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="02721-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02721-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="02721-123">-Profile</span></span>
<span data-ttu-id="02721-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02721-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02721-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="02721-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02721-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="02721-126">-SubnetNames</span></span>
<span data-ttu-id="02721-127">Specifica una matrice che contiene l'elenco di nomi di subnet.</span><span class="sxs-lookup"><span data-stu-id="02721-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02721-128">-VM</span><span class="sxs-lookup"><span data-stu-id="02721-128">-VM</span></span>
<span data-ttu-id="02721-129">Specifica l'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="02721-129">Specifies the virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02721-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02721-130">CommonParameters</span></span>
<span data-ttu-id="02721-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02721-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02721-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02721-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02721-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02721-133">INPUTS</span></span>

## <span data-ttu-id="02721-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02721-134">OUTPUTS</span></span>

## <span data-ttu-id="02721-135">Note</span><span class="sxs-lookup"><span data-stu-id="02721-135">NOTES</span></span>

## <span data-ttu-id="02721-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02721-136">RELATED LINKS</span></span>

[<span data-ttu-id="02721-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="02721-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="02721-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="02721-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="02721-139">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="02721-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


