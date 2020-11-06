---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 24c97e73728dab656a1d9fe3283e4eba6aae4ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508747"
---
# <span data-ttu-id="2bac6-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2bac6-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="2bac6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bac6-102">SYNOPSIS</span></span>
<span data-ttu-id="2bac6-103">Aggiunge le chiavi pubbliche per SSH per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2bac6-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bac6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bac6-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bac6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bac6-105">DESCRIPTION</span></span>
<span data-ttu-id="2bac6-106">Il cmdlet **Add-AzureRmVMSshPublicKey** aggiunge le chiavi pubbliche che è possibile usare per connettersi a una macchina virtuale su Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="2bac6-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="2bac6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bac6-107">EXAMPLES</span></span>

### <span data-ttu-id="2bac6-108">Esempio 1: aggiungere una chiave pubblica a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2bac6-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="2bac6-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="2bac6-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="2bac6-110">Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2bac6-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="2bac6-111">Il secondo comando aggiunge la chiave pubblica nella posizione in VirtualMachine07 specificata dal parametro path.</span><span class="sxs-lookup"><span data-stu-id="2bac6-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="2bac6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bac6-112">PARAMETERS</span></span>

### <span data-ttu-id="2bac6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bac6-113">-DefaultProfile</span></span>
<span data-ttu-id="2bac6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bac6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bac6-115">-Dati</span><span class="sxs-lookup"><span data-stu-id="2bac6-115">-KeyData</span></span>
<span data-ttu-id="2bac6-116">Specifica una codifica di base 64 di una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="2bac6-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="2bac6-117">È possibile connettersi a una macchina virtuale usando SSH o usando la chiave specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2bac6-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="2bac6-118">-Path</span><span class="sxs-lookup"><span data-stu-id="2bac6-118">-Path</span></span>
<span data-ttu-id="2bac6-119">Specifica il percorso completo di un file, nella macchina virtuale, in cui questo cmdlet archivia la chiave pubblica SSH.</span><span class="sxs-lookup"><span data-stu-id="2bac6-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="2bac6-120">Se il file esiste già, questo cmdlet aggiunge la chiave al file.</span><span class="sxs-lookup"><span data-stu-id="2bac6-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="2bac6-121">-VM</span><span class="sxs-lookup"><span data-stu-id="2bac6-121">-VM</span></span>
<span data-ttu-id="2bac6-122">Specifica l'oggetto macchina virtuale modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bac6-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="2bac6-123">Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="2bac6-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="2bac6-124">Puoi usare il cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) per creare un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2bac6-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="2bac6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bac6-125">CommonParameters</span></span>
<span data-ttu-id="2bac6-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bac6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bac6-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bac6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bac6-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bac6-128">INPUTS</span></span>

## <span data-ttu-id="2bac6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bac6-129">OUTPUTS</span></span>

## <span data-ttu-id="2bac6-130">Note</span><span class="sxs-lookup"><span data-stu-id="2bac6-130">NOTES</span></span>

## <span data-ttu-id="2bac6-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bac6-131">RELATED LINKS</span></span>

[<span data-ttu-id="2bac6-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2bac6-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2bac6-133">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="2bac6-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
