---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 046812a0339a0dd33df140f29e00ec8b882c91cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958893"
---
# <span data-ttu-id="8cc83-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="8cc83-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="8cc83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc83-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc83-103">Imposta le proprietà del profilo del sistema operativo VMSS.</span><span class="sxs-lookup"><span data-stu-id="8cc83-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="8cc83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cc83-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc83-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cc83-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc83-106">Il cmdlet **Set-AzVmssOsProfile** imposta le proprietà del profilo del sistema operativo Set di scalabilità macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cc83-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="8cc83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cc83-107">EXAMPLES</span></span>

### <span data-ttu-id="8cc83-108">Esempio 1: Impostare le proprietà del profilo del sistema operativo per un sistema VMSS</span><span class="sxs-lookup"><span data-stu-id="8cc83-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="8cc83-109">Questo comando imposta le proprietà del profilo del sistema operativo per le macchine virtuali appartenenti ai sistemi VMS denominati ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="8cc83-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="8cc83-110">Il comando imposta il prefisso del nome computer per tutte le istanze di macchine virtuali in VMSS su Test e fornisce il nome utente e la password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="8cc83-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="8cc83-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cc83-111">PARAMETERS</span></span>

### <span data-ttu-id="8cc83-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="8cc83-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="8cc83-113">Specifica un oggetto contenuto automatico.</span><span class="sxs-lookup"><span data-stu-id="8cc83-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="8cc83-114">È possibile usare la Add-AzVMAdditionalUnattendContent per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cc83-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="8cc83-115">-AdminPassword</span></span>
<span data-ttu-id="8cc83-116">Specifica la password dell'amministratore da usare per tutte le istanze di macchine virtuali nel sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8cc83-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="8cc83-117">-AdminUsername</span></span>
<span data-ttu-id="8cc83-118">Specifica il nome dell'account dell'amministratore da usare per tutte le istanze di macchine virtuali nel sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8cc83-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="8cc83-119">**Restrizione solo per Windows:** Non può terminare con \" .\"</span><span class="sxs-lookup"><span data-stu-id="8cc83-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="8cc83-120">**Valori non consentiti:** \" administrator \" , admin , user , \" \" \" \" \" user1 , test , \" \" \" \" user2 , \" \" test1 , \" \" user3 , \" \" admin1 , \" \" 1 , \" \" 123 , a , actuser , adm , admin2 , aspnet , backup , \" console \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" , david , guest , owner , root , server , sql , support , support_388945a0 , sys , test2 , test3 , user4 , user5.</span><span class="sxs-lookup"><span data-stu-id="8cc83-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="8cc83-121">**Lunghezza minima (Linux):** 1 carattere</span><span class="sxs-lookup"><span data-stu-id="8cc83-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="8cc83-122">**Lunghezza max (Linux):** 64 caratteri</span><span class="sxs-lookup"><span data-stu-id="8cc83-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="8cc83-123">**Lunghezza massima (Windows):** 20 caratteri</span><span class="sxs-lookup"><span data-stu-id="8cc83-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="8cc83-124">Per l'accesso radice a Linux VM, vedere Uso dei privilegi radice nelle [macchine virtuali Linux in Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="8cc83-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="8cc83-125">Per un elenco degli utenti di sistema predefiniti su Linux che non devono essere usati in questo campo, vedi Selezione dei nomi utente [per Linux in Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="8cc83-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="8cc83-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="8cc83-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="8cc83-127">Specifica il prefisso del nome computer per tutte le istanze di macchine virtuali nel sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8cc83-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="8cc83-128">I nomi dei computer devono contenere da 1 a 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="8cc83-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="8cc83-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="8cc83-129">-CustomData</span></span>
<span data-ttu-id="8cc83-130">Specifica una stringa di dati personalizzati codificata in base 64.</span><span class="sxs-lookup"><span data-stu-id="8cc83-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="8cc83-131">Questa decodifica viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cc83-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="8cc83-132">La lunghezza massima della matrice binaria è 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="8cc83-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="8cc83-133">Per l'uso di cloud-init per la macchina virtuale, vedi Uso [di cloud-init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)per personalizzare una macchina virtuale Linux durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="8cc83-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc83-134">-DefaultProfile</span></span>
<span data-ttu-id="8cc83-135">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc83-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cc83-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="8cc83-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="8cc83-137">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="8cc83-137">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="8cc83-138">-Listener</span></span>
<span data-ttu-id="8cc83-139">Specifica i listener di Gestione remota Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="8cc83-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="8cc83-140">In questo modo, Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cc83-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="8cc83-141">È possibile usare il cmdlet Add-AzVmssWinRMListener per creare il listener.</span><span class="sxs-lookup"><span data-stu-id="8cc83-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="8cc83-142">-PublicKey</span></span>
<span data-ttu-id="8cc83-143">Specifica l'oggetto chiave pubblica Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="8cc83-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="8cc83-144">È possibile usare il cmdlet Add-AzVMSshPublicKey per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cc83-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="8cc83-145">-Secret</span></span>
<span data-ttu-id="8cc83-146">Specifica l'oggetto segreto che contiene i riferimenti al certificato da inserire nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cc83-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="8cc83-147">È possibile usare il cmdlet Add-AzVmssSecret per creare l'oggetto segreto.</span><span class="sxs-lookup"><span data-stu-id="8cc83-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="8cc83-148">-TimeZone</span></span>
<span data-ttu-id="8cc83-149">Specifica il fuso orario della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8cc83-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="8cc83-150">ad esempio Ora \" solare \" Pacifico.</span><span class="sxs-lookup"><span data-stu-id="8cc83-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="8cc83-151">I valori possibili possono essere [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) da fusi orari restituiti da [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="8cc83-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8cc83-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8cc83-153">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="8cc83-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="8cc83-154">È possibile usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cc83-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="8cc83-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="8cc83-156">Indica se le macchine virtuali nel sistema VMS sono abilitate per gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="8cc83-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="8cc83-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="8cc83-158">Indica se è necessario eseguire il provisioning dell'agente di macchina virtuale nelle macchine virtuali nel sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="8cc83-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cc83-159">-Confirm</span></span>
<span data-ttu-id="8cc83-160">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc83-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc83-161">-WhatIf</span></span>
<span data-ttu-id="8cc83-162">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cc83-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cc83-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cc83-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cc83-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc83-164">CommonParameters</span></span>
<span data-ttu-id="8cc83-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc83-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc83-166">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8cc83-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc83-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cc83-167">INPUTS</span></span>

### <span data-ttu-id="8cc83-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8cc83-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8cc83-169">System.String</span><span class="sxs-lookup"><span data-stu-id="8cc83-169">System.String</span></span>

### <span data-ttu-id="8cc83-170">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8cc83-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8cc83-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span><span class="sxs-lookup"><span data-stu-id="8cc83-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="8cc83-172">Microsoft.Azure.Management.Compute.Models.WinRMDir[]</span><span class="sxs-lookup"><span data-stu-id="8cc83-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="8cc83-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span><span class="sxs-lookup"><span data-stu-id="8cc83-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="8cc83-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span><span class="sxs-lookup"><span data-stu-id="8cc83-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="8cc83-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cc83-175">OUTPUTS</span></span>

### <span data-ttu-id="8cc83-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8cc83-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8cc83-177">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cc83-177">NOTES</span></span>

## <span data-ttu-id="8cc83-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cc83-178">RELATED LINKS</span></span>

[<span data-ttu-id="8cc83-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="8cc83-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="8cc83-180">Add-AzVmssWinRMDir</span><span class="sxs-lookup"><span data-stu-id="8cc83-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="8cc83-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="8cc83-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="8cc83-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="8cc83-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="8cc83-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8cc83-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


