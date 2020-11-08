---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018254"
---
# <span data-ttu-id="dbded-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="dbded-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="dbded-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbded-102">SYNOPSIS</span></span>
<span data-ttu-id="dbded-103">Aggiunge informazioni al file di risposte dell'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="dbded-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="dbded-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbded-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbded-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbded-105">DESCRIPTION</span></span>
<span data-ttu-id="dbded-106">Il cmdlet **Add-AzVMAdditionalUnattendContent** aggiunge informazioni al file di risposte per l'installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="dbded-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="dbded-107">Specifica altre informazioni in formato XML di base 64 codificate che questo cmdlet aggiunge al file unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="dbded-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="dbded-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbded-108">EXAMPLES</span></span>

### <span data-ttu-id="dbded-109">Esempio 1: aggiungere contenuto a unattend.xml</span><span class="sxs-lookup"><span data-stu-id="dbded-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="dbded-110">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dbded-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="dbded-111">Il secondo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dbded-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dbded-112">Il comando assegna un nome e una dimensione alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dbded-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="dbded-113">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dbded-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="dbded-114">Il terzo comando crea un oggetto Credential usando il cmdlet Get-Credential e quindi archivia il risultato nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="dbded-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="dbded-115">Il comando richiede un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="dbded-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="dbded-116">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="dbded-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="dbded-117">Il quarto comando usa il cmdlet **set-AzVMOperatingSystem** per configurare la macchina virtuale archiviata in $virtualmachine.</span><span class="sxs-lookup"><span data-stu-id="dbded-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="dbded-118">Il quinto comando assegna il contenuto alla variabile $AucContent.</span><span class="sxs-lookup"><span data-stu-id="dbded-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="dbded-119">Il contenuto include una password.</span><span class="sxs-lookup"><span data-stu-id="dbded-119">The content includes a password.</span></span>
<span data-ttu-id="dbded-120">Il comando finale aggiunge il contenuto archiviato in $AucContent al file unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="dbded-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="dbded-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbded-121">PARAMETERS</span></span>

### <span data-ttu-id="dbded-122">-Contenuto</span><span class="sxs-lookup"><span data-stu-id="dbded-122">-Content</span></span>
<span data-ttu-id="dbded-123">Specifica il contenuto formattato XML codificato in base 64.</span><span class="sxs-lookup"><span data-stu-id="dbded-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="dbded-124">Questo cmdlet aggiunge il contenuto al file unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="dbded-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="dbded-125">Il contenuto XML deve essere inferiore a 4 KB e deve includere l'elemento radice per l'impostazione o la caratteristica inserita in questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbded-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbded-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbded-126">-DefaultProfile</span></span>
<span data-ttu-id="dbded-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbded-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbded-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="dbded-128">-SettingName</span></span>
<span data-ttu-id="dbded-129">Specifica il nome dell'impostazione a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="dbded-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="dbded-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbded-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dbded-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="dbded-131">FirstLogonCommands</span></span>
- <span data-ttu-id="dbded-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="dbded-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbded-133">-VM</span><span class="sxs-lookup"><span data-stu-id="dbded-133">-VM</span></span>
<span data-ttu-id="dbded-134">Specifica l'oggetto macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbded-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="dbded-135">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="dbded-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="dbded-136">Crea un oggetto macchina virtuale usando il cmdlet [New-AzVMConfig](./New-AzVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="dbded-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbded-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbded-137">CommonParameters</span></span>
<span data-ttu-id="dbded-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbded-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbded-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbded-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbded-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbded-140">INPUTS</span></span>

### <span data-ttu-id="dbded-141">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dbded-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="dbded-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dbded-142">System.String</span></span>

### <span data-ttu-id="dbded-143">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. SettingNames, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dbded-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="dbded-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbded-144">OUTPUTS</span></span>

### <span data-ttu-id="dbded-145">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dbded-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dbded-146">Note</span><span class="sxs-lookup"><span data-stu-id="dbded-146">NOTES</span></span>

## <span data-ttu-id="dbded-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbded-147">RELATED LINKS</span></span>

[<span data-ttu-id="dbded-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dbded-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="dbded-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="dbded-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="dbded-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dbded-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
