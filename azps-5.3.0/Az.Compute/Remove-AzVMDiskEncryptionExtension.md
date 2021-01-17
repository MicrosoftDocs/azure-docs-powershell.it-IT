---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488280"
---
# <span data-ttu-id="1b2fc-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1b2fc-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="1b2fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2fc-103">Rimuove l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="1b2fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b2fc-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b2fc-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2fc-106">Il cmdlet **Remove-AzVMDiskEncryptionExtension** rimuove l'estensione di crittografia del disco e la configurazione dell'estensione associata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="1b2fc-107">Se non viene specificato alcun nome di estensione, questo cmdlet rimuove l'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o AzureDiskEncryptionForLinux per macchine virtuali basate su Linux.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="1b2fc-108">Questo cmdlet avrà esito negativo se la crittografia nella macchina virtuale non è stata prima disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="1b2fc-109">Per disabilitare la crittografia in una macchina virtuale, usare [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span><span class="sxs-lookup"><span data-stu-id="1b2fc-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="1b2fc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b2fc-110">EXAMPLES</span></span>

### <span data-ttu-id="1b2fc-111">Esempio 1: rimuovere l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="1b2fc-112">Questo comando rimuove l'estensione con il nome predefinito AzureDiskEncryption per una macchina virtuale che esegue il sistema operativo Windows o AzureDiskEncryptionForLinux per la macchina virtuale basata su Linux denominata MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="1b2fc-113">Esempio 2: rimuovere un'estensione di crittografia disco specifica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="1b2fc-114">Questo comando rimuove l'estensione di crittografia denominata MyDiskEncryptionExtension dalla macchina virtuale denominata MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="1b2fc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b2fc-115">PARAMETERS</span></span>

### <span data-ttu-id="1b2fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2fc-116">-DefaultProfile</span></span>
<span data-ttu-id="1b2fc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2fc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1b2fc-118">-Force</span></span>
<span data-ttu-id="1b2fc-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b2fc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b2fc-120">-Name</span></span>
<span data-ttu-id="1b2fc-121">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1b2fc-122">Il cmdlet Set-AzVMDiskEncryptionExtension imposta questo nome su AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows e le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="1b2fc-123">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzVMDiskEncryptionExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="1b2fc-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="1b2fc-124">-NoWait</span></span>
<span data-ttu-id="1b2fc-125">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1b2fc-126">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1b2fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="1b2fc-128">Specifica il nome del gruppo di risorse per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="1b2fc-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b2fc-129">-VMName</span></span>
<span data-ttu-id="1b2fc-130">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1b2fc-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b2fc-131">-Confirm</span></span>
<span data-ttu-id="1b2fc-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b2fc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2fc-133">-WhatIf</span></span>
<span data-ttu-id="1b2fc-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2fc-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b2fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2fc-136">CommonParameters</span></span>
<span data-ttu-id="1b2fc-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2fc-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b2fc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2fc-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b2fc-139">INPUTS</span></span>

### <span data-ttu-id="1b2fc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1b2fc-140">System.String</span></span>

## <span data-ttu-id="1b2fc-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b2fc-141">OUTPUTS</span></span>

### <span data-ttu-id="1b2fc-142">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1b2fc-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1b2fc-143">Note</span><span class="sxs-lookup"><span data-stu-id="1b2fc-143">NOTES</span></span>

## <span data-ttu-id="1b2fc-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b2fc-144">RELATED LINKS</span></span>

[<span data-ttu-id="1b2fc-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1b2fc-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="1b2fc-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1b2fc-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


