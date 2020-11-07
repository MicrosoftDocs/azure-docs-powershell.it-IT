---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685849"
---
# <span data-ttu-id="04e91-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="04e91-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="04e91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04e91-102">SYNOPSIS</span></span>
<span data-ttu-id="04e91-103">Aggiunge le chiavi pubbliche per SSH per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04e91-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04e91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04e91-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="04e91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04e91-105">DESCRIPTION</span></span>
<span data-ttu-id="04e91-106">Il cmdlet **Add-AzureRmVMSshPublicKey** aggiunge le chiavi pubbliche che è possibile usare per connettersi a una macchina virtuale su Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="04e91-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="04e91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04e91-107">EXAMPLES</span></span>

### <span data-ttu-id="04e91-108">Esempio 1: aggiungere una chiave pubblica a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="04e91-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="04e91-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="04e91-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="04e91-110">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="04e91-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="04e91-111">Il secondo comando aggiunge la chiave pubblica nella posizione in VirtualMachine07 specificata dal parametro path.</span><span class="sxs-lookup"><span data-stu-id="04e91-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="04e91-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04e91-112">PARAMETERS</span></span>

### <span data-ttu-id="04e91-113">-Dati</span><span class="sxs-lookup"><span data-stu-id="04e91-113">-KeyData</span></span>
<span data-ttu-id="04e91-114">Specifica una codifica di base 64 di una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="04e91-114">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="04e91-115">È possibile connettersi a una macchina virtuale usando SSH o usando la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="04e91-115">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e91-116">-Path</span><span class="sxs-lookup"><span data-stu-id="04e91-116">-Path</span></span>
<span data-ttu-id="04e91-117">Specifica il percorso completo di un file, nella macchina virtuale, in cui questo cmdlet archivia la chiave pubblica SSH.</span><span class="sxs-lookup"><span data-stu-id="04e91-117">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="04e91-118">Se il file esiste già, questo cmdlet aggiunge la chiave al file.</span><span class="sxs-lookup"><span data-stu-id="04e91-118">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="04e91-119">-VM</span><span class="sxs-lookup"><span data-stu-id="04e91-119">-VM</span></span>
<span data-ttu-id="04e91-120">Specifica l'oggetto macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04e91-120">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="04e91-121">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="04e91-121">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="04e91-122">Puoi usare il cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="04e91-122">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04e91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e91-123">CommonParameters</span></span>
<span data-ttu-id="04e91-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04e91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e91-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e91-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e91-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04e91-126">INPUTS</span></span>

### <span data-ttu-id="04e91-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="04e91-127">None</span></span>
<span data-ttu-id="04e91-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="04e91-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04e91-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04e91-129">OUTPUTS</span></span>

## <span data-ttu-id="04e91-130">Note</span><span class="sxs-lookup"><span data-stu-id="04e91-130">NOTES</span></span>

## <span data-ttu-id="04e91-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04e91-131">RELATED LINKS</span></span>

[<span data-ttu-id="04e91-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04e91-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="04e91-133">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="04e91-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
