---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: cc30a9d8417603d9503fb4681cf8e05280a40c37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852185"
---
# <span data-ttu-id="84121-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="84121-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="84121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84121-102">SYNOPSIS</span></span>
<span data-ttu-id="84121-103">Aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="84121-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="84121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84121-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84121-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84121-105">DESCRIPTION</span></span>
<span data-ttu-id="84121-106">Il cmdlet **Add-AzVmssWinRMListener** aggiunge un listener di gestione remota Windows (WinRM) nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="84121-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="84121-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84121-107">EXAMPLES</span></span>

### <span data-ttu-id="84121-108">Esempio 1: aggiungere un listener di WinRM a VMSS</span><span class="sxs-lookup"><span data-stu-id="84121-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="84121-109">Questo esempio aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="84121-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="84121-110">Il primo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="84121-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="84121-111">Il secondo comando aggiunge un listener di WinRM di protocollo HTTP con il certificato in corrispondenza dell'URL specificato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="84121-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="84121-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84121-112">PARAMETERS</span></span>

### <span data-ttu-id="84121-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="84121-113">-CertificateUrl</span></span>
<span data-ttu-id="84121-114">Specifica un collegamento, come URL, del certificato con cui vengono provisioning le nuove macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="84121-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="84121-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84121-115">-DefaultProfile</span></span>
<span data-ttu-id="84121-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84121-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84121-117">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="84121-117">-Protocol</span></span>
<span data-ttu-id="84121-118">Specifica il protocollo del listener di WinRM.</span><span class="sxs-lookup"><span data-stu-id="84121-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="84121-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="84121-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84121-120">Http</span><span class="sxs-lookup"><span data-stu-id="84121-120">Http</span></span>
- <span data-ttu-id="84121-121">Https</span><span class="sxs-lookup"><span data-stu-id="84121-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84121-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="84121-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="84121-123">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="84121-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="84121-124">Puoi usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84121-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="84121-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84121-125">-Confirm</span></span>
<span data-ttu-id="84121-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84121-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84121-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84121-127">-WhatIf</span></span>
<span data-ttu-id="84121-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84121-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84121-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84121-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84121-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84121-130">CommonParameters</span></span>
<span data-ttu-id="84121-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84121-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84121-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84121-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84121-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84121-133">INPUTS</span></span>

### <span data-ttu-id="84121-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="84121-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="84121-135">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ProtocolTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="84121-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="84121-136">System. String</span><span class="sxs-lookup"><span data-stu-id="84121-136">System.String</span></span>

## <span data-ttu-id="84121-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84121-137">OUTPUTS</span></span>

### <span data-ttu-id="84121-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="84121-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="84121-139">Note</span><span class="sxs-lookup"><span data-stu-id="84121-139">NOTES</span></span>

## <span data-ttu-id="84121-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84121-140">RELATED LINKS</span></span>

[<span data-ttu-id="84121-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="84121-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


