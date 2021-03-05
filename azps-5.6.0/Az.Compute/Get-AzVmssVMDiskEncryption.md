---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: a697ead2f971191d108d4fb348a213e35b363d63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994487"
---
# <span data-ttu-id="c2956-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c2956-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="c2956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2956-102">SYNOPSIS</span></span>
<span data-ttu-id="c2956-103">Mostra lo stato di crittografia del disco delle macchine virtuali in un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2956-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="c2956-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2956-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2956-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c2956-105">DESCRIPTION</span></span>
<span data-ttu-id="c2956-106">Mostra lo stato di crittografia del disco del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2956-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="c2956-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2956-107">EXAMPLES</span></span>

### <span data-ttu-id="c2956-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2956-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="c2956-109">Mostra lo stato di crittografia del disco dell'istanza della macchina virtuale 1 nel set di scala della macchina virtuale denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="c2956-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c2956-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2956-110">PARAMETERS</span></span>

### <span data-ttu-id="c2956-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2956-111">-DefaultProfile</span></span>
<span data-ttu-id="c2956-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2956-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2956-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c2956-113">-ExtensionName</span></span>
<span data-ttu-id="c2956-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="c2956-114">The extension name.</span></span>
<span data-ttu-id="c2956-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per le macchine virtuali Windows e AzureDiskEncryptionForLinux per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="c2956-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="c2956-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c2956-116">-InstanceId</span></span>
<span data-ttu-id="c2956-117">Specifica l'ID istanza.</span><span class="sxs-lookup"><span data-stu-id="c2956-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="c2956-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2956-118">-ResourceGroupName</span></span>
<span data-ttu-id="c2956-119">Nome del gruppo di risorse del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2956-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c2956-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c2956-120">-VMScaleSetName</span></span>
<span data-ttu-id="c2956-121">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c2956-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="c2956-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2956-122">CommonParameters</span></span>
<span data-ttu-id="c2956-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2956-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2956-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2956-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2956-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="c2956-125">INPUTS</span></span>

### <span data-ttu-id="c2956-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c2956-126">System.String</span></span>

## <span data-ttu-id="c2956-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2956-127">OUTPUTS</span></span>

### <span data-ttu-id="c2956-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="c2956-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="c2956-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="c2956-129">NOTES</span></span>

## <span data-ttu-id="c2956-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2956-130">RELATED LINKS</span></span>
