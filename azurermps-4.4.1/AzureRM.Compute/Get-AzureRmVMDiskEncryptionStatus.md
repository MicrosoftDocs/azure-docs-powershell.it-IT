---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 0d7312d7ecbddf15530438e9729e470bd202e488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686862"
---
# <span data-ttu-id="ac8ff-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="ac8ff-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="ac8ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac8ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8ff-103">Ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac8ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac8ff-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac8ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac8ff-105">DESCRIPTION</span></span>
<span data-ttu-id="ac8ff-106">Il cmdlet **Get-AzureRmVMDiskEncryptionStatus** ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="ac8ff-107">Visualizza lo stato di crittografia del sistema operativo e dei volumi di dati.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="ac8ff-108">Oltre allo stato di crittografia, viene visualizzato anche l'URL segreto di crittografia, l'URL della chiave di crittografia chiave, gli ID delle risorse dei **Vault** , in cui sono presenti la chiave di crittografia e la chiave di crittografia per il volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="ac8ff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac8ff-109">EXAMPLES</span></span>

### <span data-ttu-id="ac8ff-110">Esempio 1: ottenere lo stato di crittografia di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ac8ff-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="ac8ff-111">Questo comando ottiene lo stato di crittografia della macchina virtuale denominata VM001.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="ac8ff-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac8ff-112">PARAMETERS</span></span>

### <span data-ttu-id="ac8ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8ff-113">-DefaultProfile</span></span>
<span data-ttu-id="ac8ff-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac8ff-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac8ff-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ff-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac8ff-116">-ResourceGroupName</span></span>
<span data-ttu-id="ac8ff-117">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ac8ff-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="ac8ff-118">-VMName</span></span>
<span data-ttu-id="ac8ff-119">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8ff-120">CommonParameters</span></span>
<span data-ttu-id="ac8ff-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8ff-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac8ff-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8ff-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac8ff-123">INPUTS</span></span>

## <span data-ttu-id="ac8ff-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac8ff-124">OUTPUTS</span></span>

## <span data-ttu-id="ac8ff-125">Note</span><span class="sxs-lookup"><span data-stu-id="ac8ff-125">NOTES</span></span>

## <span data-ttu-id="ac8ff-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac8ff-126">RELATED LINKS</span></span>

[<span data-ttu-id="ac8ff-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ac8ff-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="ac8ff-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ac8ff-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


