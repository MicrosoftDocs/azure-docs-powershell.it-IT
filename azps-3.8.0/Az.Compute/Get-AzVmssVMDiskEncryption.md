---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018886"
---
# <span data-ttu-id="65b6e-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="65b6e-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="65b6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="65b6e-103">Mostra lo stato di crittografia del disco delle VM in un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="65b6e-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="65b6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65b6e-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65b6e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="65b6e-106">Mostra lo stato di crittografia del disco del set di scale VM.</span><span class="sxs-lookup"><span data-stu-id="65b6e-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="65b6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="65b6e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="65b6e-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="65b6e-109">Mostra lo stato di crittografia del disco dell'istanza VM 1 nel set di proporzioni VM denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="65b6e-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="65b6e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65b6e-110">PARAMETERS</span></span>

### <span data-ttu-id="65b6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b6e-111">-DefaultProfile</span></span>
<span data-ttu-id="65b6e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65b6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65b6e-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="65b6e-113">-ExtensionName</span></span>
<span data-ttu-id="65b6e-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="65b6e-114">The extension name.</span></span>
<span data-ttu-id="65b6e-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM di Windows e AzureDiskEncryptionForLinux per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="65b6e-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="65b6e-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="65b6e-116">-InstanceId</span></span>
<span data-ttu-id="65b6e-117">Specifica l'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="65b6e-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="65b6e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b6e-118">-ResourceGroupName</span></span>
<span data-ttu-id="65b6e-119">Nome del gruppo di risorse del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65b6e-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="65b6e-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="65b6e-120">-VMScaleSetName</span></span>
<span data-ttu-id="65b6e-121">Nome del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65b6e-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="65b6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b6e-122">CommonParameters</span></span>
<span data-ttu-id="65b6e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b6e-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65b6e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b6e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65b6e-125">INPUTS</span></span>

### <span data-ttu-id="65b6e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="65b6e-126">System.String</span></span>

## <span data-ttu-id="65b6e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65b6e-127">OUTPUTS</span></span>

### <span data-ttu-id="65b6e-128">Microsoft. Azure. Commands. Compute. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="65b6e-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="65b6e-129">Note</span><span class="sxs-lookup"><span data-stu-id="65b6e-129">NOTES</span></span>

## <span data-ttu-id="65b6e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65b6e-130">RELATED LINKS</span></span>
