---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 56fcbadbcdbd874df3fea74918381eb24b2fa1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980909"
---
# <span data-ttu-id="7ba41-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7ba41-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="7ba41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba41-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba41-103">Mostra lo stato di crittografia del disco di un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ba41-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="7ba41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ba41-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ba41-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7ba41-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba41-106">Mostra lo stato di crittografia del disco di un set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ba41-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="7ba41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ba41-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba41-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7ba41-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7ba41-109">Mostra lo stato di crittografia del disco del set di scale della macchina virtuale denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="7ba41-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="7ba41-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ba41-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba41-111">-DefaultProfile</span></span>
<span data-ttu-id="7ba41-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba41-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ba41-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="7ba41-113">-ExtensionName</span></span>
<span data-ttu-id="7ba41-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="7ba41-114">The extension name.</span></span>
<span data-ttu-id="7ba41-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per le macchine virtuali Windows e AzureDiskEncryptionForLinux per le macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="7ba41-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="7ba41-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba41-116">-ResourceGroupName</span></span>
<span data-ttu-id="7ba41-117">Nome del gruppo di risorse del set di scalabilità della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7ba41-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="7ba41-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7ba41-118">-VMScaleSetName</span></span>
<span data-ttu-id="7ba41-119">Nome del set di scalabilità della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ba41-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="7ba41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba41-120">CommonParameters</span></span>
<span data-ttu-id="7ba41-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba41-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ba41-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba41-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="7ba41-123">INPUTS</span></span>

### <span data-ttu-id="7ba41-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7ba41-124">System.String</span></span>

## <span data-ttu-id="7ba41-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ba41-125">OUTPUTS</span></span>

### <span data-ttu-id="7ba41-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="7ba41-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="7ba41-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="7ba41-127">NOTES</span></span>

## <span data-ttu-id="7ba41-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ba41-128">RELATED LINKS</span></span>
