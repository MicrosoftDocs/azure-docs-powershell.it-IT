---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301555"
---
# <span data-ttu-id="5e559-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5e559-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="5e559-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e559-102">SYNOPSIS</span></span>
<span data-ttu-id="5e559-103">Disabilita la crittografia in una macchina virtuale IaaS.</span><span class="sxs-lookup"><span data-stu-id="5e559-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="5e559-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e559-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e559-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e559-105">DESCRIPTION</span></span>
<span data-ttu-id="5e559-106">Il cmdlet **Disable-AzVMDiskEncryption Disabilita** la crittografia in una macchina virtuale dell'infrastruttura come servizio (IaaS).</span><span class="sxs-lookup"><span data-stu-id="5e559-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="5e559-107">Questo cmdlet è supportato solo in macchine virtuali Windows e non in macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="5e559-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="5e559-108">Questo cmdlet installa un'estensione nella macchina virtuale per disabilitare la crittografia.</span><span class="sxs-lookup"><span data-stu-id="5e559-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="5e559-109">Se il parametro *Name* non è specificato, viene creata un'estensione con il nome predefinito "AzureDiskEncryption per Windows VM".</span><span class="sxs-lookup"><span data-stu-id="5e559-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="5e559-110">Attenzione: questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5e559-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="5e559-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e559-111">EXAMPLES</span></span>

### <span data-ttu-id="5e559-112">Esempio 1: disabilitare la crittografia per tutti i volumi in una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="5e559-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="5e559-113">Questo comando Disabilita la crittografia per i volumi di tipo all per la macchina virtuale denominata VM002 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="5e559-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="5e559-114">Dato che il parametro *VolumeType* non è specificato, il cmdlet imposta il valore su All.</span><span class="sxs-lookup"><span data-stu-id="5e559-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="5e559-115">Esempio 2: disabilitare la crittografia per i volumi di dati in una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="5e559-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="5e559-116">Questo comando Disabilita la crittografia per i volumi di dati di tipo per la macchina virtuale denominata VM004 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="5e559-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="5e559-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e559-117">PARAMETERS</span></span>

### <span data-ttu-id="5e559-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e559-118">-DefaultProfile</span></span>
<span data-ttu-id="5e559-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e559-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e559-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5e559-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5e559-121">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5e559-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="5e559-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="5e559-123">Nome dell'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5e559-123">The extension publisher name.</span></span> <span data-ttu-id="5e559-124">Specifica questo parametro solo per eseguire l'override del valore predefinito "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="5e559-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="5e559-125">-ExtensionType</span></span>
<span data-ttu-id="5e559-126">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="5e559-126">The extension type.</span></span> <span data-ttu-id="5e559-127">Specifica questo parametro per eseguire l'override del valore predefinito "AzureDiskEncryption" per le VM di Windows e "AzureDiskEncryptionForLinux" per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="5e559-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-128">-Force</span><span class="sxs-lookup"><span data-stu-id="5e559-128">-Force</span></span>
<span data-ttu-id="5e559-129">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5e559-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e559-130">-Name</span></span>
<span data-ttu-id="5e559-131">Specifica il nome della risorsa di Azure Resource Manager (ARM) che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="5e559-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="5e559-132">Se questo parametro non viene specificato, questo cmdlet viene impostato su "AzureDiskEncryption for Windows VM".</span><span class="sxs-lookup"><span data-stu-id="5e559-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e559-133">-ResourceGroupName</span></span>
<span data-ttu-id="5e559-134">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5e559-134">Specifies the resource group name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5e559-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="5e559-136">Specifica la versione dell'estensione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="5e559-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="5e559-137">Se non specifichi un valore per questo parametro, viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5e559-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="5e559-138">-VMName</span></span>
<span data-ttu-id="5e559-139">Specifica il nome della macchina virtuale in cui questo cmdlet disabilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="5e559-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="5e559-140">-VolumeType</span></span>
<span data-ttu-id="5e559-141">Specifica il tipo di volumi della macchina virtuale per eseguire l'operazione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="5e559-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="5e559-142">Per le macchine virtuali Windows, i valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5e559-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="5e559-143">Tutti</span><span class="sxs-lookup"><span data-stu-id="5e559-143">All</span></span>
- <span data-ttu-id="5e559-144">OS</span><span class="sxs-lookup"><span data-stu-id="5e559-144">OS</span></span>
- <span data-ttu-id="5e559-145">Dati.</span><span class="sxs-lookup"><span data-stu-id="5e559-145">Data.</span></span>
<span data-ttu-id="5e559-146">Se non specifichi un valore per questo parametro, il valore predefinito è all.</span><span class="sxs-lookup"><span data-stu-id="5e559-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="5e559-147">Disabilita la crittografia non è attualmente supportata per Linux.</span><span class="sxs-lookup"><span data-stu-id="5e559-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e559-148">-Confirm</span></span>
<span data-ttu-id="5e559-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e559-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e559-150">-WhatIf</span></span>
<span data-ttu-id="5e559-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e559-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e559-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e559-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e559-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e559-153">CommonParameters</span></span>
<span data-ttu-id="5e559-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e559-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e559-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e559-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e559-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e559-156">INPUTS</span></span>

### <span data-ttu-id="5e559-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5e559-157">System.String</span></span>

### <span data-ttu-id="5e559-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5e559-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5e559-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e559-159">OUTPUTS</span></span>

### <span data-ttu-id="5e559-160">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5e559-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5e559-161">Note</span><span class="sxs-lookup"><span data-stu-id="5e559-161">NOTES</span></span>

## <span data-ttu-id="5e559-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e559-162">RELATED LINKS</span></span>

[<span data-ttu-id="5e559-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="5e559-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="5e559-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5e559-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="5e559-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5e559-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


