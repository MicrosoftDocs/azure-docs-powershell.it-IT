---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 2e096b04830d50840d6298e7aa8085b0090a347e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520203"
---
# <span data-ttu-id="eb096-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="eb096-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="eb096-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb096-102">SYNOPSIS</span></span>
<span data-ttu-id="eb096-103">Rigenera la chiave specificata dell'account di archiviazione di Azure con chiave Key Vault.</span><span class="sxs-lookup"><span data-stu-id="eb096-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb096-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb096-104">SYNTAX</span></span>

### <span data-ttu-id="eb096-105">ByDefinitionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb096-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb096-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb096-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb096-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb096-107">DESCRIPTION</span></span>
<span data-ttu-id="eb096-108">Rigenera la chiave specificata di un account di archiviazione di Azure con chiave Key Vault e imposta la chiave come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="eb096-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="eb096-109">Key Vault inoltra la chiamata a Azure Resource Manager per rigenerare la chiave.</span><span class="sxs-lookup"><span data-stu-id="eb096-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="eb096-110">Il chiamante deve possedere le autorizzazioni per rigenerare le chiavi in un account di archiviazione di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="eb096-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="eb096-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb096-111">EXAMPLES</span></span>

### <span data-ttu-id="eb096-112">Esempio 1: rigenerare una chiave</span><span class="sxs-lookup"><span data-stu-id="eb096-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="eb096-113">Rigenera "Key1" dell'account "mystorageaccount" e imposta "Key1" come attivo dell'account di archiviazione di Azure Key.</span><span class="sxs-lookup"><span data-stu-id="eb096-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="eb096-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb096-114">PARAMETERS</span></span>

### <span data-ttu-id="eb096-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb096-115">-AccountName</span></span>
<span data-ttu-id="eb096-116">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="eb096-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="eb096-117">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="eb096-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb096-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb096-118">-DefaultProfile</span></span>
<span data-ttu-id="eb096-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eb096-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb096-120">-Force</span><span class="sxs-lookup"><span data-stu-id="eb096-120">-Force</span></span>
<span data-ttu-id="eb096-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="eb096-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb096-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb096-122">-InputObject</span></span>
<span data-ttu-id="eb096-123">Oggetto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="eb096-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb096-124">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="eb096-124">-KeyName</span></span>
<span data-ttu-id="eb096-125">Nome della chiave dell'account di archiviazione per rigenerare e rendere attivo.</span><span class="sxs-lookup"><span data-stu-id="eb096-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb096-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb096-126">-PassThru</span></span>
<span data-ttu-id="eb096-127">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="eb096-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="eb096-128">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="eb096-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="eb096-129">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="eb096-129">-VaultName</span></span>
<span data-ttu-id="eb096-130">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="eb096-130">Vault name.</span></span>
<span data-ttu-id="eb096-131">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="eb096-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb096-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eb096-132">-Confirm</span></span>
<span data-ttu-id="eb096-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb096-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb096-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb096-134">-WhatIf</span></span>
<span data-ttu-id="eb096-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb096-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb096-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb096-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb096-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb096-137">CommonParameters</span></span>
<span data-ttu-id="eb096-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb096-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb096-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb096-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb096-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb096-140">INPUTS</span></span>

### <span data-ttu-id="eb096-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="eb096-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="eb096-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eb096-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="eb096-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb096-143">OUTPUTS</span></span>

### <span data-ttu-id="eb096-144">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb096-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="eb096-145">Note</span><span class="sxs-lookup"><span data-stu-id="eb096-145">NOTES</span></span>

## <span data-ttu-id="eb096-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb096-146">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

