---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190536"
---
# <span data-ttu-id="a9543-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a9543-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="a9543-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9543-102">SYNOPSIS</span></span>
<span data-ttu-id="a9543-103">Aggiunge le chiavi pubbliche per SSH per una macchina virtuale, quando si crea solo la VM.</span><span class="sxs-lookup"><span data-stu-id="a9543-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="a9543-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9543-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9543-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9543-105">DESCRIPTION</span></span>
<span data-ttu-id="a9543-106">Il cmdlet **Add-AzVMSshPublicKey** aggiunge le chiavi pubbliche che è possibile usare per connettersi a una macchina virtuale Linux su Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="a9543-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="a9543-107">Questo non può essere usato dopo la creazione di VM, se si prova a usare questo dopo la creazione di VM senza Update-AzVM, non ci sarà alcun errore, se si usa il comando con Update-AzVM, il comando verrà errore.</span><span class="sxs-lookup"><span data-stu-id="a9543-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="a9543-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9543-108">EXAMPLES</span></span>

### <span data-ttu-id="a9543-109">Esempio 1: aggiungere una chiave pubblica a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="a9543-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="a9543-110">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="a9543-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="a9543-111">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a9543-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a9543-112">Il secondo comando aggiunge la chiave pubblica nella posizione in VirtualMachine07 specificata dal parametro path.</span><span class="sxs-lookup"><span data-stu-id="a9543-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="a9543-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9543-113">PARAMETERS</span></span>

### <span data-ttu-id="a9543-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9543-114">-DefaultProfile</span></span>
<span data-ttu-id="a9543-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9543-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9543-116">-Dati</span><span class="sxs-lookup"><span data-stu-id="a9543-116">-KeyData</span></span>
<span data-ttu-id="a9543-117">Specifica una codifica di base 64 di una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="a9543-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="a9543-118">Puoi connetterti a una macchina virtuale Linux usando SSH o usando la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a9543-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9543-119">-Path</span><span class="sxs-lookup"><span data-stu-id="a9543-119">-Path</span></span>
<span data-ttu-id="a9543-120">Specifica il percorso completo di un file, nella macchina virtuale, in cui questo cmdlet archivia la chiave pubblica SSH.</span><span class="sxs-lookup"><span data-stu-id="a9543-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="a9543-121">Se il file esiste già, questo cmdlet aggiunge la chiave al file.</span><span class="sxs-lookup"><span data-stu-id="a9543-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="a9543-122">-VM</span><span class="sxs-lookup"><span data-stu-id="a9543-122">-VM</span></span>
<span data-ttu-id="a9543-123">Specifica l'oggetto macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9543-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="a9543-124">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="a9543-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="a9543-125">Puoi usare il cmdlet [New-AzVMConfig](./New-AzVMConfig.md) per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a9543-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9543-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9543-126">CommonParameters</span></span>
<span data-ttu-id="a9543-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9543-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9543-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9543-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9543-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9543-129">INPUTS</span></span>

### <span data-ttu-id="a9543-130">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a9543-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a9543-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a9543-131">System.String</span></span>

## <span data-ttu-id="a9543-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9543-132">OUTPUTS</span></span>

### <span data-ttu-id="a9543-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a9543-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a9543-134">Note</span><span class="sxs-lookup"><span data-stu-id="a9543-134">NOTES</span></span>

## <span data-ttu-id="a9543-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9543-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9543-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a9543-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a9543-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a9543-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
