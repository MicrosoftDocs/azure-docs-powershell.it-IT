---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 908810f658cdd4083bd24356eaab4e52d4dd5158
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395119"
---
# <span data-ttu-id="560e4-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="560e4-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="560e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="560e4-102">SYNOPSIS</span></span>
<span data-ttu-id="560e4-103">Aggiunge un segreto a un VMSS.</span><span class="sxs-lookup"><span data-stu-id="560e4-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="560e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="560e4-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="560e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="560e4-105">DESCRIPTION</span></span>
<span data-ttu-id="560e4-106">Il cmdlet **Add-AzVmssSecret** aggiunge un segreto al set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="560e4-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="560e4-107">Il segreto deve essere archiviato in un Vault di chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="560e4-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="560e4-108">Per altre informazioni relative a Key Vault, vedere [cos'è Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="560e4-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="560e4-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="560e4-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="560e4-110">Per altre informazioni sui cmdlet, vedere cmdlet di [Key Vault di Azure](/powershell/module/az.keyvault) o cmdlet [set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) .</span><span class="sxs-lookup"><span data-stu-id="560e4-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="560e4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="560e4-111">EXAMPLES</span></span>

### <span data-ttu-id="560e4-112">Esempio 1: aggiungere un segreto a VMSS</span><span class="sxs-lookup"><span data-stu-id="560e4-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="560e4-113">Questo esempio aggiunge un segreto a VMSS.</span><span class="sxs-lookup"><span data-stu-id="560e4-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="560e4-114">Il primo comando usa il cmdlet Get-AzKeyVault per ottenere un segreto della volta dal Vault denominato ContosoVault e archivia il risultato nella variabile denominata $Vault.</span><span class="sxs-lookup"><span data-stu-id="560e4-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="560e4-115">Il secondo comando usa il cmdlet **New-AzVmssVaultCertificateConfig** per creare una configurazione chiave del certificato Vault usando l'URL del certificato specificato dall'archivio certificati denominato certificati e archivia i risultati nella variabile denominata $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="560e4-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="560e4-116">Il terzo comando usa il cmdlet **New-AzVmssConfig** per creare un oggetto di configurazione vmss e archivia il risultato nella variabile denominata $vmss.</span><span class="sxs-lookup"><span data-stu-id="560e4-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="560e4-117">Il quarto comando aggiunge un segreto a VMSS con il segreto della volta usando l'ID risorsa chiave e il certificato del Vault archiviato nelle variabili $Vault e $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="560e4-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="560e4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="560e4-118">PARAMETERS</span></span>

### <span data-ttu-id="560e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560e4-119">-DefaultProfile</span></span>
<span data-ttu-id="560e4-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="560e4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="560e4-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="560e4-121">-SourceVaultId</span></span>
<span data-ttu-id="560e4-122">Specifica l'ID risorsa del Vault chiave che contiene i certificati che è possibile aggiungere alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="560e4-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="560e4-123">Questo valore funge anche da chiave per l'aggiunta di più certificati.</span><span class="sxs-lookup"><span data-stu-id="560e4-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="560e4-124">Questo significa che puoi usare lo stesso valore per il parametro *SourceVaultId* quando Aggiungi più certificati dallo stesso Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="560e4-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="560e4-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="560e4-125">-VaultCertificate</span></span>
<span data-ttu-id="560e4-126">Specifica l'oggetto **certificato** del Vault che contiene l'URL del certificato e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="560e4-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="560e4-127">Puoi usare il cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) per creare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="560e4-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="560e4-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="560e4-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="560e4-129">Specifica l'oggetto VMSS.</span><span class="sxs-lookup"><span data-stu-id="560e4-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="560e4-130">Puoi usare il cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) per creare questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="560e4-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="560e4-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="560e4-131">-Confirm</span></span>
<span data-ttu-id="560e4-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="560e4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="560e4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="560e4-133">-WhatIf</span></span>
<span data-ttu-id="560e4-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="560e4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="560e4-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="560e4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="560e4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560e4-136">CommonParameters</span></span>
<span data-ttu-id="560e4-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="560e4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560e4-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560e4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560e4-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="560e4-139">INPUTS</span></span>

### <span data-ttu-id="560e4-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="560e4-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="560e4-141">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="560e4-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="560e4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="560e4-142">OUTPUTS</span></span>

### <span data-ttu-id="560e4-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="560e4-143">None</span></span>
<span data-ttu-id="560e4-144">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="560e4-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="560e4-145">Note</span><span class="sxs-lookup"><span data-stu-id="560e4-145">NOTES</span></span>

## <span data-ttu-id="560e4-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="560e4-146">RELATED LINKS</span></span>

[<span data-ttu-id="560e4-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="560e4-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="560e4-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="560e4-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
