---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 6ca619ba75fcf639e36650dc66d45d2f86ec8375
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687949"
---
# <span data-ttu-id="e2911-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e2911-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="e2911-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2911-102">SYNOPSIS</span></span>
<span data-ttu-id="e2911-103">Aggiunge le chiavi pubbliche SSH a VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2911-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2911-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2911-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2911-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2911-105">DESCRIPTION</span></span>
<span data-ttu-id="e2911-106">Il cmdlet **Add-AzureRmVmssSshPublicKey** aggiunge le chiavi pubbliche che è possibile usare per connettersi alle macchine virtuali vmss (Virtual Machine scale set) su Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="e2911-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="e2911-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2911-107">EXAMPLES</span></span>

### <span data-ttu-id="e2911-108">Esempio 1: aggiungere una chiave pubblica SSH a VMSS</span><span class="sxs-lookup"><span data-stu-id="e2911-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="e2911-109">Questo esempio aggiunge una chiave pubblica SSH a VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2911-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="e2911-110">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="e2911-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="e2911-111">Il secondo comando aggiunge una chiave SSH con i dati chiave specificati e archivia la chiave nel percorso specificato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e2911-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="e2911-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2911-112">PARAMETERS</span></span>

### <span data-ttu-id="e2911-113">-Dati</span><span class="sxs-lookup"><span data-stu-id="e2911-113">-KeyData</span></span>
<span data-ttu-id="e2911-114">Specifica i dati di una chiave pubblica RSA di SSH.</span><span class="sxs-lookup"><span data-stu-id="e2911-114">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="e2911-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e2911-115">-Path</span></span>
<span data-ttu-id="e2911-116">Specifica il percorso completo di un file, nella macchina virtuale, in cui questo cmdlet archivia la chiave pubblica SSH.</span><span class="sxs-lookup"><span data-stu-id="e2911-116">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="e2911-117">Se il file esiste già, questo cmdlet aggiunge la chiave al file.</span><span class="sxs-lookup"><span data-stu-id="e2911-117">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="e2911-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2911-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e2911-119">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2911-119">Specifies the VMSS object.</span></span>
<span data-ttu-id="e2911-120">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e2911-120">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2911-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2911-121">-Confirm</span></span>
<span data-ttu-id="e2911-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2911-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2911-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2911-123">-WhatIf</span></span>
<span data-ttu-id="e2911-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2911-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2911-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2911-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2911-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2911-126">CommonParameters</span></span>
<span data-ttu-id="e2911-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2911-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2911-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2911-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2911-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2911-129">INPUTS</span></span>

### <span data-ttu-id="e2911-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e2911-130">None</span></span>
<span data-ttu-id="e2911-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e2911-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2911-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2911-132">OUTPUTS</span></span>

###  
<span data-ttu-id="e2911-133">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e2911-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e2911-134">Note</span><span class="sxs-lookup"><span data-stu-id="e2911-134">NOTES</span></span>

## <span data-ttu-id="e2911-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2911-135">RELATED LINKS</span></span>

[<span data-ttu-id="e2911-136">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e2911-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
