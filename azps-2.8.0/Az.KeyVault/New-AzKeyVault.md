---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 08f3b7ebaa7b1bc07bdac10b5b7cc16cb4405534
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674144"
---
# <span data-ttu-id="f40b9-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f40b9-101">New-AzKeyVault</span></span>

## <span data-ttu-id="f40b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f40b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f40b9-103">Crea un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f40b9-103">Creates a key vault.</span></span>

## <span data-ttu-id="f40b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f40b9-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f40b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f40b9-105">DESCRIPTION</span></span>
<span data-ttu-id="f40b9-106">Il cmdlet **New-AzKeyVault** crea un Vault Key nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="f40b9-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="f40b9-107">Questo cmdlet concede anche le autorizzazioni per l'utente attualmente connesso per aggiungere, rimuovere o elencare chiavi e segreti nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="f40b9-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="f40b9-108">Nota: se viene visualizzato l'errore **l'abbonamento non è registrato per l'uso dello spazio dei nomi "Microsoft. Key Vault"** quando si tenta di creare il nuovo Vault chiave, eseguire **Register-AzResourceProvider-ProviderNamespace "Microsoft. Key Vault"** e quindi eseguire di nuovo il comando **New-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="f40b9-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="f40b9-109">Per altre informazioni, vedere Register-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="f40b9-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="f40b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f40b9-110">EXAMPLES</span></span>

### <span data-ttu-id="f40b9-111">Esempio 1: creare un Vault chiave standard</span><span class="sxs-lookup"><span data-stu-id="f40b9-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="f40b9-112">Questo comando crea un Vault chiave denominato Contoso03Vault, nell'area di Azure est US.</span><span class="sxs-lookup"><span data-stu-id="f40b9-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="f40b9-113">Il comando aggiunge il Vault chiave al gruppo di risorse denominato Group14.</span><span class="sxs-lookup"><span data-stu-id="f40b9-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="f40b9-114">Poiché il comando non specifica un valore per il parametro *SKU* , crea un Vault chiave standard.</span><span class="sxs-lookup"><span data-stu-id="f40b9-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="f40b9-115">Esempio 2: creare un Vault Key Premium</span><span class="sxs-lookup"><span data-stu-id="f40b9-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="f40b9-116">Questo comando crea un Vault chiave, proprio come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="f40b9-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="f40b9-117">Tuttavia, specifica un valore Premium per il parametro *SKU* per creare un Vault Key Premium.</span><span class="sxs-lookup"><span data-stu-id="f40b9-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="f40b9-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f40b9-118">PARAMETERS</span></span>

### <span data-ttu-id="f40b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f40b9-119">-DefaultProfile</span></span>
<span data-ttu-id="f40b9-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f40b9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f40b9-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f40b9-121">-EnabledForDeployment</span></span>
<span data-ttu-id="f40b9-122">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f40b9-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f40b9-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f40b9-124">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="f40b9-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f40b9-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f40b9-126">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="f40b9-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="f40b9-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="f40b9-128">Se specificato, la protezione dall'eliminazione immediata è abilitata per il Vault; è necessario abilitare l'eliminazione morbida anche.</span><span class="sxs-lookup"><span data-stu-id="f40b9-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="f40b9-129">-EnableSoftDelete</span></span>
<span data-ttu-id="f40b9-130">Specifica che la funzionalità di eliminazione morbida è abilitata per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f40b9-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="f40b9-131">Quando è abilitata l'eliminazione morbida, per un periodo di tolleranza, è possibile recuperare il Vault chiave e il relativo contenuto dopo l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="f40b9-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="f40b9-132">Per altre informazioni su questa funzionalità, vedere [Panoramica dell'eliminazione di Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="f40b9-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="f40b9-133">Per istruzioni su come fare, Vedi [come usare Key Vault soft-delete con PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="f40b9-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f40b9-134">-Location</span></span>
<span data-ttu-id="f40b9-135">Specifica l'area di Azure in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f40b9-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="f40b9-136">Usare il comando [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) per visualizzare le opzioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="f40b9-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="f40b9-137">-Name</span></span>
<span data-ttu-id="f40b9-138">Specifica un nome per il Vault della chiave da creare.</span><span class="sxs-lookup"><span data-stu-id="f40b9-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="f40b9-139">Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="f40b9-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="f40b9-140">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="f40b9-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="f40b9-141">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="f40b9-141">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f40b9-142">-ResourceGroupName</span></span>
<span data-ttu-id="f40b9-143">Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f40b9-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="f40b9-144">-Sku</span></span>
<span data-ttu-id="f40b9-145">Specifica l'USK dell'istanza Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f40b9-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="f40b9-146">Per informazioni sulle caratteristiche disponibili per ogni Usk, vedere il sito Web relativo ai prezzi di Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="f40b9-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="f40b9-147">-Tag</span></span>
<span data-ttu-id="f40b9-148">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f40b9-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f40b9-149">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f40b9-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f40b9-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f40b9-150">-Confirm</span></span>
<span data-ttu-id="f40b9-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f40b9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f40b9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f40b9-152">-WhatIf</span></span>
<span data-ttu-id="f40b9-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f40b9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f40b9-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f40b9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f40b9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f40b9-155">CommonParameters</span></span>
<span data-ttu-id="f40b9-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f40b9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f40b9-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f40b9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f40b9-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f40b9-158">INPUTS</span></span>

### <span data-ttu-id="f40b9-159">System. String</span><span class="sxs-lookup"><span data-stu-id="f40b9-159">System.String</span></span>

### <span data-ttu-id="f40b9-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f40b9-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f40b9-161">Microsoft. Azure. Management. DataVault. Models. SkuName</span><span class="sxs-lookup"><span data-stu-id="f40b9-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="f40b9-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f40b9-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f40b9-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f40b9-163">OUTPUTS</span></span>

### <span data-ttu-id="f40b9-164">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f40b9-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f40b9-165">Note</span><span class="sxs-lookup"><span data-stu-id="f40b9-165">NOTES</span></span>

## <span data-ttu-id="f40b9-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f40b9-166">RELATED LINKS</span></span>

[<span data-ttu-id="f40b9-167">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f40b9-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="f40b9-168">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="f40b9-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)