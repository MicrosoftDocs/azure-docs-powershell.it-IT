---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515792"
---
# <span data-ttu-id="3ad7f-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="3ad7f-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="3ad7f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ad7f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad7f-103">Ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ad7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ad7f-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ad7f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ad7f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad7f-106">Il cmdlet **Get-AzureRmVMDiskEncryptionStatus** ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="3ad7f-107">Visualizza lo stato di crittografia del sistema operativo e dei volumi di dati.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="3ad7f-108">Oltre allo stato di crittografia, viene visualizzato anche l'URL segreto di crittografia, l'URL della chiave di crittografia chiave, gli ID delle risorse dei **Vault** , in cui sono presenti la chiave di crittografia e la chiave di crittografia per il volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="3ad7f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ad7f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ad7f-110">Esempio 1: ottenere lo stato di crittografia di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3ad7f-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="3ad7f-111">Questo comando ottiene lo stato di crittografia della macchina virtuale denominata VM001.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="3ad7f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ad7f-112">PARAMETERS</span></span>

### <span data-ttu-id="3ad7f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ad7f-113">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad7f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad7f-114">-ResourceGroupName</span></span>
<span data-ttu-id="3ad7f-115">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3ad7f-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="3ad7f-116">-VMName</span></span>
<span data-ttu-id="3ad7f-117">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad7f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad7f-118">CommonParameters</span></span>
<span data-ttu-id="3ad7f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad7f-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad7f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad7f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ad7f-121">INPUTS</span></span>

### <span data-ttu-id="3ad7f-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ad7f-122">None</span></span>
<span data-ttu-id="3ad7f-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ad7f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ad7f-124">OUTPUTS</span></span>

## <span data-ttu-id="3ad7f-125">Note</span><span class="sxs-lookup"><span data-stu-id="3ad7f-125">NOTES</span></span>

## <span data-ttu-id="3ad7f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ad7f-126">RELATED LINKS</span></span>

[<span data-ttu-id="3ad7f-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3ad7f-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="3ad7f-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3ad7f-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


