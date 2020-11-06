---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: 23da9524d2641f390fcd29a62fd469d34cf05de3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517491"
---
# <span data-ttu-id="81e46-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="81e46-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="81e46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81e46-102">SYNOPSIS</span></span>
<span data-ttu-id="81e46-103">Aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="81e46-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81e46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81e46-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81e46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81e46-105">DESCRIPTION</span></span>
<span data-ttu-id="81e46-106">Il cmdlet **Add-AzureRmVmssWinRMListener** aggiunge un listener di gestione remota Windows (WinRM) nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="81e46-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="81e46-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81e46-107">EXAMPLES</span></span>

### <span data-ttu-id="81e46-108">Esempio 1: aggiungere un listener di WinRM a VMSS</span><span class="sxs-lookup"><span data-stu-id="81e46-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="81e46-109">Questo esempio aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="81e46-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="81e46-110">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="81e46-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="81e46-111">Il secondo comando aggiunge un listener di WinRM di protocollo HTTP con il certificato in corrispondenza dell'URL specificato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="81e46-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="81e46-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81e46-112">PARAMETERS</span></span>

### <span data-ttu-id="81e46-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="81e46-113">-CertificateUrl</span></span>
<span data-ttu-id="81e46-114">Specifica un collegamento, come URL, del certificato con cui vengono provisioning le nuove macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="81e46-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="81e46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e46-115">-DefaultProfile</span></span>
<span data-ttu-id="81e46-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81e46-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e46-117">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="81e46-117">-Protocol</span></span>
<span data-ttu-id="81e46-118">Specifica il protocollo del listener di WinRM.</span><span class="sxs-lookup"><span data-stu-id="81e46-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="81e46-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="81e46-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="81e46-120">Http</span><span class="sxs-lookup"><span data-stu-id="81e46-120">Http</span></span>
- <span data-ttu-id="81e46-121">Https</span><span class="sxs-lookup"><span data-stu-id="81e46-121">Https</span></span>

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

### <span data-ttu-id="81e46-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="81e46-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="81e46-123">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="81e46-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="81e46-124">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="81e46-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="81e46-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81e46-125">-Confirm</span></span>
<span data-ttu-id="81e46-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e46-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e46-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e46-127">-WhatIf</span></span>
<span data-ttu-id="81e46-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81e46-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81e46-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81e46-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e46-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e46-130">CommonParameters</span></span>
<span data-ttu-id="81e46-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e46-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e46-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e46-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e46-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81e46-133">INPUTS</span></span>

### <span data-ttu-id="81e46-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="81e46-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="81e46-135">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ProtocolTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="81e46-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="81e46-136">System. String</span><span class="sxs-lookup"><span data-stu-id="81e46-136">System.String</span></span>

## <span data-ttu-id="81e46-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81e46-137">OUTPUTS</span></span>

### <span data-ttu-id="81e46-138">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="81e46-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="81e46-139">Note</span><span class="sxs-lookup"><span data-stu-id="81e46-139">NOTES</span></span>

## <span data-ttu-id="81e46-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81e46-140">RELATED LINKS</span></span>

[<span data-ttu-id="81e46-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="81e46-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


