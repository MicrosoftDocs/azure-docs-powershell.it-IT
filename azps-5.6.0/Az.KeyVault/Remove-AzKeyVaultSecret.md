---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 675107a27774cf2fe44ef328cdb0d7a3569e8abb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952493"
---
# <span data-ttu-id="488df-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="488df-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="488df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="488df-102">SYNOPSIS</span></span>
<span data-ttu-id="488df-103">Elimina un segreto in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="488df-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="488df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="488df-104">SYNTAX</span></span>

### <span data-ttu-id="488df-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="488df-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="488df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="488df-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="488df-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="488df-107">DESCRIPTION</span></span>
<span data-ttu-id="488df-108">Il Remove-AzKeyVaultSecret cmdlet elimina un segreto in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="488df-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="488df-109">Se il segreto è stato eliminato accidentalmente, il segreto può essere recuperato usando Undo-AzKeyVaultSecretRemoval da un utente con speciali autorizzazioni di "recupero".</span><span class="sxs-lookup"><span data-stu-id="488df-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="488df-110">Questo cmdlet ha un valore alto per la **proprietà ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="488df-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="488df-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="488df-111">EXAMPLES</span></span>

### <span data-ttu-id="488df-112">Esempio 1: Rimuovere un segreto da un vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="488df-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

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

<span data-ttu-id="488df-113">Questo comando rimuove il segreto denominato FinanceSecret dalla chiave vault denominata Contoso.'</span><span class="sxs-lookup"><span data-stu-id="488df-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="488df-114">Esempio 2: Rimuovere un segreto da un vault delle chiavi senza conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="488df-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

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

<span data-ttu-id="488df-115">Questo comando rimuove il segreto denominato FinanceSecret dalla chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="488df-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="488df-116">Il comando specifica i parametri *Force* e *Confirm* e, di conseguenza, il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="488df-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="488df-117">Esempio 3: Ripulire il segreto eliminato dal vault delle chiavi in modo permanente</span><span class="sxs-lookup"><span data-stu-id="488df-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="488df-118">Questo comando elimina definitivamente il segreto denominato FinanceSecret dalla chiave vault contoso.</span><span class="sxs-lookup"><span data-stu-id="488df-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="488df-119">Per l'esecuzione di questo cmdlet è necessaria l'autorizzazione di eliminazione, che deve essere stata concessa in precedenza ed esplicitamente all'utente per il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="488df-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="488df-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="488df-120">PARAMETERS</span></span>

### <span data-ttu-id="488df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="488df-121">-DefaultProfile</span></span>
<span data-ttu-id="488df-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="488df-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="488df-123">-Force</span><span class="sxs-lookup"><span data-stu-id="488df-123">-Force</span></span>
<span data-ttu-id="488df-124">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="488df-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="488df-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="488df-125">-InputObject</span></span>
<span data-ttu-id="488df-126">Oggetto segreto vault chiave</span><span class="sxs-lookup"><span data-stu-id="488df-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="488df-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="488df-127">-InRemovedState</span></span>
<span data-ttu-id="488df-128">Se presente, rimuove definitivamente il segreto eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="488df-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="488df-129">-Name</span><span class="sxs-lookup"><span data-stu-id="488df-129">-Name</span></span>
<span data-ttu-id="488df-130">Specifica il nome di un segreto.</span><span class="sxs-lookup"><span data-stu-id="488df-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="488df-131">Questo cmdlet crea il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del vault delle chiavi e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="488df-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="488df-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="488df-132">-PassThru</span></span>
<span data-ttu-id="488df-133">Indica che questo cmdlet restituisce un **oggetto Microsoft.Azure.Commands.KeyVault.Models.Secret.**</span><span class="sxs-lookup"><span data-stu-id="488df-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="488df-134">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="488df-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="488df-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="488df-135">-VaultName</span></span>
<span data-ttu-id="488df-136">Specifica il nome del vault della chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="488df-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="488df-137">Questo cmdlet crea l'FQDN di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="488df-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="488df-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="488df-138">-Confirm</span></span>
<span data-ttu-id="488df-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="488df-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="488df-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="488df-140">-WhatIf</span></span>
<span data-ttu-id="488df-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="488df-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="488df-142">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="488df-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="488df-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="488df-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="488df-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="488df-144">CommonParameters</span></span>
<span data-ttu-id="488df-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="488df-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="488df-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="488df-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="488df-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="488df-147">INPUTS</span></span>

### <span data-ttu-id="488df-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="488df-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="488df-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="488df-149">OUTPUTS</span></span>

### <span data-ttu-id="488df-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="488df-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="488df-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="488df-151">NOTES</span></span>

## <span data-ttu-id="488df-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="488df-152">RELATED LINKS</span></span>

[<span data-ttu-id="488df-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="488df-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="488df-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="488df-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="488df-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="488df-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

