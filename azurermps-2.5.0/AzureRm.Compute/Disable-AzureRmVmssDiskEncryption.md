---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: b130be059432a6ca21fb0c1669660ebed34c670e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866767"
---
# <span data-ttu-id="4f1db-101">Disable-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4f1db-101">Disable-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="4f1db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f1db-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1db-103">Disabilita la crittografia del disco in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="4f1db-103">Disables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f1db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f1db-104">SYNTAX</span></span>

```
Disable-AzureRmVmssDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-ExtensionName] <String>] [-VolumeType <String>] [-ForceUpdate] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1db-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f1db-105">DESCRIPTION</span></span>
<span data-ttu-id="4f1db-106">Disabilita la crittografia del disco in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="4f1db-106">Disables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="4f1db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f1db-107">EXAMPLES</span></span>

### <span data-ttu-id="4f1db-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f1db-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4f1db-109">Disabilita la crittografia del disco nel set di scale VM denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="4f1db-109">Disables disk encryption on the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4f1db-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f1db-110">PARAMETERS</span></span>

### <span data-ttu-id="4f1db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f1db-111">-AsJob</span></span>
<span data-ttu-id="4f1db-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4f1db-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f1db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1db-113">-DefaultProfile</span></span>
<span data-ttu-id="4f1db-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f1db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f1db-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4f1db-115">-ExtensionName</span></span>
<span data-ttu-id="4f1db-116">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="4f1db-116">The extension name.</span></span>
<span data-ttu-id="4f1db-117">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM di Windows e AzureDiskEncryptionForLinux per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="4f1db-117">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="4f1db-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4f1db-118">-Force</span></span>
<span data-ttu-id="4f1db-119">Per forzare la rimozione dell'estensione dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4f1db-119">To force the removal of the extension from the virtual machine.</span></span>

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

### <span data-ttu-id="4f1db-120">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="4f1db-120">-ForceUpdate</span></span>
<span data-ttu-id="4f1db-121">Genera un contrassegno per Force Update.</span><span class="sxs-lookup"><span data-stu-id="4f1db-121">Generate a tag for force update.</span></span>  <span data-ttu-id="4f1db-122">Questa operazione deve essere concessa per eseguire ripetute operazioni di crittografia nella stessa VM.</span><span class="sxs-lookup"><span data-stu-id="4f1db-122">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f1db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f1db-123">-ResourceGroupName</span></span>
<span data-ttu-id="4f1db-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4f1db-124">The resource group name.</span></span>

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

### <span data-ttu-id="4f1db-125">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4f1db-125">-VMScaleSetName</span></span>
<span data-ttu-id="4f1db-126">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4f1db-126">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f1db-127">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="4f1db-127">-VolumeType</span></span>
<span data-ttu-id="4f1db-128">Tipo di volume (OS o dati) per eseguire l'operazione di crittografia</span><span class="sxs-lookup"><span data-stu-id="4f1db-128">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f1db-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f1db-129">-Confirm</span></span>
<span data-ttu-id="4f1db-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f1db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f1db-131">-WhatIf</span></span>
<span data-ttu-id="4f1db-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f1db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f1db-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f1db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1db-134">CommonParameters</span></span>
<span data-ttu-id="4f1db-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1db-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f1db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1db-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f1db-137">INPUTS</span></span>

### <span data-ttu-id="4f1db-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4f1db-138">System.String</span></span>

## <span data-ttu-id="4f1db-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f1db-139">OUTPUTS</span></span>

### <span data-ttu-id="4f1db-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4f1db-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4f1db-141">Note</span><span class="sxs-lookup"><span data-stu-id="4f1db-141">NOTES</span></span>

## <span data-ttu-id="4f1db-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f1db-142">RELATED LINKS</span></span>

