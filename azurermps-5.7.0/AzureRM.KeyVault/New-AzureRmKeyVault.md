---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 7cc4af3e849a6cd24c2144c6e92c990da261e9d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687485"
---
# <span data-ttu-id="09826-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="09826-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="09826-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09826-102">SYNOPSIS</span></span>
<span data-ttu-id="09826-103">Crea un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="09826-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09826-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09826-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09826-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09826-105">DESCRIPTION</span></span>
<span data-ttu-id="09826-106">Il cmdlet **New-AzureRmKeyVault** crea un Vault Key nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="09826-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="09826-107">Questo cmdlet concede anche le autorizzazioni per l'utente attualmente connesso per aggiungere, rimuovere o elencare chiavi e segreti nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="09826-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="09826-108">Nota: se viene visualizzato l'errore **l'abbonamento non è registrato per l'uso dello spazio dei nomi "Microsoft. Key Vault"** quando si tenta di creare il nuovo Vault chiave, eseguire **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. Key Vault"** e quindi eseguire di nuovo il comando **New-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="09826-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="09826-109">Per altre informazioni, vedere Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="09826-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="09826-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09826-110">EXAMPLES</span></span>

### <span data-ttu-id="09826-111">Esempio 1: creare un Vault chiave standard</span><span class="sxs-lookup"><span data-stu-id="09826-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="09826-112">Questo comando crea un Vault chiave denominato Contoso03Vault, nell'area di Azure est US.</span><span class="sxs-lookup"><span data-stu-id="09826-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="09826-113">Il comando aggiunge il Vault chiave al gruppo di risorse denominato Group14.</span><span class="sxs-lookup"><span data-stu-id="09826-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="09826-114">Poiché il comando non specifica un valore per il parametro *SKU* , crea un Vault chiave standard.</span><span class="sxs-lookup"><span data-stu-id="09826-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="09826-115">Esempio 2: creare un Vault Key Premium</span><span class="sxs-lookup"><span data-stu-id="09826-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="09826-116">Questo comando crea un Vault chiave, proprio come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="09826-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="09826-117">Tuttavia, specifica un valore Premium per il parametro *SKU* per creare un Vault Key Premium.</span><span class="sxs-lookup"><span data-stu-id="09826-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="09826-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09826-118">PARAMETERS</span></span>

### <span data-ttu-id="09826-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09826-119">-DefaultProfile</span></span>
<span data-ttu-id="09826-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="09826-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09826-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="09826-121">-EnabledForDeployment</span></span>
<span data-ttu-id="09826-122">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09826-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="09826-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="09826-124">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="09826-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="09826-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="09826-126">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="09826-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-127">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="09826-127">-EnableSoftDelete</span></span>
<span data-ttu-id="09826-128">Specifica che la funzionalità di eliminazione morbida è abilitata per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="09826-128">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="09826-129">Quando è abilitata l'eliminazione morbida, per un periodo di tolleranza, è possibile recuperare il Vault chiave e il relativo contenuto dopo l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="09826-129">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>

<span data-ttu-id="09826-130">Per altre informazioni su questa funzionalità, vedere [Panoramica dell'eliminazione di Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="09826-130">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="09826-131">Per istruzioni su come fare, Vedi [come usare Key Vault soft-delete con PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="09826-131">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-132">-Posizione</span><span class="sxs-lookup"><span data-stu-id="09826-132">-Location</span></span>
<span data-ttu-id="09826-133">Specifica l'area di Azure in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="09826-133">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="09826-134">Usare il comando [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) per visualizzare le opzioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="09826-134">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="09826-135">-Name</span></span>
<span data-ttu-id="09826-136">Specifica un nome per il Vault della chiave da creare.</span><span class="sxs-lookup"><span data-stu-id="09826-136">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="09826-137">Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="09826-137">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="09826-138">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="09826-138">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="09826-139">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="09826-139">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09826-140">-ResourceGroupName</span></span>
<span data-ttu-id="09826-141">Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="09826-141">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="09826-142">-Sku</span></span>
<span data-ttu-id="09826-143">Specifica l'USK dell'istanza Key Vault.</span><span class="sxs-lookup"><span data-stu-id="09826-143">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="09826-144">Per informazioni sulle caratteristiche disponibili per ogni Usk, vedere il sito Web relativo ai prezzi di Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="09826-144">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="09826-145">-Tag</span></span>
<span data-ttu-id="09826-146">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="09826-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="09826-147">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="09826-147">For example:</span></span>

<span data-ttu-id="09826-148">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="09826-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09826-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09826-149">-Confirm</span></span>
<span data-ttu-id="09826-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09826-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09826-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09826-151">-WhatIf</span></span>
<span data-ttu-id="09826-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09826-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09826-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09826-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09826-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09826-154">CommonParameters</span></span>
<span data-ttu-id="09826-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09826-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09826-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09826-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09826-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09826-157">INPUTS</span></span>

### <span data-ttu-id="09826-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09826-158">None</span></span>
<span data-ttu-id="09826-159">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="09826-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09826-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09826-160">OUTPUTS</span></span>

### <span data-ttu-id="09826-161">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="09826-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="09826-162">Note</span><span class="sxs-lookup"><span data-stu-id="09826-162">NOTES</span></span>

## <span data-ttu-id="09826-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09826-163">RELATED LINKS</span></span>

[<span data-ttu-id="09826-164">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="09826-164">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="09826-165">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="09826-165">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
