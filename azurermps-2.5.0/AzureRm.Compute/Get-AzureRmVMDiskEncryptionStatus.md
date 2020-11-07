---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
ms.openlocfilehash: 667ebae58974b2dc68d19daa6a4f3a9d2e98075d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865853"
---
# <span data-ttu-id="75854-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="75854-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="75854-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75854-102">SYNOPSIS</span></span>
<span data-ttu-id="75854-103">Ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75854-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75854-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75854-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75854-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75854-105">DESCRIPTION</span></span>
<span data-ttu-id="75854-106">Il cmdlet **Get-AzureRmVMDiskEncryptionStatus** ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75854-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="75854-107">Visualizza lo stato di crittografia del sistema operativo e dei volumi di dati.</span><span class="sxs-lookup"><span data-stu-id="75854-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="75854-108">Oltre allo stato di crittografia, viene visualizzato anche l'URL segreto di crittografia, l'URL della chiave di crittografia chiave, gli ID delle risorse dei **Vault** , in cui sono presenti la chiave di crittografia e la chiave di crittografia per il volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="75854-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="75854-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75854-109">EXAMPLES</span></span>

### <span data-ttu-id="75854-110">Esempio 1: ottenere lo stato di crittografia di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="75854-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="75854-111">Questo comando ottiene lo stato di crittografia della macchina virtuale denominata VM001.</span><span class="sxs-lookup"><span data-stu-id="75854-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="75854-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75854-112">PARAMETERS</span></span>

### <span data-ttu-id="75854-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75854-113">-DefaultProfile</span></span>
<span data-ttu-id="75854-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75854-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75854-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="75854-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="75854-116">Nome dell'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="75854-116">The extension publisher name.</span></span> <span data-ttu-id="75854-117">Specifica questo parametro solo per eseguire l'override del valore predefinito "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="75854-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75854-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="75854-118">-ExtensionType</span></span>
<span data-ttu-id="75854-119">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="75854-119">The extension type.</span></span> <span data-ttu-id="75854-120">Specifica questo parametro per eseguire l'override del valore predefinito "AzureDiskEncryption" per le VM di Windows e "AzureDiskEncryptionForLinux" per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="75854-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75854-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="75854-121">-Name</span></span>
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

### <span data-ttu-id="75854-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75854-122">-ResourceGroupName</span></span>
<span data-ttu-id="75854-123">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75854-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="75854-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="75854-124">-VMName</span></span>
<span data-ttu-id="75854-125">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="75854-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="75854-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75854-126">CommonParameters</span></span>
<span data-ttu-id="75854-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75854-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75854-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75854-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75854-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75854-129">INPUTS</span></span>

### <span data-ttu-id="75854-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="75854-130">None</span></span>
<span data-ttu-id="75854-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="75854-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75854-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75854-132">OUTPUTS</span></span>

### <span data-ttu-id="75854-133">Microsoft. Azure. Commands. Compute. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="75854-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="75854-134">Note</span><span class="sxs-lookup"><span data-stu-id="75854-134">NOTES</span></span>

## <span data-ttu-id="75854-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75854-135">RELATED LINKS</span></span>

[<span data-ttu-id="75854-136">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="75854-136">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="75854-137">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="75854-137">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


