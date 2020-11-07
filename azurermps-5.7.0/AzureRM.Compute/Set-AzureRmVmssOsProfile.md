---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: ee9649d7a2a88dd3a91f428201ddc66d1a6562da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687929"
---
# <span data-ttu-id="5874a-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5874a-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="5874a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5874a-102">SYNOPSIS</span></span>
<span data-ttu-id="5874a-103">Imposta le proprietà del profilo del sistema operativo VMSS.</span><span class="sxs-lookup"><span data-stu-id="5874a-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5874a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5874a-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5874a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5874a-105">DESCRIPTION</span></span>
<span data-ttu-id="5874a-106">Il cmdlet **set-AzureRmVmssOsProfile** imposta la scala della macchina virtuale imposta le proprietà del profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5874a-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="5874a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5874a-107">EXAMPLES</span></span>

### <span data-ttu-id="5874a-108">Esempio 1: impostare le proprietà del profilo del sistema operativo per un VMSS</span><span class="sxs-lookup"><span data-stu-id="5874a-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="5874a-109">Questo comando imposta le proprietà del profilo del sistema operativo per le macchine virtuali che appartengono al VMSS denominato ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="5874a-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="5874a-110">Il comando imposta il prefisso del nome computer per tutte le istanze della macchina virtuale in VMSS per testare e fornire il nome utente e la password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="5874a-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="5874a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5874a-111">PARAMETERS</span></span>

### <span data-ttu-id="5874a-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="5874a-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="5874a-113">Specifica un oggetto contenuto non presidiato.</span><span class="sxs-lookup"><span data-stu-id="5874a-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="5874a-114">Puoi usare la Add-AzureRmVMAdditionalUnattendContent per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5874a-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="5874a-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="5874a-115">-AdminPassword</span></span>
<span data-ttu-id="5874a-116">Specifica la password di amministratore da usare per tutte le istanze della macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="5874a-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="5874a-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="5874a-117">-AdminUsername</span></span>
<span data-ttu-id="5874a-118">Specifica il nome dell'account di amministratore da usare per tutte le istanze della macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="5874a-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="5874a-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="5874a-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="5874a-120">Specifica il prefisso del nome computer per tutte le istanze della macchina virtuale in VMSS.</span><span class="sxs-lookup"><span data-stu-id="5874a-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="5874a-121">I nomi dei computer devono essere lunghi da 1 a 15 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5874a-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="5874a-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="5874a-122">-CustomData</span></span>
<span data-ttu-id="5874a-123">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="5874a-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="5874a-124">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5874a-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="5874a-125">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="5874a-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="5874a-126">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="5874a-126">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="5874a-127">Indica che questo cmdlet disabilita l'autenticazione tramite password.</span><span class="sxs-lookup"><span data-stu-id="5874a-127">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="5874a-128">-Listener</span><span class="sxs-lookup"><span data-stu-id="5874a-128">-Listener</span></span>
<span data-ttu-id="5874a-129">Specifica i listener di gestione remota (WinRM) di Windows.</span><span class="sxs-lookup"><span data-stu-id="5874a-129">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="5874a-130">In questo modo viene abilitato Windows PowerShell remoto.</span><span class="sxs-lookup"><span data-stu-id="5874a-130">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="5874a-131">Puoi usare il cmdlet Add-AzureRmVmssWinRMListener per creare il listener.</span><span class="sxs-lookup"><span data-stu-id="5874a-131">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="5874a-132">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="5874a-132">-PublicKey</span></span>
<span data-ttu-id="5874a-133">Specifica l'oggetto chiave pubblica Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="5874a-133">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="5874a-134">Puoi usare il cmdlet Add-AzureRmVMSshPublicKey per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5874a-134">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="5874a-135">-Segreto</span><span class="sxs-lookup"><span data-stu-id="5874a-135">-Secret</span></span>
<span data-ttu-id="5874a-136">Specifica l'oggetto Secrets che contiene i riferimenti di certificato da posizionare nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5874a-136">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="5874a-137">Puoi usare il cmdlet Add-AzureRmVmssSecret per creare l'oggetto Secrets.</span><span class="sxs-lookup"><span data-stu-id="5874a-137">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="5874a-138">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="5874a-138">-TimeZone</span></span>
<span data-ttu-id="5874a-139">Specifica il fuso orario per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5874a-139">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="5874a-140">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5874a-140">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5874a-141">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="5874a-141">Specifies the VMSS object.</span></span>
<span data-ttu-id="5874a-142">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5874a-142">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5874a-143">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="5874a-143">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="5874a-144">Indica se le macchine virtuali in VMSS sono abilitate per gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="5874a-144">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="5874a-145">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="5874a-145">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="5874a-146">Indica se l'agente macchina virtuale deve essere eseguito il provisioning sulle macchine virtuali in VMSS.</span><span class="sxs-lookup"><span data-stu-id="5874a-146">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="5874a-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5874a-147">-Confirm</span></span>
<span data-ttu-id="5874a-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5874a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5874a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5874a-149">-WhatIf</span></span>
<span data-ttu-id="5874a-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5874a-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5874a-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5874a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5874a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5874a-152">CommonParameters</span></span>
<span data-ttu-id="5874a-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5874a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5874a-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5874a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5874a-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5874a-155">INPUTS</span></span>

### <span data-ttu-id="5874a-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5874a-156">None</span></span>
<span data-ttu-id="5874a-157">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5874a-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5874a-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5874a-158">OUTPUTS</span></span>

### <span data-ttu-id="5874a-159">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="5874a-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5874a-160">Note</span><span class="sxs-lookup"><span data-stu-id="5874a-160">NOTES</span></span>

## <span data-ttu-id="5874a-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5874a-161">RELATED LINKS</span></span>

[<span data-ttu-id="5874a-162">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="5874a-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="5874a-163">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="5874a-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="5874a-164">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="5874a-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="5874a-165">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="5874a-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="5874a-166">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5874a-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


