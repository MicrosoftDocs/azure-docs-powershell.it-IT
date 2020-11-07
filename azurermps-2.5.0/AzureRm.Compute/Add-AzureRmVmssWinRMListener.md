---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
ms.openlocfilehash: dd9c13298adac34a53ed2f97bbc1e3edc95892df
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866151"
---
# <span data-ttu-id="b47e6-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="b47e6-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="b47e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b47e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b47e6-103">Aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="b47e6-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b47e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b47e6-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b47e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b47e6-105">DESCRIPTION</span></span>
<span data-ttu-id="b47e6-106">Il cmdlet **Add-AzureRmVmssWinRMListener** aggiunge un listener di gestione remota Windows (WinRM) nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b47e6-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b47e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b47e6-107">EXAMPLES</span></span>

### <span data-ttu-id="b47e6-108">Esempio 1: aggiungere un listener di WinRM a VMSS</span><span class="sxs-lookup"><span data-stu-id="b47e6-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="b47e6-109">Questo esempio aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="b47e6-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="b47e6-110">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="b47e6-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="b47e6-111">Il secondo comando aggiunge un listener di WinRM di protocollo HTTP con il certificato in corrispondenza dell'URL specificato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="b47e6-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="b47e6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b47e6-112">PARAMETERS</span></span>

### <span data-ttu-id="b47e6-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b47e6-113">-CertificateUrl</span></span>
<span data-ttu-id="b47e6-114">Specifica un collegamento, come URL, del certificato con cui vengono provisioning le nuove macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b47e6-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="b47e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47e6-115">-DefaultProfile</span></span>
<span data-ttu-id="b47e6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b47e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b47e6-117">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="b47e6-117">-Protocol</span></span>
<span data-ttu-id="b47e6-118">Specifica il protocollo del listener di WinRM.</span><span class="sxs-lookup"><span data-stu-id="b47e6-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="b47e6-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b47e6-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b47e6-120">Http</span><span class="sxs-lookup"><span data-stu-id="b47e6-120">Http</span></span>
- <span data-ttu-id="b47e6-121">Https</span><span class="sxs-lookup"><span data-stu-id="b47e6-121">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b47e6-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b47e6-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b47e6-123">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="b47e6-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="b47e6-124">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b47e6-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b47e6-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b47e6-125">-Confirm</span></span>
<span data-ttu-id="b47e6-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b47e6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b47e6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b47e6-127">-WhatIf</span></span>
<span data-ttu-id="b47e6-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b47e6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b47e6-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b47e6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b47e6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47e6-130">CommonParameters</span></span>
<span data-ttu-id="b47e6-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47e6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47e6-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b47e6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47e6-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b47e6-133">INPUTS</span></span>

### <span data-ttu-id="b47e6-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b47e6-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="b47e6-135">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b47e6-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="b47e6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b47e6-136">OUTPUTS</span></span>

### <span data-ttu-id="b47e6-137">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b47e6-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b47e6-138">Note</span><span class="sxs-lookup"><span data-stu-id="b47e6-138">NOTES</span></span>

## <span data-ttu-id="b47e6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b47e6-139">RELATED LINKS</span></span>

[<span data-ttu-id="b47e6-140">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b47e6-140">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


