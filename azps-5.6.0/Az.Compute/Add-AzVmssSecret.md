---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: ec07964f62a22385d98c8cd9b8c98ea0b088ec8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969533"
---
# <span data-ttu-id="db156-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="db156-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="db156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db156-102">SYNOPSIS</span></span>
<span data-ttu-id="db156-103">Aggiunge un segreto a un sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="db156-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="db156-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db156-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db156-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db156-105">DESCRIPTION</span></span>
<span data-ttu-id="db156-106">Il cmdlet **Add-AzVmssSecret** aggiunge un segreto al set di scalabilità delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="db156-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="db156-107">Il segreto deve essere archiviato in un Vault chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="db156-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="db156-108">Per altre informazioni relative al Vault delle chiavi, vedere [Che cos'è il Vault delle chiavi di Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="db156-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="db156-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="db156-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="db156-110">Per altre informazioni sui cmdlet, vedere i cmdlet del Vault delle chiavi di [Azure](/powershell/module/az.keyvault) o il cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="db156-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="db156-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db156-111">EXAMPLES</span></span>

### <span data-ttu-id="db156-112">Esempio 1: Aggiungere un segreto al sistema VMS</span><span class="sxs-lookup"><span data-stu-id="db156-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="db156-113">Questo esempio aggiunge un segreto al sistema VMSS.</span><span class="sxs-lookup"><span data-stu-id="db156-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="db156-114">Il primo comando usa il cmdlet Get-AzKeyVault per ottenere un segreto del vault dal vault denominato ContosoVault e archivia il risultato nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="db156-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="db156-115">Il secondo comando usa il cmdlet **New-AzVmssVaultCertificateConfig** per creare una configurazione del certificato del Vault delle chiavi usando l'URL del certificato specificato dall'archivio certificati denominato Certificati e archivia i risultati nella variabile denominata $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="db156-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="db156-116">Il terzo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione VMSS e archivia il risultato nella variabile $VMSS.</span><span class="sxs-lookup"><span data-stu-id="db156-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="db156-117">Il quarto comando aggiunge un segreto a VMSS usando il segreto del vault usando l'ID risorsa chiave e il certificato di vault archiviati nelle variabili $Vault e $CertConfig chiave.</span><span class="sxs-lookup"><span data-stu-id="db156-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="db156-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db156-118">PARAMETERS</span></span>

### <span data-ttu-id="db156-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db156-119">-DefaultProfile</span></span>
<span data-ttu-id="db156-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db156-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db156-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="db156-121">-SourceVaultId</span></span>
<span data-ttu-id="db156-122">Specifica l'ID della risorsa del Vault delle chiavi che contiene i certificati che è possibile aggiungere alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="db156-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="db156-123">Questo valore funge anche da chiave per l'aggiunta di più certificati.</span><span class="sxs-lookup"><span data-stu-id="db156-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="db156-124">Questo significa che è possibile usare lo stesso valore per il parametro *SourceVaultId* quando si aggiungono più certificati dallo stesso Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="db156-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="db156-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="db156-125">-VaultCertificate</span></span>
<span data-ttu-id="db156-126">Specifica l'oggetto **Certificato del** Vault che contiene l'URL del certificato e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="db156-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="db156-127">È possibile usare il cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) per creare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="db156-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db156-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="db156-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="db156-129">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="db156-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="db156-130">È possibile usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="db156-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="db156-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db156-131">-Confirm</span></span>
<span data-ttu-id="db156-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db156-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db156-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db156-133">-WhatIf</span></span>
<span data-ttu-id="db156-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db156-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db156-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db156-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db156-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db156-136">CommonParameters</span></span>
<span data-ttu-id="db156-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db156-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db156-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db156-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db156-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="db156-139">INPUTS</span></span>

### <span data-ttu-id="db156-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="db156-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="db156-141">System.String</span><span class="sxs-lookup"><span data-stu-id="db156-141">System.String</span></span>

### <span data-ttu-id="db156-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="db156-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="db156-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db156-143">OUTPUTS</span></span>

### <span data-ttu-id="db156-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="db156-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="db156-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="db156-145">NOTES</span></span>

## <span data-ttu-id="db156-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db156-146">RELATED LINKS</span></span>

[<span data-ttu-id="db156-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="db156-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="db156-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="db156-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
