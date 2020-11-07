---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: b208d7c0e0db028f1b3242a70be508fbbc3788ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686923"
---
# <span data-ttu-id="4a4c9-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="4a4c9-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="4a4c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4c9-103">Ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a4c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a4c9-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a4c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a4c9-105">DESCRIPTION</span></span>
<span data-ttu-id="4a4c9-106">Il cmdlet **Get-AzureRmVMDiskEncryptionStatus** ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="4a4c9-107">Visualizza lo stato di crittografia del sistema operativo e dei volumi di dati.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="4a4c9-108">Oltre allo stato di crittografia, viene visualizzato anche l'URL segreto di crittografia, l'URL della chiave di crittografia chiave, gli ID delle risorse dei **Vault** , in cui sono presenti la chiave di crittografia e la chiave di crittografia per il volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="4a4c9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a4c9-109">EXAMPLES</span></span>

### <span data-ttu-id="4a4c9-110">Esempio 1: ottenere lo stato di crittografia di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="4a4c9-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="4a4c9-111">Questo comando ottiene lo stato di crittografia della macchina virtuale denominata VM001.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="4a4c9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a4c9-112">PARAMETERS</span></span>

### <span data-ttu-id="4a4c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4c9-113">-DefaultProfile</span></span>
<span data-ttu-id="4a4c9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a4c9-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="4a4c9-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="4a4c9-116">Nome dell'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-116">The extension publisher name.</span></span> <span data-ttu-id="4a4c9-117">Specifica questo parametro solo per eseguire l'override del valore predefinito "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="4a4c9-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="4a4c9-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="4a4c9-118">-ExtensionType</span></span>
<span data-ttu-id="4a4c9-119">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-119">The extension type.</span></span> <span data-ttu-id="4a4c9-120">Specifica questo parametro per eseguire l'override del valore predefinito "AzureDiskEncryption" per le VM di Windows e "AzureDiskEncryptionForLinux" per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="4a4c9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a4c9-121">-Name</span></span>
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

### <span data-ttu-id="4a4c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a4c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a4c9-123">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4a4c9-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="4a4c9-124">-VMName</span></span>
<span data-ttu-id="4a4c9-125">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="4a4c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4c9-126">CommonParameters</span></span>
<span data-ttu-id="4a4c9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4c9-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a4c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4c9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a4c9-129">INPUTS</span></span>

### <span data-ttu-id="4a4c9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a4c9-130">System.String</span></span>

## <span data-ttu-id="4a4c9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a4c9-131">OUTPUTS</span></span>

### <span data-ttu-id="4a4c9-132">Microsoft. Azure. Commands. Compute. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="4a4c9-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="4a4c9-133">Note</span><span class="sxs-lookup"><span data-stu-id="4a4c9-133">NOTES</span></span>

## <span data-ttu-id="4a4c9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a4c9-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a4c9-135">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4a4c9-135">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="4a4c9-136">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4a4c9-136">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


