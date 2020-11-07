---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: c49fc472c6cc3693145487bdfe7488d0eabfe237
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866371"
---
# <span data-ttu-id="fd3d1-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fd3d1-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="fd3d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fd3d1-103">Mostra lo stato di crittografia del disco di un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd3d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd3d1-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd3d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd3d1-105">DESCRIPTION</span></span>
<span data-ttu-id="fd3d1-106">Mostra lo stato di crittografia del disco di un set di proporzioni VM.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="fd3d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd3d1-107">EXAMPLES</span></span>

### <span data-ttu-id="fd3d1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd3d1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fd3d1-109">Mostra lo stato di crittografia del disco del set di proporzioni VM denominato VMSS001 che appartiene al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="fd3d1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd3d1-110">PARAMETERS</span></span>

### <span data-ttu-id="fd3d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd3d1-111">-DefaultProfile</span></span>
<span data-ttu-id="fd3d1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd3d1-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="fd3d1-113">-ExtensionName</span></span>
<span data-ttu-id="fd3d1-114">Nome dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-114">The extension name.</span></span>
<span data-ttu-id="fd3d1-115">Se questo parametro non è specificato, i valori predefiniti usati sono AzureDiskEncryption per VM di Windows e AzureDiskEncryptionForLinux per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="fd3d1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd3d1-116">-ResourceGroupName</span></span>
<span data-ttu-id="fd3d1-117">Nome del gruppo di risorse del set di scale della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="fd3d1-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3d1-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fd3d1-118">-VMScaleSetName</span></span>
<span data-ttu-id="fd3d1-119">Nome del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-119">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd3d1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd3d1-120">CommonParameters</span></span>
<span data-ttu-id="fd3d1-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd3d1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd3d1-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd3d1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd3d1-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd3d1-123">INPUTS</span></span>

### <span data-ttu-id="fd3d1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fd3d1-124">System.String</span></span>

## <span data-ttu-id="fd3d1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd3d1-125">OUTPUTS</span></span>

### <span data-ttu-id="fd3d1-126">Microsoft. Azure. Commands. Compute. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="fd3d1-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="fd3d1-127">Note</span><span class="sxs-lookup"><span data-stu-id="fd3d1-127">NOTES</span></span>

## <span data-ttu-id="fd3d1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd3d1-128">RELATED LINKS</span></span>

