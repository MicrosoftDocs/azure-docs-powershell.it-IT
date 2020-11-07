---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 98ebce4e139d230607da77536492d0ba40d0760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863326"
---
# <span data-ttu-id="f015e-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f015e-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="f015e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f015e-102">SYNOPSIS</span></span>
<span data-ttu-id="f015e-103">Imposta le proprietà del profilo del sistema operativo VMSS.</span><span class="sxs-lookup"><span data-stu-id="f015e-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="f015e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f015e-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f015e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f015e-105">DESCRIPTION</span></span>
<span data-ttu-id="f015e-106">Il cmdlet **set-AzVmssOsProfile** imposta la scala della macchina virtuale imposta le proprietà del profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f015e-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="f015e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f015e-107">EXAMPLES</span></span>

### <span data-ttu-id="f015e-108">Esempio 1: impostare le proprietà del profilo del sistema operativo per un VMSS</span><span class="sxs-lookup"><span data-stu-id="f015e-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="f015e-109">Questo comando imposta le proprietà del profilo del sistema operativo per le macchine virtuali che appartengono al VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="f015e-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="f015e-110">Il comando imposta il prefisso del nome computer per tutte le istanze della macchina virtuale in VMSS per testare e fornire il nome utente e la password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="f015e-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="f015e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f015e-111">PARAMETERS</span></span>

### <span data-ttu-id="f015e-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="f015e-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="f015e-113">Specifica un oggetto contenuto non presidiato.</span><span class="sxs-lookup"><span data-stu-id="f015e-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="f015e-114">Puoi usare la Add-AzVMAdditionalUnattendContent per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f015e-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="f015e-115">-AdminPassword</span></span>
<span data-ttu-id="f015e-116">Specifica la password di amministratore da usare per tutte le istanze della macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="f015e-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="f015e-117">-AdminUsername</span></span>
<span data-ttu-id="f015e-118">Specifica il nome dell'account di amministratore da usare per tutte le istanze della macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="f015e-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f015e-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="f015e-120">Specifica il prefisso del nome computer per tutte le istanze della macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="f015e-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="f015e-121">I nomi dei computer devono essere lunghi da 1 a 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f015e-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="f015e-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="f015e-122">-CustomData</span></span>
<span data-ttu-id="f015e-123">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f015e-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="f015e-124">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f015e-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="f015e-125">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="f015e-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f015e-126">-DefaultProfile</span></span>
<span data-ttu-id="f015e-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f015e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="f015e-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="f015e-129">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="f015e-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="f015e-130">-Listener</span></span>
<span data-ttu-id="f015e-131">Specifica i listener di gestione remota (WinRM) di Windows.</span><span class="sxs-lookup"><span data-stu-id="f015e-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="f015e-132">In questo modo viene abilitato Windows PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="f015e-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="f015e-133">Puoi usare il cmdlet Add-AzVmssWinRMListener per creare il listener.</span><span class="sxs-lookup"><span data-stu-id="f015e-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="f015e-134">-PublicKey</span></span>
<span data-ttu-id="f015e-135">Specifica l'oggetto chiave pubblica Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="f015e-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="f015e-136">Puoi usare il cmdlet Add-AzVMSshPublicKey per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f015e-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-137">-Segreto</span><span class="sxs-lookup"><span data-stu-id="f015e-137">-Secret</span></span>
<span data-ttu-id="f015e-138">Specifica l'oggetto Secrets che contiene i riferimenti di certificato da posizionare nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f015e-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="f015e-139">Puoi usare il cmdlet Add-AzVmssSecret per creare l'oggetto Secrets.</span><span class="sxs-lookup"><span data-stu-id="f015e-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="f015e-140">-TimeZone</span></span>
<span data-ttu-id="f015e-141">Specifica il fuso orario per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f015e-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f015e-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f015e-143">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="f015e-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="f015e-144">Puoi usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f015e-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="f015e-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="f015e-146">Indica se le macchine virtuali in VMSS sono abilitate per gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="f015e-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="f015e-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="f015e-148">Indica se l'agente macchina virtuale deve essere eseguito il provisioning sulle macchine virtuali in VMSS.</span><span class="sxs-lookup"><span data-stu-id="f015e-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f015e-149">-Confirm</span></span>
<span data-ttu-id="f015e-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f015e-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f015e-151">-WhatIf</span></span>
<span data-ttu-id="f015e-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f015e-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f015e-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f015e-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f015e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f015e-154">CommonParameters</span></span>
<span data-ttu-id="f015e-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f015e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f015e-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f015e-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f015e-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f015e-157">INPUTS</span></span>

### <span data-ttu-id="f015e-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f015e-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="f015e-159">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f015e-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="f015e-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f015e-160">OUTPUTS</span></span>

### <span data-ttu-id="f015e-161">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f015e-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f015e-162">Note</span><span class="sxs-lookup"><span data-stu-id="f015e-162">NOTES</span></span>

## <span data-ttu-id="f015e-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f015e-163">RELATED LINKS</span></span>

[<span data-ttu-id="f015e-164">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="f015e-164">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="f015e-165">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="f015e-165">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="f015e-166">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f015e-166">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="f015e-167">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="f015e-167">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="f015e-168">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f015e-168">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


