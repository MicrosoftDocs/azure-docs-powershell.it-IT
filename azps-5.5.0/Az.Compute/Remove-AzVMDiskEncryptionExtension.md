---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177550"
---
# <span data-ttu-id="8b131-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8b131-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="8b131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b131-102">SYNOPSIS</span></span>
<span data-ttu-id="8b131-103">Rimuove l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b131-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="8b131-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b131-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b131-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b131-105">DESCRIPTION</span></span>
<span data-ttu-id="8b131-106">Il cmdlet **Remove-AzVMDiskEncryptionExtension** rimuove l'estensione di crittografia del disco e la configurazione dell'estensione associata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b131-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="8b131-107">Se non viene specificato alcun nome di estensione, questo cmdlet rimuove l'estensione con nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o AzureDiskEncryptionForLinux per le macchine virtuali basate su Linux.</span><span class="sxs-lookup"><span data-stu-id="8b131-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="8b131-108">Questo cmdlet non riesce se la crittografia nella macchina virtuale non è stata prima disabilitata.</span><span class="sxs-lookup"><span data-stu-id="8b131-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="8b131-109">Per disabilitare la crittografia in una macchina virtuale, usare [Disable-AzVMDiskEncryption.](./Disable-AzVMDiskEncryption.md)</span><span class="sxs-lookup"><span data-stu-id="8b131-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="8b131-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b131-110">EXAMPLES</span></span>

### <span data-ttu-id="8b131-111">Esempio 1: Rimuovere l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b131-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="8b131-112">Questo comando rimuove l'estensione con il nome predefinito AzureDiskEncryption per una macchina virtuale che esegue il sistema operativo Windows o AzureDiskEncryptionForLinux per macchina virtuale basata su Linux denominata MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="8b131-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="8b131-113">Esempio 2: Rimuovere una specifica estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b131-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="8b131-114">Questo comando rimuove l'estensione di crittografia denominata MyDiskEncryptionExtension dalla macchina virtuale myTestVM.</span><span class="sxs-lookup"><span data-stu-id="8b131-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="8b131-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b131-115">PARAMETERS</span></span>

### <span data-ttu-id="8b131-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b131-116">-DefaultProfile</span></span>
<span data-ttu-id="8b131-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b131-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b131-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8b131-118">-Force</span></span>
<span data-ttu-id="8b131-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="8b131-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b131-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8b131-120">-Name</span></span>
<span data-ttu-id="8b131-121">Specifica il nome della risorsa Gestione risorse di Azure che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="8b131-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="8b131-122">Il cmdlet Set-AzVMDiskEncryptionExtension imposta questo nome su AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows e le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="8b131-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="8b131-123">Specificare questo parametro solo se è stato modificato il nome predefinito nel cmdlet **Set-AzVMDiskEncryptionExtension** o se è stato usato un nome di risorsa diverso in un modello di Gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="8b131-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b131-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8b131-124">-NoWait</span></span>
<span data-ttu-id="8b131-125">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8b131-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8b131-126">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="8b131-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8b131-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b131-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b131-128">Specifica il nome del gruppo di risorse per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b131-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="8b131-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b131-129">-VMName</span></span>
<span data-ttu-id="8b131-130">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8b131-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8b131-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b131-131">-Confirm</span></span>
<span data-ttu-id="8b131-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b131-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b131-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b131-133">-WhatIf</span></span>
<span data-ttu-id="8b131-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b131-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b131-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b131-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b131-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b131-136">CommonParameters</span></span>
<span data-ttu-id="8b131-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b131-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b131-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b131-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b131-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b131-139">INPUTS</span></span>

### <span data-ttu-id="8b131-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8b131-140">System.String</span></span>

## <span data-ttu-id="8b131-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b131-141">OUTPUTS</span></span>

### <span data-ttu-id="8b131-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8b131-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8b131-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b131-143">NOTES</span></span>

## <span data-ttu-id="8b131-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b131-144">RELATED LINKS</span></span>

[<span data-ttu-id="8b131-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="8b131-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="8b131-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8b131-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


