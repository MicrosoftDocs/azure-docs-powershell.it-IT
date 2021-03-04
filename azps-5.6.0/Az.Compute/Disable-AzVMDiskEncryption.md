---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: bd96a26eda14770dcc7a5592e12e64e15eac02f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969437"
---
# <span data-ttu-id="15db7-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="15db7-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="15db7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15db7-102">SYNOPSIS</span></span>
<span data-ttu-id="15db7-103">Disabilita la crittografia in una macchina virtuale IaaS.</span><span class="sxs-lookup"><span data-stu-id="15db7-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="15db7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15db7-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15db7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15db7-105">DESCRIPTION</span></span>
<span data-ttu-id="15db7-106">Il cmdlet **Disable-AzVMDiskEncryption** disabilita la crittografia di un'infrastruttura come macchina virtuale di servizio (IaaS).</span><span class="sxs-lookup"><span data-stu-id="15db7-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="15db7-107">Questo cmdlet è supportato solo in macchine virtuali Windows e non in macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="15db7-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="15db7-108">Questo cmdlet installa un'estensione nella macchina virtuale per disabilitare la crittografia.</span><span class="sxs-lookup"><span data-stu-id="15db7-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="15db7-109">Se non *si* specifica il parametro Name, viene creata un'estensione con il nome predefinito "AzureDiskEncryption for Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="15db7-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="15db7-110">Attenzione: questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="15db7-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="15db7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15db7-111">EXAMPLES</span></span>

### <span data-ttu-id="15db7-112">Esempio 1: Disabilitare la crittografia per tutti i volumi in una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="15db7-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="15db7-113">Questo comando disabilita la crittografia per volumi di tipo tutti per la macchina virtuale denominata VM002 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="15db7-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="15db7-114">Poiché il *parametro VolumeType* non è specificato, il cmdlet imposta il valore su All.</span><span class="sxs-lookup"><span data-stu-id="15db7-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="15db7-115">Esempio 2: Disabilitare la crittografia per volumi di dati in una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="15db7-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="15db7-116">Questo comando disabilita la crittografia per volumi di dati tipo per la macchina virtuale denominata VM004 che appartiene al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="15db7-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="15db7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15db7-117">PARAMETERS</span></span>

### <span data-ttu-id="15db7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15db7-118">-DefaultProfile</span></span>
<span data-ttu-id="15db7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15db7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15db7-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="15db7-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="15db7-121">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="15db7-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="15db7-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="15db7-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="15db7-123">Nome dell'autore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="15db7-123">The extension publisher name.</span></span> <span data-ttu-id="15db7-124">Specificare questo parametro solo per ignorare il valore predefinito di "Microsoft.Azure.Security".</span><span class="sxs-lookup"><span data-stu-id="15db7-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="15db7-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="15db7-125">-ExtensionType</span></span>
<span data-ttu-id="15db7-126">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="15db7-126">The extension type.</span></span> <span data-ttu-id="15db7-127">Specificare questo parametro per ignorare il valore predefinito "AzureDiskEncryption" per le macchine virtuali Windows e "AzureDiskEncryptionForLinux" per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="15db7-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="15db7-128">-Force</span><span class="sxs-lookup"><span data-stu-id="15db7-128">-Force</span></span>
<span data-ttu-id="15db7-129">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="15db7-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="15db7-130">-Name</span><span class="sxs-lookup"><span data-stu-id="15db7-130">-Name</span></span>
<span data-ttu-id="15db7-131">Specifica il nome della risorsa Gestione risorse di Azure (ARM) che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="15db7-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="15db7-132">Se questo parametro non è specificato, per impostazione predefinita questo cmdlet è "AzureDiskEncryption per le macchine virtuali Windows".</span><span class="sxs-lookup"><span data-stu-id="15db7-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="15db7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15db7-133">-ResourceGroupName</span></span>
<span data-ttu-id="15db7-134">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="15db7-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="15db7-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="15db7-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="15db7-136">Specifica la versione dell'estensione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="15db7-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="15db7-137">Se non si specifica un valore per questo parametro, viene usata la versione più recente dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="15db7-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="15db7-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="15db7-138">-VMName</span></span>
<span data-ttu-id="15db7-139">Specifica il nome della macchina virtuale per cui questo cmdlet disabilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="15db7-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="15db7-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="15db7-140">-VolumeType</span></span>
<span data-ttu-id="15db7-141">Specifica il tipo di volumi della macchina virtuale per eseguire l'operazione di crittografia.</span><span class="sxs-lookup"><span data-stu-id="15db7-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="15db7-142">Per le macchine virtuali Windows, i valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="15db7-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="15db7-143">Tutti</span><span class="sxs-lookup"><span data-stu-id="15db7-143">All</span></span>
- <span data-ttu-id="15db7-144">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="15db7-144">OS</span></span>
- <span data-ttu-id="15db7-145">Dati.</span><span class="sxs-lookup"><span data-stu-id="15db7-145">Data.</span></span>
<span data-ttu-id="15db7-146">Se non si specifica alcun valore per questo parametro, il valore predefinito è All.</span><span class="sxs-lookup"><span data-stu-id="15db7-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="15db7-147">La disabilitazione della crittografia non è attualmente supportata per Linux.</span><span class="sxs-lookup"><span data-stu-id="15db7-147">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="15db7-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15db7-148">-Confirm</span></span>
<span data-ttu-id="15db7-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15db7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15db7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15db7-150">-WhatIf</span></span>
<span data-ttu-id="15db7-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15db7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15db7-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15db7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15db7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15db7-153">CommonParameters</span></span>
<span data-ttu-id="15db7-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15db7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15db7-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="15db7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15db7-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="15db7-156">INPUTS</span></span>

### <span data-ttu-id="15db7-157">System.String</span><span class="sxs-lookup"><span data-stu-id="15db7-157">System.String</span></span>

### <span data-ttu-id="15db7-158">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15db7-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15db7-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15db7-159">OUTPUTS</span></span>

### <span data-ttu-id="15db7-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="15db7-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="15db7-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="15db7-161">NOTES</span></span>

## <span data-ttu-id="15db7-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15db7-162">RELATED LINKS</span></span>

[<span data-ttu-id="15db7-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="15db7-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="15db7-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="15db7-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="15db7-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="15db7-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


