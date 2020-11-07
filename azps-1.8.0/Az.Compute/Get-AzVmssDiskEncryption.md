---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5219b43a1d80515f0bce02c5f6fdd2117b736a00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684794"
---
# <span data-ttu-id="ddefa-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ddefa-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="ddefa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddefa-102">SYNOPSIS</span></span>
<span data-ttu-id="ddefa-103">Mostra lo stato di crittografia del disco di un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="ddefa-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="ddefa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddefa-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddefa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddefa-105">DESCRIPTION</span></span>
<span data-ttu-id="ddefa-106">Mostra lo stato di crittografia del disco di un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="ddefa-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="ddefa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddefa-107">EXAMPLES</span></span>

### <span data-ttu-id="ddefa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddefa-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ddefa-109">Mostra lo stato di crittografia del disco del set di proporzioni VM denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="ddefa-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="ddefa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddefa-110">PARAMETERS</span></span>

### <span data-ttu-id="ddefa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddefa-111">-DefaultProfile</span></span>
<span data-ttu-id="ddefa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddefa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddefa-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ddefa-113">-ExtensionName</span></span>
<span data-ttu-id="ddefa-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ddefa-114">The extension name.</span></span>
<span data-ttu-id="ddefa-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM di Windows e AzureDiskEncryptionForLinux per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="ddefa-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="ddefa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddefa-116">-ResourceGroupName</span></span>
<span data-ttu-id="ddefa-117">Nome del gruppo di risorse del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ddefa-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="ddefa-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddefa-118">-VMScaleSetName</span></span>
<span data-ttu-id="ddefa-119">Nome del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ddefa-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="ddefa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddefa-120">CommonParameters</span></span>
<span data-ttu-id="ddefa-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddefa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddefa-122">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddefa-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddefa-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddefa-123">INPUTS</span></span>

### <span data-ttu-id="ddefa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ddefa-124">System.String</span></span>

## <span data-ttu-id="ddefa-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddefa-125">OUTPUTS</span></span>

### <span data-ttu-id="ddefa-126">Microsoft. Azure. Commands. Compute. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="ddefa-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="ddefa-127">Note</span><span class="sxs-lookup"><span data-stu-id="ddefa-127">NOTES</span></span>

## <span data-ttu-id="ddefa-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddefa-128">RELATED LINKS</span></span>
