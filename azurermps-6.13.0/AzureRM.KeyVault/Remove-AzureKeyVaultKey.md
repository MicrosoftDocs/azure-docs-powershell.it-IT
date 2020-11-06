---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: ff7e5a02899d806633e485f06f419a6f1f2082a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516583"
---
# <span data-ttu-id="906c3-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="906c3-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="906c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="906c3-102">SYNOPSIS</span></span>
<span data-ttu-id="906c3-103">Elimina una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="906c3-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="906c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="906c3-104">SYNTAX</span></span>

### <span data-ttu-id="906c3-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="906c3-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="906c3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="906c3-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="906c3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="906c3-107">DESCRIPTION</span></span>
<span data-ttu-id="906c3-108">Il cmdlet Remove-AzureKeyVaultKey Elimina una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="906c3-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="906c3-109">Se la chiave è stata eliminata accidentalmente, la chiave può essere recuperata usando Undo-AzureKeyVaultKeyRemoval da un utente con autorizzazioni di ripristino speciali.</span><span class="sxs-lookup"><span data-stu-id="906c3-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="906c3-110">Questo cmdlet ha un valore elevato per la proprietà **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="906c3-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="906c3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="906c3-111">EXAMPLES</span></span>

### <span data-ttu-id="906c3-112">Esempio 1: rimuovere una chiave da un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="906c3-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

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

<span data-ttu-id="906c3-113">Questo comando rimuove la chiave denominata ITSoftware dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="906c3-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="906c3-114">Esempio 2: rimuovere una chiave senza la conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="906c3-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="906c3-115">Questo comando rimuove la chiave denominata ITSoftware dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="906c3-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="906c3-116">Il comando specifica il parametro *Force* e, di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="906c3-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="906c3-117">Esempio 3: eliminare definitivamente una chiave eliminata dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="906c3-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="906c3-118">Questo comando rimuove la chiave denominata ITSoftware dal Vault chiave denominato Contoso in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="906c3-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="906c3-119">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="906c3-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="906c3-120">Esempio 4: rimuovere le chiavi usando l'operatore pipeline</span><span class="sxs-lookup"><span data-stu-id="906c3-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="906c3-121">Questo comando consente di ottenere tutte le chiavi nel Vault chiave denominato Contoso e di passarle al cmdlet **Where-Object** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="906c3-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="906c3-122">Questo cmdlet passa le chiavi che hanno un valore di $False per l'attributo **Enabled** al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="906c3-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="906c3-123">Questo cmdlet consente di rimuovere le chiavi.</span><span class="sxs-lookup"><span data-stu-id="906c3-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="906c3-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="906c3-124">PARAMETERS</span></span>

### <span data-ttu-id="906c3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906c3-125">-DefaultProfile</span></span>
<span data-ttu-id="906c3-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="906c3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="906c3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="906c3-127">-Force</span></span>
<span data-ttu-id="906c3-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="906c3-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="906c3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="906c3-129">-InputObject</span></span>
<span data-ttu-id="906c3-130">Oggetto bundle</span><span class="sxs-lookup"><span data-stu-id="906c3-130">KeyBundle Object</span></span>

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

### <span data-ttu-id="906c3-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="906c3-131">-InRemovedState</span></span>
<span data-ttu-id="906c3-132">Rimuovere definitivamente la chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="906c3-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="906c3-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="906c3-133">-Name</span></span>
<span data-ttu-id="906c3-134">Specifica il nome della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="906c3-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="906c3-135">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="906c3-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="906c3-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="906c3-136">-PassThru</span></span>
<span data-ttu-id="906c3-137">Indica che questo cmdlet restituisce un oggetto **Microsoft. Azure. Commands. DataVault. Models. PSKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="906c3-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="906c3-138">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="906c3-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="906c3-139">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="906c3-139">-VaultName</span></span>
<span data-ttu-id="906c3-140">Specifica il nome del Vault chiave da cui rimuovere la chiave.</span><span class="sxs-lookup"><span data-stu-id="906c3-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="906c3-141">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="906c3-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="906c3-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="906c3-142">-Confirm</span></span>
<span data-ttu-id="906c3-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="906c3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="906c3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="906c3-144">-WhatIf</span></span>
<span data-ttu-id="906c3-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="906c3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="906c3-146">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="906c3-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="906c3-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="906c3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="906c3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906c3-148">CommonParameters</span></span>
<span data-ttu-id="906c3-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="906c3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906c3-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="906c3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906c3-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="906c3-151">INPUTS</span></span>

### <span data-ttu-id="906c3-152">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="906c3-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="906c3-153">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="906c3-153">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="906c3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="906c3-154">OUTPUTS</span></span>

### <span data-ttu-id="906c3-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="906c3-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="906c3-156">Note</span><span class="sxs-lookup"><span data-stu-id="906c3-156">NOTES</span></span>

## <span data-ttu-id="906c3-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="906c3-157">RELATED LINKS</span></span>

[<span data-ttu-id="906c3-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="906c3-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="906c3-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="906c3-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="906c3-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="906c3-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="906c3-161">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="906c3-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

