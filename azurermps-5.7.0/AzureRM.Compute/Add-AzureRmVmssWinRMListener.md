---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508372"
---
# <span data-ttu-id="9f897-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="9f897-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="9f897-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f897-102">SYNOPSIS</span></span>
<span data-ttu-id="9f897-103">Aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="9f897-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f897-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f897-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f897-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f897-105">DESCRIPTION</span></span>
<span data-ttu-id="9f897-106">Il cmdlet **Add-AzureRmVmssWinRMListener** aggiunge un listener di gestione remota Windows (WinRM) nel set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9f897-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9f897-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f897-107">EXAMPLES</span></span>

### <span data-ttu-id="9f897-108">Esempio 1: aggiungere un listener di WinRM a VMSS</span><span class="sxs-lookup"><span data-stu-id="9f897-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="9f897-109">Questo esempio aggiunge un listener di WinRM a VMSS.</span><span class="sxs-lookup"><span data-stu-id="9f897-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="9f897-110">Il primo comando usa il cmdlet **New-AzureRmVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="9f897-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="9f897-111">Il secondo comando aggiunge un listener di WinRM di protocollo HTTP con il certificato in corrispondenza dell'URL specificato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="9f897-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="9f897-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f897-112">PARAMETERS</span></span>

### <span data-ttu-id="9f897-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="9f897-113">-CertificateUrl</span></span>
<span data-ttu-id="9f897-114">Specifica un collegamento, come URL, del certificato con cui vengono provisioning le nuove macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="9f897-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="9f897-115">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="9f897-115">-Protocol</span></span>
<span data-ttu-id="9f897-116">Specifica il protocollo del listener di WinRM.</span><span class="sxs-lookup"><span data-stu-id="9f897-116">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="9f897-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9f897-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f897-118">Http</span><span class="sxs-lookup"><span data-stu-id="9f897-118">Http</span></span>
- <span data-ttu-id="9f897-119">Https</span><span class="sxs-lookup"><span data-stu-id="9f897-119">Https</span></span>

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

### <span data-ttu-id="9f897-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9f897-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9f897-121">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="9f897-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="9f897-122">Puoi usare il cmdlet New-AzureRmVmssConfig per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9f897-122">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="9f897-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f897-123">-Confirm</span></span>
<span data-ttu-id="9f897-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f897-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f897-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f897-125">-WhatIf</span></span>
<span data-ttu-id="9f897-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f897-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f897-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f897-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f897-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f897-128">CommonParameters</span></span>
<span data-ttu-id="9f897-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f897-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f897-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f897-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f897-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f897-131">INPUTS</span></span>

### <span data-ttu-id="9f897-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9f897-132">None</span></span>
<span data-ttu-id="9f897-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9f897-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f897-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f897-134">OUTPUTS</span></span>

### <span data-ttu-id="9f897-135">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9f897-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9f897-136">Note</span><span class="sxs-lookup"><span data-stu-id="9f897-136">NOTES</span></span>

## <span data-ttu-id="9f897-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f897-137">RELATED LINKS</span></span>

[<span data-ttu-id="9f897-138">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9f897-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


