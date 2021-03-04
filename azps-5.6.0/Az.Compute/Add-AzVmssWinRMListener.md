---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 9e4c560021f03b2612d2b7d3bd60fd91a72aa53b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969470"
---
# <span data-ttu-id="3aef4-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="3aef4-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="3aef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aef4-102">SYNOPSIS</span></span>
<span data-ttu-id="3aef4-103">Aggiunge un listener WinRM al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="3aef4-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="3aef4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3aef4-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3aef4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3aef4-105">DESCRIPTION</span></span>
<span data-ttu-id="3aef4-106">Il cmdlet **Add-AzVmssWinRM Consente** di aggiungere un listener Windows Remote Management (WinRM) nel set di scala delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3aef4-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3aef4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3aef4-107">EXAMPLES</span></span>

### <span data-ttu-id="3aef4-108">Esempio 1: Aggiungere un listener WinRM a VMSS</span><span class="sxs-lookup"><span data-stu-id="3aef4-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="3aef4-109">Questo esempio aggiunge un listener WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="3aef4-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="3aef4-110">Il primo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione VMSS e archivia il risultato nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="3aef4-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="3aef4-111">Il secondo comando aggiunge un listener WinRM del protocollo HTTP con il certificato all'URL specificato al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="3aef4-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="3aef4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aef4-112">PARAMETERS</span></span>

### <span data-ttu-id="3aef4-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="3aef4-113">-CertificateUrl</span></span>
<span data-ttu-id="3aef4-114">Specifica un collegamento, come URL, del certificato con cui viene eseguito il provisioning delle nuove macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="3aef4-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="3aef4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aef4-115">-DefaultProfile</span></span>
<span data-ttu-id="3aef4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3aef4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aef4-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3aef4-117">-Protocol</span></span>
<span data-ttu-id="3aef4-118">Specifica il protocollo del listener WinRM.</span><span class="sxs-lookup"><span data-stu-id="3aef4-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="3aef4-119">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="3aef4-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3aef4-120">Http (http)</span><span class="sxs-lookup"><span data-stu-id="3aef4-120">Http</span></span>
- <span data-ttu-id="3aef4-121">Https</span><span class="sxs-lookup"><span data-stu-id="3aef4-121">Https</span></span>

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

### <span data-ttu-id="3aef4-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3aef4-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3aef4-123">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="3aef4-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="3aef4-124">È possibile usare il cmdlet New-AzVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3aef4-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="3aef4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3aef4-125">-Confirm</span></span>
<span data-ttu-id="3aef4-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aef4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aef4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aef4-127">-WhatIf</span></span>
<span data-ttu-id="3aef4-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3aef4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3aef4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3aef4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aef4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aef4-130">CommonParameters</span></span>
<span data-ttu-id="3aef4-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aef4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aef4-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3aef4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aef4-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="3aef4-133">INPUTS</span></span>

### <span data-ttu-id="3aef4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3aef4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3aef4-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3aef4-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3aef4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3aef4-136">System.String</span></span>

## <span data-ttu-id="3aef4-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3aef4-137">OUTPUTS</span></span>

### <span data-ttu-id="3aef4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3aef4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3aef4-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="3aef4-139">NOTES</span></span>

## <span data-ttu-id="3aef4-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3aef4-140">RELATED LINKS</span></span>

[<span data-ttu-id="3aef4-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3aef4-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


