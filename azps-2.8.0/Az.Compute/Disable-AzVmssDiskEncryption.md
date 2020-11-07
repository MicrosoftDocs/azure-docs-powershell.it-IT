---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVmssDiskEncryption.md
ms.openlocfilehash: 1b816e51d93ed375a8b281bba360a103380e9476
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675451"
---
# <span data-ttu-id="f7202-101">Disable-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f7202-101">Disable-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="f7202-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7202-102">SYNOPSIS</span></span>
<span data-ttu-id="f7202-103">Disabilita la crittografia del disco in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="f7202-103">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="f7202-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7202-104">SYNTAX</span></span>

```
Disable-AzVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7202-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7202-105">DESCRIPTION</span></span>
<span data-ttu-id="f7202-106">Disabilita la crittografia del disco in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="f7202-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="f7202-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7202-107">EXAMPLES</span></span>

### <span data-ttu-id="f7202-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7202-108">Example 1</span></span>
```
PS C:\> Disable-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f7202-109">Disabilita la crittografia del disco nel set di scale VM denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="f7202-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f7202-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7202-110">PARAMETERS</span></span>

### <span data-ttu-id="f7202-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7202-111">-AsJob</span></span>
<span data-ttu-id="f7202-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f7202-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7202-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7202-113">-DefaultProfile</span></span>
<span data-ttu-id="f7202-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7202-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7202-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f7202-115">-ExtensionName</span></span>
<span data-ttu-id="f7202-116">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f7202-116">The extension name.</span></span>
<span data-ttu-id="f7202-117">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM di Windows e AzureDiskEncryptionForLinux per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="f7202-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="f7202-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f7202-118">-Force</span></span>
<span data-ttu-id="f7202-119">Per forzare la rimozione dell'estensione dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7202-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="f7202-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="f7202-120">-ForceUpdate</span></span>
<span data-ttu-id="f7202-121">Genera un contrassegno per Force Update.</span><span class="sxs-lookup"><span data-stu-id="f7202-121">Generate a tag for force update.</span></span>  <span data-ttu-id="f7202-122">Questa operazione deve essere concessa per eseguire ripetute operazioni di crittografia nella stessa VM.</span><span class="sxs-lookup"><span data-stu-id="f7202-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="f7202-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7202-123">-ResourceGroupName</span></span>
<span data-ttu-id="f7202-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7202-124">The resource group name.</span></span>

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

### <span data-ttu-id="f7202-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f7202-125">-VMScaleSetName</span></span>
<span data-ttu-id="f7202-126">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7202-126">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7202-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="f7202-127">-VolumeType</span></span>
<span data-ttu-id="f7202-128">Tipo di volume (OS o dati) per eseguire l'operazione di crittografia</span><span class="sxs-lookup"><span data-stu-id="f7202-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7202-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7202-129">-Confirm</span></span>
<span data-ttu-id="f7202-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7202-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7202-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7202-131">-WhatIf</span></span>
<span data-ttu-id="f7202-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7202-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7202-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7202-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7202-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7202-134">CommonParameters</span></span>
<span data-ttu-id="f7202-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7202-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7202-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7202-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7202-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7202-137">INPUTS</span></span>

### <span data-ttu-id="f7202-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f7202-138">System.String</span></span>

### <span data-ttu-id="f7202-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7202-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7202-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7202-140">OUTPUTS</span></span>

### <span data-ttu-id="f7202-141">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f7202-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f7202-142">Note</span><span class="sxs-lookup"><span data-stu-id="f7202-142">NOTES</span></span>

## <span data-ttu-id="f7202-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7202-143">RELATED LINKS</span></span>
