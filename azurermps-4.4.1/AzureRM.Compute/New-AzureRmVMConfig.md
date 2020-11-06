---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 2022a8a830d868f412e505f23e65c4c297bea543
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521747"
---
# <span data-ttu-id="c0719-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c0719-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="c0719-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0719-102">SYNOPSIS</span></span>
<span data-ttu-id="c0719-103">Crea un oggetto macchina virtuale configurabile.</span><span class="sxs-lookup"><span data-stu-id="c0719-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0719-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0719-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [[-IdentityType] <ResourceIdentityType>] [-AssignIdentity] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0719-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0719-105">DESCRIPTION</span></span>
<span data-ttu-id="c0719-106">Il cmdlet **New-AzureRmVMConfig** crea un oggetto macchina virtuale configurabile locale per Azure.</span><span class="sxs-lookup"><span data-stu-id="c0719-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="c0719-107">Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface e set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="c0719-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="c0719-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0719-108">EXAMPLES</span></span>

### <span data-ttu-id="c0719-109">Esempio 1: creare un oggetto macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c0719-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="c0719-110">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c0719-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="c0719-111">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c0719-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c0719-112">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0719-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c0719-113">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c0719-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="c0719-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0719-114">PARAMETERS</span></span>

### <span data-ttu-id="c0719-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c0719-115">-AssignIdentity</span></span>
<span data-ttu-id="c0719-116">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0719-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="c0719-117">-AvailabilitySetId</span></span>
<span data-ttu-id="c0719-118">Specifica l'ID di un set di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="c0719-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="c0719-119">Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzureRmAvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c0719-119">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="c0719-120">L'oggetto set di disponibilità contiene una proprietà ID.</span><span class="sxs-lookup"><span data-stu-id="c0719-120">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0719-121">-DefaultProfile</span></span>
<span data-ttu-id="c0719-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0719-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c0719-123">-IdentityType</span></span>
<span data-ttu-id="c0719-124">Identità della macchina virtuale, se configurata.</span><span class="sxs-lookup"><span data-stu-id="c0719-124">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c0719-125">-LicenseType</span></span>
<span data-ttu-id="c0719-126">Il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="c0719-126">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0719-127">-Tags</span></span>
<span data-ttu-id="c0719-128">Tag allegati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="c0719-128">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="c0719-129">-VMName</span></span>
<span data-ttu-id="c0719-130">Specifica un nome per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0719-130">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-131">-VMSize</span><span class="sxs-lookup"><span data-stu-id="c0719-131">-VMSize</span></span>
<span data-ttu-id="c0719-132">Specifica le dimensioni per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0719-132">Specifies the size for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-133">-Zona</span><span class="sxs-lookup"><span data-stu-id="c0719-133">-Zone</span></span>
<span data-ttu-id="c0719-134">Specifica l'elenco delle aree per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c0719-134">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0719-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0719-135">CommonParameters</span></span>
<span data-ttu-id="c0719-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0719-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0719-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0719-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0719-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0719-138">INPUTS</span></span>

## <span data-ttu-id="c0719-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0719-139">OUTPUTS</span></span>

## <span data-ttu-id="c0719-140">Note</span><span class="sxs-lookup"><span data-stu-id="c0719-140">NOTES</span></span>

## <span data-ttu-id="c0719-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0719-141">RELATED LINKS</span></span>

[<span data-ttu-id="c0719-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c0719-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="c0719-143">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c0719-143">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="c0719-144">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="c0719-144">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="c0719-145">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0719-145">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


