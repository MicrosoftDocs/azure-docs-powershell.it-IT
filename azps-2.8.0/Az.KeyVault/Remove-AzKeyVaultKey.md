---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: afa9f59520cba9f90f0f5d0a2edb6564b73245bf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406146"
---
# <span data-ttu-id="4786f-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4786f-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="4786f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4786f-102">SYNOPSIS</span></span>
<span data-ttu-id="4786f-103">Elimina una chiave in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="4786f-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="4786f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4786f-104">SYNTAX</span></span>

### <span data-ttu-id="4786f-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4786f-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4786f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4786f-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4786f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4786f-107">DESCRIPTION</span></span>
<span data-ttu-id="4786f-108">Il Remove-AzKeyVaultKey cmdlet elimina una chiave in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="4786f-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="4786f-109">Se la chiave è stata eliminata accidentalmente, può essere recuperata usando Undo-AzKeyVaultKeyRemoval da un utente con speciali autorizzazioni di "recupero".</span><span class="sxs-lookup"><span data-stu-id="4786f-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="4786f-110">Questo cmdlet ha un valore alto per la **proprietà ConfirmImpact.**</span><span class="sxs-lookup"><span data-stu-id="4786f-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="4786f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4786f-111">EXAMPLES</span></span>

### <span data-ttu-id="4786f-112">Esempio 1: Rimuovere una chiave da un vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="4786f-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="4786f-113">Questo comando rimuove la chiave denominata ITSoftware dalla chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="4786f-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="4786f-114">Esempio 2: Rimuovere una chiave senza conferma utente</span><span class="sxs-lookup"><span data-stu-id="4786f-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="4786f-115">Questo comando rimuove la chiave denominata ITSoftware dalla chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="4786f-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="4786f-116">Il comando specifica il *parametro Force* e, di conseguenza, il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="4786f-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4786f-117">Esempio 3: Eliminare definitivamente una chiave eliminata dal vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="4786f-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="4786f-118">Questo comando rimuove la chiave denominata ITSoftware dalla chiave vault denominata Contoso in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="4786f-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="4786f-119">Per l'esecuzione di questo cmdlet è necessaria l'autorizzazione di eliminazione, che deve essere stata concessa in precedenza ed esplicitamente all'utente per il vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="4786f-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="4786f-120">Esempio 4: Rimuovere chiavi usando l'operatore pipeline</span><span class="sxs-lookup"><span data-stu-id="4786f-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="4786f-121">Questo comando recupera tutte le chiavi nel vault delle chiavi denominato Contoso e le passa al cmdlet **Where-Object** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="4786f-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4786f-122">Questo cmdlet passa le chiavi che hanno un valore di $False per **l'attributo Enabled** al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="4786f-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="4786f-123">Questo cmdlet rimuove queste chiavi.</span><span class="sxs-lookup"><span data-stu-id="4786f-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="4786f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4786f-124">PARAMETERS</span></span>

### <span data-ttu-id="4786f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4786f-125">-DefaultProfile</span></span>
<span data-ttu-id="4786f-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4786f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4786f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4786f-127">-Force</span></span>
<span data-ttu-id="4786f-128">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="4786f-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4786f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4786f-129">-InputObject</span></span>
<span data-ttu-id="4786f-130">Oggetto KeyBundle</span><span class="sxs-lookup"><span data-stu-id="4786f-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4786f-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4786f-131">-InRemovedState</span></span>
<span data-ttu-id="4786f-132">Rimuovere definitivamente la chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4786f-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="4786f-133">-Name</span><span class="sxs-lookup"><span data-stu-id="4786f-133">-Name</span></span>
<span data-ttu-id="4786f-134">Specifica il nome della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4786f-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="4786f-135">Questo cmdlet crea il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, al nome del vault delle chiavi e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="4786f-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4786f-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4786f-136">-PassThru</span></span>
<span data-ttu-id="4786f-137">Indica che questo cmdlet restituisce un **oggetto Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="4786f-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="4786f-138">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4786f-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4786f-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4786f-139">-VaultName</span></span>
<span data-ttu-id="4786f-140">Specifica il nome del vault della chiave da cui rimuovere la chiave.</span><span class="sxs-lookup"><span data-stu-id="4786f-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="4786f-141">Questo cmdlet crea l'FQDN di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="4786f-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="4786f-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4786f-142">-Confirm</span></span>
<span data-ttu-id="4786f-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4786f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4786f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4786f-144">-WhatIf</span></span>
<span data-ttu-id="4786f-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4786f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4786f-146">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4786f-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4786f-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4786f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4786f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4786f-148">CommonParameters</span></span>
<span data-ttu-id="4786f-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4786f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4786f-150">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4786f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4786f-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="4786f-151">INPUTS</span></span>

### <span data-ttu-id="4786f-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4786f-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="4786f-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4786f-153">OUTPUTS</span></span>

### <span data-ttu-id="4786f-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4786f-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="4786f-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="4786f-155">NOTES</span></span>

## <span data-ttu-id="4786f-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4786f-156">RELATED LINKS</span></span>

[<span data-ttu-id="4786f-157">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4786f-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="4786f-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4786f-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)


[<span data-ttu-id="4786f-159">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="4786f-159">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

