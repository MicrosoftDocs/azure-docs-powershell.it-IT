---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Disable-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 8cb68b45637496cb87e387c6755fe861fe3e21f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521759"
---
# <span data-ttu-id="7d26d-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7d26d-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="7d26d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d26d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d26d-103">Disabilita la crittografia del disco in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="7d26d-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d26d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d26d-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d26d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d26d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d26d-106">Disabilita la crittografia del disco in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="7d26d-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="7d26d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d26d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d26d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d26d-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7d26d-109">Disabilita la crittografia del disco nel set di scale VM denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="7d26d-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="7d26d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d26d-110">PARAMETERS</span></span>

### <span data-ttu-id="7d26d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d26d-111">-DefaultProfile</span></span>
<span data-ttu-id="7d26d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d26d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d26d-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="7d26d-113">-ExtensionName</span></span>
<span data-ttu-id="7d26d-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7d26d-114">The extension name.</span></span>
<span data-ttu-id="7d26d-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM di Windows e AzureDiskEncryptionForLinux per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="7d26d-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="7d26d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7d26d-116">-Force</span></span>
<span data-ttu-id="7d26d-117">Per forzare la rimozione dell'estensione dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d26d-117">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="7d26d-118">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="7d26d-118">-ForceUpdate</span></span>
<span data-ttu-id="7d26d-119">Genera un contrassegno per Force Update.</span><span class="sxs-lookup"><span data-stu-id="7d26d-119">Generate a tag for force update.</span></span>  <span data-ttu-id="7d26d-120">Questa operazione deve essere concessa per eseguire ripetute operazioni di crittografia nella stessa VM.</span><span class="sxs-lookup"><span data-stu-id="7d26d-120">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="7d26d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d26d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d26d-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d26d-122">The resource group name.</span></span>

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

### <span data-ttu-id="7d26d-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7d26d-123">-VMScaleSetName</span></span>
<span data-ttu-id="7d26d-124">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7d26d-124">The virtual machine name.</span></span>

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

### <span data-ttu-id="7d26d-125">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="7d26d-125">-VolumeType</span></span>
<span data-ttu-id="7d26d-126">Tipo di volume (OS o dati) per eseguire l'operazione di crittografia</span><span class="sxs-lookup"><span data-stu-id="7d26d-126">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="7d26d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d26d-127">-Confirm</span></span>
<span data-ttu-id="7d26d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d26d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d26d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d26d-129">-WhatIf</span></span>
<span data-ttu-id="7d26d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d26d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d26d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d26d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d26d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d26d-132">CommonParameters</span></span>
<span data-ttu-id="7d26d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d26d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d26d-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d26d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d26d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d26d-135">INPUTS</span></span>

### <span data-ttu-id="7d26d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7d26d-136">System.String</span></span>

## <span data-ttu-id="7d26d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d26d-137">OUTPUTS</span></span>

### <span data-ttu-id="7d26d-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7d26d-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7d26d-139">Note</span><span class="sxs-lookup"><span data-stu-id="7d26d-139">NOTES</span></span>

## <span data-ttu-id="7d26d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d26d-140">RELATED LINKS</span></span>

