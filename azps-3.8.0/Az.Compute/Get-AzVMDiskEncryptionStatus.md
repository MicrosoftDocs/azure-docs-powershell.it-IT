---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94023008"
---
# <span data-ttu-id="c610b-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="c610b-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="c610b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c610b-102">SYNOPSIS</span></span>
<span data-ttu-id="c610b-103">Ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c610b-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="c610b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c610b-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c610b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c610b-105">DESCRIPTION</span></span>
<span data-ttu-id="c610b-106">Il cmdlet **Get-AzVMDiskEncryptionStatus** ottiene lo stato di crittografia della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c610b-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="c610b-107">Visualizza lo stato di crittografia del sistema operativo e dei volumi di dati.</span><span class="sxs-lookup"><span data-stu-id="c610b-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="c610b-108">Oltre allo stato di crittografia, viene visualizzato anche l'URL segreto di crittografia, l'URL della chiave di crittografia chiave, gli ID delle risorse dei **Vault** , in cui sono presenti la chiave di crittografia e la chiave di crittografia per il volume del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c610b-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="c610b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c610b-109">EXAMPLES</span></span>

### <span data-ttu-id="c610b-110">Esempio 1: ottenere lo stato di crittografia di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c610b-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="c610b-111">Questo comando ottiene lo stato di crittografia della macchina virtuale denominata VM001.</span><span class="sxs-lookup"><span data-stu-id="c610b-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="c610b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c610b-112">PARAMETERS</span></span>

### <span data-ttu-id="c610b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c610b-113">-DefaultProfile</span></span>
<span data-ttu-id="c610b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c610b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c610b-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="c610b-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="c610b-116">Nome dell'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="c610b-116">The extension publisher name.</span></span> <span data-ttu-id="c610b-117">Specifica questo parametro solo per eseguire l'override del valore predefinito "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="c610b-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="c610b-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="c610b-118">-ExtensionType</span></span>
<span data-ttu-id="c610b-119">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="c610b-119">The extension type.</span></span> <span data-ttu-id="c610b-120">Specifica questo parametro per eseguire l'override del valore predefinito "AzureDiskEncryption" per le VM di Windows e "AzureDiskEncryptionForLinux" per le VM di Linux.</span><span class="sxs-lookup"><span data-stu-id="c610b-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="c610b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c610b-121">-Name</span></span>
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

### <span data-ttu-id="c610b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c610b-122">-ResourceGroupName</span></span>
<span data-ttu-id="c610b-123">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c610b-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c610b-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="c610b-124">-VMName</span></span>
<span data-ttu-id="c610b-125">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c610b-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="c610b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c610b-126">CommonParameters</span></span>
<span data-ttu-id="c610b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c610b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c610b-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c610b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c610b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c610b-129">INPUTS</span></span>

### <span data-ttu-id="c610b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c610b-130">System.String</span></span>

## <span data-ttu-id="c610b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c610b-131">OUTPUTS</span></span>

### <span data-ttu-id="c610b-132">Microsoft. Azure. Commands. Compute. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c610b-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="c610b-133">Note</span><span class="sxs-lookup"><span data-stu-id="c610b-133">NOTES</span></span>

## <span data-ttu-id="c610b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c610b-134">RELATED LINKS</span></span>

[<span data-ttu-id="c610b-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c610b-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="c610b-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="c610b-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


