---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: de1cee534afa765c84cd20f4932b859cca8a71a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519279"
---
# <span data-ttu-id="e8471-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e8471-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="e8471-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8471-102">SYNOPSIS</span></span>
<span data-ttu-id="e8471-103">Aggiunge le chiavi pubbliche SSH a VMSS.</span><span class="sxs-lookup"><span data-stu-id="e8471-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8471-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8471-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8471-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8471-105">DESCRIPTION</span></span>
<span data-ttu-id="e8471-106">Il cmdlet **Add-AzureRmVmssSshPublicKey** aggiunge le chiavi pubbliche che è possibile usare per connettersi alle macchine virtuali vmss (Virtual Machine scale set) su Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="e8471-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="e8471-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8471-107">EXAMPLES</span></span>

### <span data-ttu-id="e8471-108">Esempio 1: aggiungere una chiave pubblica SSH a VMSS</span><span class="sxs-lookup"><span data-stu-id="e8471-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="e8471-109">Questo esempio aggiunge una chiave pubblica SSH a VMSS.</span><span class="sxs-lookup"><span data-stu-id="e8471-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="e8471-110">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="e8471-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="e8471-111">Il secondo comando aggiunge una chiave SSH con i dati chiave specificati e archivia la chiave nel percorso specificato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8471-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="e8471-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8471-112">PARAMETERS</span></span>

### <span data-ttu-id="e8471-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8471-113">-DefaultProfile</span></span>
<span data-ttu-id="e8471-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8471-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8471-115">-Dati</span><span class="sxs-lookup"><span data-stu-id="e8471-115">-KeyData</span></span>
<span data-ttu-id="e8471-116">Specifica i dati di una chiave pubblica RSA di SSH.</span><span class="sxs-lookup"><span data-stu-id="e8471-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="e8471-117">-Path</span><span class="sxs-lookup"><span data-stu-id="e8471-117">-Path</span></span>
<span data-ttu-id="e8471-118">Specifica il percorso completo di un file, nella macchina virtuale, in cui questo cmdlet archivia la chiave pubblica SSH.</span><span class="sxs-lookup"><span data-stu-id="e8471-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="e8471-119">Se il file esiste già, questo cmdlet aggiunge la chiave al file.</span><span class="sxs-lookup"><span data-stu-id="e8471-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="e8471-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8471-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e8471-121">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="e8471-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="e8471-122">Puoi usare il cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e8471-122">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8471-123">-Confirm</span></span>
<span data-ttu-id="e8471-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8471-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8471-125">-WhatIf</span></span>
<span data-ttu-id="e8471-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8471-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8471-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8471-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8471-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8471-128">CommonParameters</span></span>
<span data-ttu-id="e8471-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8471-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8471-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8471-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8471-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8471-131">INPUTS</span></span>

### <span data-ttu-id="e8471-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8471-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e8471-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e8471-133">System.String</span></span>

## <span data-ttu-id="e8471-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8471-134">OUTPUTS</span></span>

### <span data-ttu-id="e8471-135">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e8471-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e8471-136">Note</span><span class="sxs-lookup"><span data-stu-id="e8471-136">NOTES</span></span>

## <span data-ttu-id="e8471-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8471-137">RELATED LINKS</span></span>

[<span data-ttu-id="e8471-138">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e8471-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
