---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 6c580b862ed2c8a420e8f203131ff9d18d187443
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866560"
---
# <span data-ttu-id="0b458-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0b458-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="0b458-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b458-102">SYNOPSIS</span></span>
<span data-ttu-id="0b458-103">Rimuove l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b458-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b458-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b458-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b458-105">DESCRIPTION</span></span>
<span data-ttu-id="0b458-106">Il cmdlet **Remove-AzureRmVMDiskEncryptionExtension** rimuove l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="0b458-107">Se non viene specificato alcun nome di estensione, questo cmdlet rimuove l'estensione con il nome predefinito AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows o AzureDiskEncryptionForLinux per macchine virtuali basate su Linux.</span><span class="sxs-lookup"><span data-stu-id="0b458-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="0b458-108">Questo cmdlet non disabilita la crittografia nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="0b458-109">Rimuove l'estensione e la configurazione dell'estensione associata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="0b458-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b458-110">EXAMPLES</span></span>

### <span data-ttu-id="0b458-111">Esempio 1: rimuovere l'estensione di crittografia disco da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="0b458-112">Questo comando rimuove l'estensione con il nome predefinito AzureDiskEncryption per una macchina virtuale che esegue il sistema operativo Windows o AzureDiskEncryptionForLinux per la macchina virtuale basata su Linux denominata MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="0b458-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="0b458-113">Esempio 2: rimuovere un'estensione di crittografia disco specifica da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="0b458-114">Questo comando rimuove l'estensione di crittografia denominata MyDiskEncryptionExtension dalla macchina virtuale denominata MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="0b458-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="0b458-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b458-115">PARAMETERS</span></span>

### <span data-ttu-id="0b458-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b458-116">-DefaultProfile</span></span>
<span data-ttu-id="0b458-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b458-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b458-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0b458-118">-Force</span></span>
<span data-ttu-id="0b458-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0b458-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b458-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b458-120">-Name</span></span>
<span data-ttu-id="0b458-121">Specifica il nome della risorsa di Azure Resource Manager che rappresenta l'estensione.</span><span class="sxs-lookup"><span data-stu-id="0b458-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="0b458-122">Il cmdlet Set-AzureRmVMDiskEncryptionExtension imposta questo nome su AzureDiskEncryption per le macchine virtuali che eseguono il sistema operativo Windows e le macchine virtuali AzureDiskEncryptionForLinux per Linux.</span><span class="sxs-lookup"><span data-stu-id="0b458-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="0b458-123">Specifica questo parametro solo se il nome predefinito è stato modificato nel cmdlet **set-AzureRmVMDiskEncryptionExtension** o si usa un nome di risorsa diverso in un modello di gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="0b458-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="0b458-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b458-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b458-125">Specifica il nome del gruppo di risorse per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-125">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="0b458-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="0b458-126">-VMName</span></span>
<span data-ttu-id="0b458-127">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b458-127">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0b458-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b458-128">-Confirm</span></span>
<span data-ttu-id="0b458-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b458-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b458-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b458-130">-WhatIf</span></span>
<span data-ttu-id="0b458-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b458-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0b458-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b458-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b458-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b458-133">CommonParameters</span></span>
<span data-ttu-id="0b458-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b458-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b458-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b458-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b458-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b458-136">INPUTS</span></span>

### <span data-ttu-id="0b458-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0b458-137">None</span></span>
<span data-ttu-id="0b458-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0b458-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b458-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b458-139">OUTPUTS</span></span>

### <span data-ttu-id="0b458-140">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b458-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0b458-141">Note</span><span class="sxs-lookup"><span data-stu-id="0b458-141">NOTES</span></span>

## <span data-ttu-id="0b458-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b458-142">RELATED LINKS</span></span>

[<span data-ttu-id="0b458-143">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0b458-143">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="0b458-144">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0b458-144">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


