---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514531"
---
# <span data-ttu-id="281e9-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="281e9-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="281e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="281e9-102">SYNOPSIS</span></span>
<span data-ttu-id="281e9-103">Aggiunge informazioni al file di risposte dell'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="281e9-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="281e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="281e9-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## <span data-ttu-id="281e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="281e9-105">DESCRIPTION</span></span>
<span data-ttu-id="281e9-106">Il cmdlet **Add-AzureRmVMAdditionalUnattendContent** aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="281e9-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="281e9-107">Specifica altre informazioni in formato XML di base 64 codificate che questo cmdlet aggiunge al file unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="281e9-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="281e9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="281e9-108">EXAMPLES</span></span>

### <span data-ttu-id="281e9-109">Esempio 1: aggiungere contenuto a unattend.xml</span><span class="sxs-lookup"><span data-stu-id="281e9-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="281e9-110">Il primo comando ottiene il set di disponibilità denominato AvailablitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="281e9-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="281e9-111">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="281e9-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="281e9-112">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="281e9-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="281e9-113">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="281e9-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="281e9-114">Il terzo comando crea un oggetto Credential usando il cmdlet Get-Credential e quindi archivia il risultato nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="281e9-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="281e9-115">Il comando richiede un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="281e9-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="281e9-116">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="281e9-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="281e9-117">Il quarto comando usa il cmdlet **set-AzureRmVMOperatingSystem** per configurare la macchina virtuale archiviata in $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="281e9-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="281e9-118">Il quinto comando assegna il contenuto alla variabile $AucContent.</span><span class="sxs-lookup"><span data-stu-id="281e9-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="281e9-119">Il contenuto include una password.</span><span class="sxs-lookup"><span data-stu-id="281e9-119">The content includes a password.</span></span>

<span data-ttu-id="281e9-120">Il comando finale aggiunge il contenuto archiviato in $AucContent al file unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="281e9-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="281e9-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="281e9-121">PARAMETERS</span></span>

### <span data-ttu-id="281e9-122">-Contenuto</span><span class="sxs-lookup"><span data-stu-id="281e9-122">-Content</span></span>
<span data-ttu-id="281e9-123">Specifica il contenuto formattato XML codificato in base 64.</span><span class="sxs-lookup"><span data-stu-id="281e9-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="281e9-124">Questo cmdlet aggiunge il contenuto al file unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="281e9-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="281e9-125">Il contenuto XML deve essere inferiore a 4 KB e deve includere l'elemento radice per l'impostazione o la caratteristica inserita in questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="281e9-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="281e9-126">-SettingName</span><span class="sxs-lookup"><span data-stu-id="281e9-126">-SettingName</span></span>
<span data-ttu-id="281e9-127">Specifica il nome dell'impostazione a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="281e9-127">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="281e9-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="281e9-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="281e9-129">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="281e9-129">FirstLogonCommands</span></span>
- <span data-ttu-id="281e9-130">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="281e9-130">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="281e9-131">-VM</span><span class="sxs-lookup"><span data-stu-id="281e9-131">-VM</span></span>
<span data-ttu-id="281e9-132">Specifica l'oggetto macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="281e9-132">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="281e9-133">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="281e9-133">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="281e9-134">Crea un oggetto macchina virtuale usando il cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="281e9-134">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="281e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281e9-135">CommonParameters</span></span>
<span data-ttu-id="281e9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="281e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281e9-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="281e9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281e9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="281e9-138">INPUTS</span></span>

### <span data-ttu-id="281e9-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="281e9-139">None</span></span>
<span data-ttu-id="281e9-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="281e9-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="281e9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="281e9-141">OUTPUTS</span></span>

## <span data-ttu-id="281e9-142">Note</span><span class="sxs-lookup"><span data-stu-id="281e9-142">NOTES</span></span>

## <span data-ttu-id="281e9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="281e9-143">RELATED LINKS</span></span>

[<span data-ttu-id="281e9-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="281e9-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="281e9-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="281e9-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="281e9-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="281e9-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
