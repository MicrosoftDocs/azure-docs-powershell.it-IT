---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
ms.openlocfilehash: 551e5928ca4628b9964132ee117cbf65fdbaedba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507599"
---
# <span data-ttu-id="18062-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="18062-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="18062-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18062-102">SYNOPSIS</span></span>
<span data-ttu-id="18062-103">Mostra lo stato di crittografia del disco delle VM in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="18062-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18062-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18062-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18062-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18062-105">DESCRIPTION</span></span>
<span data-ttu-id="18062-106">Mostra lo stato di crittografia del disco del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="18062-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="18062-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18062-107">EXAMPLES</span></span>

### <span data-ttu-id="18062-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18062-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="18062-109">Mostra lo stato di crittografia del disco dell'istanza VM 1 nel set di proporzioni VM denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="18062-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="18062-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18062-110">PARAMETERS</span></span>

### <span data-ttu-id="18062-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18062-111">-DefaultProfile</span></span>
<span data-ttu-id="18062-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18062-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18062-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="18062-113">-ExtensionName</span></span>
<span data-ttu-id="18062-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="18062-114">The extension name.</span></span>
<span data-ttu-id="18062-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM di Windows e AzureDiskEncryptionForLinux per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="18062-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="18062-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="18062-116">-InstanceId</span></span>
<span data-ttu-id="18062-117">Specifica l'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="18062-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="18062-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18062-118">-ResourceGroupName</span></span>
<span data-ttu-id="18062-119">Nome del gruppo di risorse del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18062-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="18062-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="18062-120">-VMScaleSetName</span></span>
<span data-ttu-id="18062-121">Nome del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="18062-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="18062-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18062-122">CommonParameters</span></span>
<span data-ttu-id="18062-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18062-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18062-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18062-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18062-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18062-125">INPUTS</span></span>

### <span data-ttu-id="18062-126">System. String</span><span class="sxs-lookup"><span data-stu-id="18062-126">System.String</span></span>

## <span data-ttu-id="18062-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18062-127">OUTPUTS</span></span>

### <span data-ttu-id="18062-128">Microsoft. Azure. Commands. Compute. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="18062-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="18062-129">Note</span><span class="sxs-lookup"><span data-stu-id="18062-129">NOTES</span></span>

## <span data-ttu-id="18062-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18062-130">RELATED LINKS</span></span>