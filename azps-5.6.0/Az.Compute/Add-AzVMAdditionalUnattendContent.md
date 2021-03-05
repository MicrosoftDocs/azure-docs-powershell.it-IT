---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 2ec50d8e0c11143f72e327a7b73784c1a49e926c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991562"
---
# <span data-ttu-id="7259e-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="7259e-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="7259e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7259e-102">SYNOPSIS</span></span>
<span data-ttu-id="7259e-103">Aggiunge informazioni al file di risposte di Installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="7259e-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="7259e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7259e-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7259e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7259e-105">DESCRIPTION</span></span>
<span data-ttu-id="7259e-106">Il cmdlet **Add-AzVMAdditionalUnattendContent** aggiunge informazioni al file di risposte di Installazione automatica di Windows.</span><span class="sxs-lookup"><span data-stu-id="7259e-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="7259e-107">Specificare altre informazioni formattate in formato XML codificato in base 64 che questo cmdlet aggiunge al file unattend.xml base.</span><span class="sxs-lookup"><span data-stu-id="7259e-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="7259e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7259e-108">EXAMPLES</span></span>

### <span data-ttu-id="7259e-109">Esempio 1: Aggiungere contenuto unattend.xml</span><span class="sxs-lookup"><span data-stu-id="7259e-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="7259e-110">Il primo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.</span><span class="sxs-lookup"><span data-stu-id="7259e-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="7259e-111">Il secondo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.</span><span class="sxs-lookup"><span data-stu-id="7259e-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7259e-112">Il comando assegna un nome e le dimensioni alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7259e-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7259e-113">La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7259e-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="7259e-114">Il terzo comando crea un oggetto credenziali usando il cmdlet Get-Credential e quindi archivia il risultato nella $Credential variabile.</span><span class="sxs-lookup"><span data-stu-id="7259e-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="7259e-115">Il comando chiede di specificare un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="7259e-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="7259e-116">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="7259e-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="7259e-117">Il quarto comando usa il cmdlet **Set-AzVMOperatingSystem** per configurare la macchina virtuale archiviata in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7259e-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7259e-118">Il quinto comando assegna contenuto alla $AucContent variabile.</span><span class="sxs-lookup"><span data-stu-id="7259e-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="7259e-119">Il contenuto include una password.</span><span class="sxs-lookup"><span data-stu-id="7259e-119">The content includes a password.</span></span>
<span data-ttu-id="7259e-120">Il comando finale aggiunge il contenuto archiviato in $AucContent al file unattend.xml finale.</span><span class="sxs-lookup"><span data-stu-id="7259e-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="7259e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7259e-121">PARAMETERS</span></span>

### <span data-ttu-id="7259e-122">-Content</span><span class="sxs-lookup"><span data-stu-id="7259e-122">-Content</span></span>
<span data-ttu-id="7259e-123">Specifica il contenuto in formato XML codificato in base 64.</span><span class="sxs-lookup"><span data-stu-id="7259e-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="7259e-124">Questo cmdlet aggiunge il contenuto al file unattend.xml file.</span><span class="sxs-lookup"><span data-stu-id="7259e-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="7259e-125">Il contenuto XML deve essere inferiore a 4 KB e deve includere l'elemento radice per l'impostazione o la caratteristica inserita dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7259e-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="7259e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7259e-126">-DefaultProfile</span></span>
<span data-ttu-id="7259e-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7259e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7259e-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="7259e-128">-SettingName</span></span>
<span data-ttu-id="7259e-129">Specifica il nome dell'impostazione a cui si applica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="7259e-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="7259e-130">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7259e-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7259e-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="7259e-131">FirstLogonCommands</span></span>
- <span data-ttu-id="7259e-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="7259e-132">AutoLogon</span></span>

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

### <span data-ttu-id="7259e-133">-VM</span><span class="sxs-lookup"><span data-stu-id="7259e-133">-VM</span></span>
<span data-ttu-id="7259e-134">Specifica l'oggetto della macchina virtuale modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7259e-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="7259e-135">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="7259e-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="7259e-136">Creare un oggetto macchina virtuale usando il cmdlet [New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="7259e-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="7259e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7259e-137">CommonParameters</span></span>
<span data-ttu-id="7259e-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7259e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7259e-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7259e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7259e-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="7259e-140">INPUTS</span></span>

### <span data-ttu-id="7259e-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7259e-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7259e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7259e-142">System.String</span></span>

### <span data-ttu-id="7259e-143">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7259e-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7259e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7259e-144">OUTPUTS</span></span>

### <span data-ttu-id="7259e-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7259e-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7259e-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="7259e-146">NOTES</span></span>

## <span data-ttu-id="7259e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7259e-147">RELATED LINKS</span></span>

[<span data-ttu-id="7259e-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7259e-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="7259e-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7259e-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="7259e-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7259e-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
