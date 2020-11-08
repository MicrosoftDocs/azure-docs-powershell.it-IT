---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023820"
---
# <span data-ttu-id="a091a-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="a091a-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="a091a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a091a-102">SYNOPSIS</span></span>
<span data-ttu-id="a091a-103">Imposta le informazioni sull'indirizzo IP VNet statico per un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a091a-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="a091a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a091a-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a091a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a091a-105">DESCRIPTION</span></span>
<span data-ttu-id="a091a-106">Il cmdlet **set-AzureStaticVNetIP** imposta le informazioni sull'indirizzo IP della rete virtuale statica (VNet) per un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a091a-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="a091a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a091a-107">EXAMPLES</span></span>

### <span data-ttu-id="a091a-108">Esempio 1: impostare l'indirizzo IP di rete virtuale associato a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a091a-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="a091a-109">Il primo comando imposta il percorso di configurazione per una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a091a-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="a091a-110">Il secondo comando crea una configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a091a-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="a091a-111">Il terzo comando imposta la subnet per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a091a-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="a091a-112">Il quarto comando imposta l'indirizzo IP per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a091a-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="a091a-113">Il quinto comando crea una macchina virtuale usando la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a091a-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="a091a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a091a-114">PARAMETERS</span></span>

### <span data-ttu-id="a091a-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a091a-115">-InformationAction</span></span>
<span data-ttu-id="a091a-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a091a-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a091a-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a091a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a091a-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="a091a-118">Continue</span></span>
- <span data-ttu-id="a091a-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="a091a-119">Ignore</span></span>
- <span data-ttu-id="a091a-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a091a-120">Inquire</span></span>
- <span data-ttu-id="a091a-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a091a-121">SilentlyContinue</span></span>
- <span data-ttu-id="a091a-122">Stop</span><span class="sxs-lookup"><span data-stu-id="a091a-122">Stop</span></span>
- <span data-ttu-id="a091a-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a091a-123">Suspend</span></span>

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

### <span data-ttu-id="a091a-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a091a-124">-InformationVariable</span></span>
<span data-ttu-id="a091a-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a091a-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a091a-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a091a-126">-IPAddress</span></span>
<span data-ttu-id="a091a-127">Specifica l'indirizzo IP VNet statico</span><span class="sxs-lookup"><span data-stu-id="a091a-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a091a-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="a091a-128">-Profile</span></span>
<span data-ttu-id="a091a-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a091a-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a091a-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a091a-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a091a-131">-VM</span><span class="sxs-lookup"><span data-stu-id="a091a-131">-VM</span></span>
<span data-ttu-id="a091a-132">Specifica un oggetto macchina virtuale persistente per cui impostare l'indirizzo IP VNet statico.</span><span class="sxs-lookup"><span data-stu-id="a091a-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="a091a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a091a-133">CommonParameters</span></span>
<span data-ttu-id="a091a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a091a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a091a-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a091a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a091a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a091a-136">INPUTS</span></span>

## <span data-ttu-id="a091a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a091a-137">OUTPUTS</span></span>

## <span data-ttu-id="a091a-138">Note</span><span class="sxs-lookup"><span data-stu-id="a091a-138">NOTES</span></span>

## <span data-ttu-id="a091a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a091a-139">RELATED LINKS</span></span>

[<span data-ttu-id="a091a-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="a091a-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="a091a-141">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="a091a-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


