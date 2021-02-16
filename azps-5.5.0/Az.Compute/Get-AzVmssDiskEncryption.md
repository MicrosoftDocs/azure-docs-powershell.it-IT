---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204898"
---
# <span data-ttu-id="30213-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="30213-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="30213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30213-102">SYNOPSIS</span></span>
<span data-ttu-id="30213-103">Mostra lo stato di crittografia del disco di un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="30213-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="30213-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30213-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30213-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30213-105">DESCRIPTION</span></span>
<span data-ttu-id="30213-106">Mostra lo stato di crittografia del disco di un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="30213-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="30213-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30213-107">EXAMPLES</span></span>

### <span data-ttu-id="30213-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30213-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="30213-109">Mostra lo stato di crittografia del disco del set di scale della macchina virtuale denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="30213-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="30213-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30213-110">PARAMETERS</span></span>

### <span data-ttu-id="30213-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30213-111">-DefaultProfile</span></span>
<span data-ttu-id="30213-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30213-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30213-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="30213-113">-ExtensionName</span></span>
<span data-ttu-id="30213-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="30213-114">The extension name.</span></span>
<span data-ttu-id="30213-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per le macchine virtuali Windows e AzureDiskEncryptionForLinux per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="30213-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="30213-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30213-116">-ResourceGroupName</span></span>
<span data-ttu-id="30213-117">Nome del gruppo di risorse del set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="30213-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30213-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="30213-118">-VMScaleSetName</span></span>
<span data-ttu-id="30213-119">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="30213-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30213-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30213-120">CommonParameters</span></span>
<span data-ttu-id="30213-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30213-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30213-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30213-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30213-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="30213-123">INPUTS</span></span>

### <span data-ttu-id="30213-124">System.String</span><span class="sxs-lookup"><span data-stu-id="30213-124">System.String</span></span>

## <span data-ttu-id="30213-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30213-125">OUTPUTS</span></span>

### <span data-ttu-id="30213-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="30213-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="30213-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="30213-127">NOTES</span></span>

## <span data-ttu-id="30213-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30213-128">RELATED LINKS</span></span>
