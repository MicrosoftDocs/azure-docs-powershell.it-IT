---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 51b1273e5c44756df56177878dbe4fbc9563ec2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863526"
---
# <span data-ttu-id="efe8e-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="efe8e-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="efe8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efe8e-102">SYNOPSIS</span></span>
<span data-ttu-id="efe8e-103">Rimuove l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="efe8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efe8e-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efe8e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efe8e-105">DESCRIPTION</span></span>
<span data-ttu-id="efe8e-106">Il cmdlet **Remove-AzVMDiskEncryptionExtension** rimuove l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="efe8e-107">Se non viene specificato alcun nome di estensione, questo cmdlet rimuove l'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o AzureDiskEncryptionForLinux per macchine virtuali basate su Linux.</span><span class="sxs-lookup"><span data-stu-id="efe8e-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="efe8e-108">Questo cmdlet non disabilita la crittografia nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="efe8e-109">Rimuove l'estensione e la configurazione dell'estensione associata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="efe8e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efe8e-110">EXAMPLES</span></span>

### <span data-ttu-id="efe8e-111">Esempio 1: rimuovere l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="efe8e-112">Questo comando rimuove l'estensione con il nome predefinito AzureDiskEncryption per una macchina virtuale che esegue il sistema operativo Windows o AzureDiskEncryptionForLinux per la macchina virtuale basata su Linux denominata MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="efe8e-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="efe8e-113">Esempio 2: rimuovere un'estensione di crittografia disco specifica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="efe8e-114">Questo comando rimuove l'estensione di crittografia denominata MyDiskEncryptionExtension dalla macchina virtuale denominata MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="efe8e-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="efe8e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efe8e-115">PARAMETERS</span></span>

### <span data-ttu-id="efe8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe8e-116">-DefaultProfile</span></span>
<span data-ttu-id="efe8e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efe8e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efe8e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="efe8e-118">-Force</span></span>
<span data-ttu-id="efe8e-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="efe8e-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe8e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="efe8e-120">-Name</span></span>
<span data-ttu-id="efe8e-121">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="efe8e-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="efe8e-122">Il cmdlet Set-AzVMDiskEncryptionExtension imposta questo nome su AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows e le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="efe8e-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="efe8e-123">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzVMDiskEncryptionExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="efe8e-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="efe8e-125">Specifica il nome del gruppo di risorse per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-125">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe8e-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="efe8e-126">-VMName</span></span>
<span data-ttu-id="efe8e-127">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe8e-127">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe8e-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efe8e-128">-Confirm</span></span>
<span data-ttu-id="efe8e-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efe8e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe8e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efe8e-130">-WhatIf</span></span>
<span data-ttu-id="efe8e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efe8e-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="efe8e-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efe8e-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efe8e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe8e-133">CommonParameters</span></span>
<span data-ttu-id="efe8e-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe8e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe8e-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe8e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe8e-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efe8e-136">INPUTS</span></span>

### <span data-ttu-id="efe8e-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="efe8e-137">None</span></span>
<span data-ttu-id="efe8e-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="efe8e-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efe8e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efe8e-139">OUTPUTS</span></span>

### <span data-ttu-id="efe8e-140">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="efe8e-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="efe8e-141">Note</span><span class="sxs-lookup"><span data-stu-id="efe8e-141">NOTES</span></span>

## <span data-ttu-id="efe8e-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efe8e-142">RELATED LINKS</span></span>

[<span data-ttu-id="efe8e-143">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="efe8e-143">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="efe8e-144">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="efe8e-144">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


