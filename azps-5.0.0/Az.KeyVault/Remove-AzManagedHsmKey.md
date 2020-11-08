---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193247"
---
# <span data-ttu-id="b9060-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b9060-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="b9060-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9060-102">SYNOPSIS</span></span>
<span data-ttu-id="b9060-103">Elimina una chiave in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="b9060-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="b9060-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9060-104">SYNTAX</span></span>

### <span data-ttu-id="b9060-105">RemoveByKeyNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9060-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9060-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9060-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9060-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9060-107">DESCRIPTION</span></span>
<span data-ttu-id="b9060-108">Il cmdlet Remove-AzManagedHsmKey Elimina una chiave in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="b9060-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="b9060-109">Se la chiave è stata eliminata accidentalmente, la chiave può essere recuperata usando Undo-AzManagedHsmKeyRemoval da un utente con autorizzazioni di ripristino speciali.</span><span class="sxs-lookup"><span data-stu-id="b9060-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="b9060-110">Questo cmdlet ha un valore elevato per la proprietà **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="b9060-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="b9060-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9060-111">EXAMPLES</span></span>

### <span data-ttu-id="b9060-112">Esempio 1: rimuovere una chiave da un HSM gestito</span><span class="sxs-lookup"><span data-stu-id="b9060-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="b9060-113">Questo comando rimuove la chiave denominata TestKey dall'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="b9060-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="b9060-114">Esempio 2: rimuovere una chiave senza la conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="b9060-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="b9060-115">Questo comando rimuove la chiave denominata TestKey dall'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="b9060-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="b9060-116">Il comando specifica il parametro *Force* e, di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="b9060-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b9060-117">Esempio 3: eliminare definitivamente una chiave eliminata dall'HSM gestito</span><span class="sxs-lookup"><span data-stu-id="b9060-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="b9060-118">Questo comando consente di rimuovere definitivamente la chiave denominata TestKey dall'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="b9060-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="b9060-119">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente per questo HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="b9060-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="b9060-120">Esempio 4: rimuovere le chiavi usando l'operatore pipeline</span><span class="sxs-lookup"><span data-stu-id="b9060-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="b9060-121">Questo comando consente di ottenere tutte le chiavi nell'HSM gestito denominato testmhsm e di passarle al cmdlet **Where-Object** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9060-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b9060-122">Questo cmdlet passa le chiavi che hanno un valore di $False per l'attributo **Enabled** al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="b9060-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="b9060-123">Questo cmdlet consente di rimuovere le chiavi.</span><span class="sxs-lookup"><span data-stu-id="b9060-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="b9060-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9060-124">PARAMETERS</span></span>

### <span data-ttu-id="b9060-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9060-125">-DefaultProfile</span></span>
<span data-ttu-id="b9060-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9060-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9060-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b9060-127">-Force</span></span>
<span data-ttu-id="b9060-128">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b9060-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b9060-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b9060-129">-HsmName</span></span>
<span data-ttu-id="b9060-130">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="b9060-130">HSM name.</span></span> <span data-ttu-id="b9060-131">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="b9060-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9060-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9060-132">-InputObject</span></span>
<span data-ttu-id="b9060-133">Oggetto chiave</span><span class="sxs-lookup"><span data-stu-id="b9060-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9060-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b9060-134">-InRemovedState</span></span>
<span data-ttu-id="b9060-135">Rimuovere definitivamente la chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b9060-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="b9060-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9060-136">-Name</span></span>
<span data-ttu-id="b9060-137">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="b9060-137">Key name.</span></span>
<span data-ttu-id="b9060-138">Cmdlet costruisce il nome di dominio completo di una chiave dal nome di HSM gestito, dall'ambiente selezionato e dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="b9060-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9060-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9060-139">-PassThru</span></span>
<span data-ttu-id="b9060-140">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b9060-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b9060-141">Se questa opzione è specificata, il cmdlet restituisce l'oggetto chiave che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="b9060-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="b9060-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9060-142">-Confirm</span></span>
<span data-ttu-id="b9060-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9060-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9060-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9060-144">-WhatIf</span></span>
<span data-ttu-id="b9060-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9060-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9060-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9060-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9060-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9060-147">CommonParameters</span></span>
<span data-ttu-id="b9060-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9060-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9060-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9060-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9060-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9060-150">INPUTS</span></span>

### <span data-ttu-id="b9060-151">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b9060-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="b9060-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9060-152">OUTPUTS</span></span>

### <span data-ttu-id="b9060-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b9060-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="b9060-154">Note</span><span class="sxs-lookup"><span data-stu-id="b9060-154">NOTES</span></span>

## <span data-ttu-id="b9060-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9060-155">RELATED LINKS</span></span>

[<span data-ttu-id="b9060-156">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b9060-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="b9060-157">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b9060-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="b9060-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b9060-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="b9060-159">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="b9060-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="b9060-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b9060-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="b9060-161">Ripristinare-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="b9060-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)