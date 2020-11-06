---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: bff9c08a0c36fb7a4d89fb86d9c219491f3642b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515212"
---
# <span data-ttu-id="f2e54-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f2e54-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="f2e54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2e54-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e54-103">Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="f2e54-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2e54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2e54-104">SYNTAX</span></span>

### <span data-ttu-id="f2e54-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2e54-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2e54-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2e54-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2e54-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2e54-107">DESCRIPTION</span></span>
<span data-ttu-id="f2e54-108">Il cmdlet Remove-AzureKeyVaultSecret Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="f2e54-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="f2e54-109">Se il segreto è stato eliminato accidentalmente, il segreto può essere recuperato usando Undo-AzureKeyVaultSecretRemoval da un utente con autorizzazioni di ripristino speciali.</span><span class="sxs-lookup"><span data-stu-id="f2e54-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="f2e54-110">Questo cmdlet ha un valore elevato per la proprietà **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="f2e54-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="f2e54-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2e54-111">EXAMPLES</span></span>

### <span data-ttu-id="f2e54-112">Esempio 1: rimuovere un segreto da un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="f2e54-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="f2e54-113">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="f2e54-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="f2e54-114">Esempio 2: rimuovere un segreto da un Vault chiave senza la conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="f2e54-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="f2e54-115">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="f2e54-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="f2e54-116">Il comando specifica i parametri *Force* e *Confirm* e, di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="f2e54-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f2e54-117">Esempio 3: eliminare definitivamente il segreto eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="f2e54-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="f2e54-118">Questo comando Premove il segreto denominato FinanceSecret dal Vault chiave denominato Contoso in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="f2e54-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="f2e54-119">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="f2e54-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="f2e54-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2e54-120">PARAMETERS</span></span>

### <span data-ttu-id="f2e54-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e54-121">-DefaultProfile</span></span>
<span data-ttu-id="f2e54-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f2e54-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2e54-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f2e54-123">-Force</span></span>
<span data-ttu-id="f2e54-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f2e54-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2e54-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2e54-125">-InputObject</span></span>
<span data-ttu-id="f2e54-126">Oggetto segreto Key Vault</span><span class="sxs-lookup"><span data-stu-id="f2e54-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2e54-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f2e54-127">-InRemovedState</span></span>
<span data-ttu-id="f2e54-128">Se presente, rimuove definitivamente il segreto precedentemente eliminato.</span><span class="sxs-lookup"><span data-stu-id="f2e54-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="f2e54-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2e54-129">-Name</span></span>
<span data-ttu-id="f2e54-130">Specifica il nome di un segreto.</span><span class="sxs-lookup"><span data-stu-id="f2e54-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="f2e54-131">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="f2e54-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e54-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2e54-132">-PassThru</span></span>
<span data-ttu-id="f2e54-133">Indica che questo cmdlet restituisce un oggetto **Microsoft. Azure. Commands. DataVault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="f2e54-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="f2e54-134">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f2e54-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f2e54-135">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="f2e54-135">-VaultName</span></span>
<span data-ttu-id="f2e54-136">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="f2e54-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="f2e54-137">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="f2e54-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e54-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2e54-138">-Confirm</span></span>
<span data-ttu-id="f2e54-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2e54-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e54-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e54-140">-WhatIf</span></span>
<span data-ttu-id="f2e54-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2e54-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e54-142">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2e54-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2e54-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2e54-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2e54-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e54-144">CommonParameters</span></span>
<span data-ttu-id="f2e54-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2e54-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e54-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e54-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e54-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2e54-147">INPUTS</span></span>

### <span data-ttu-id="f2e54-148">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f2e54-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="f2e54-149">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2e54-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f2e54-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2e54-150">OUTPUTS</span></span>

### <span data-ttu-id="f2e54-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f2e54-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="f2e54-152">Note</span><span class="sxs-lookup"><span data-stu-id="f2e54-152">NOTES</span></span>

## <span data-ttu-id="f2e54-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2e54-153">RELATED LINKS</span></span>

[<span data-ttu-id="f2e54-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f2e54-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="f2e54-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f2e54-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="f2e54-156">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f2e54-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)
