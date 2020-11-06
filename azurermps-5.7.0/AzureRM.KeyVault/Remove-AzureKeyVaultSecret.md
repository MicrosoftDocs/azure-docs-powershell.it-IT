---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: a4b90f91c44fc54f60539c326a6b37caba868488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518099"
---
# <span data-ttu-id="511da-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="511da-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="511da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="511da-102">SYNOPSIS</span></span>
<span data-ttu-id="511da-103">Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="511da-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="511da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="511da-104">SYNTAX</span></span>

### <span data-ttu-id="511da-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="511da-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="511da-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="511da-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511da-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="511da-107">DESCRIPTION</span></span>
<span data-ttu-id="511da-108">Il cmdlet Remove-AzureKeyVaultSecret Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="511da-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="511da-109">Se il segreto è stato eliminato accidentalmente, il segreto può essere recuperato usando Undo-AzureKeyVaultSecretRemoval da un utente con autorizzazioni di ripristino speciali.</span><span class="sxs-lookup"><span data-stu-id="511da-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="511da-110">Questo cmdlet ha un valore elevato per la proprietà **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="511da-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="511da-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="511da-111">EXAMPLES</span></span>

### <span data-ttu-id="511da-112">Esempio 1: rimuovere un segreto da un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="511da-112">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="511da-113">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="511da-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="511da-114">Esempio 2: rimuovere un segreto da un Vault chiave senza la conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="511da-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="511da-115">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="511da-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="511da-116">Il comando specifica i parametri *Force* e *Confirm* e, di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="511da-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="511da-117">Esempio 3: eliminare definitivamente il segreto eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="511da-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="511da-118">Questo comando Premove il segreto denominato FinanceSecret dal Vault chiave denominato Contoso in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="511da-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="511da-119">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="511da-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="511da-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="511da-120">PARAMETERS</span></span>

### <span data-ttu-id="511da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511da-121">-DefaultProfile</span></span>
<span data-ttu-id="511da-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="511da-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="511da-123">-Force</span><span class="sxs-lookup"><span data-stu-id="511da-123">-Force</span></span>
<span data-ttu-id="511da-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="511da-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511da-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="511da-125">-InputObject</span></span>
<span data-ttu-id="511da-126">Oggetto segreto Key Vault</span><span class="sxs-lookup"><span data-stu-id="511da-126">Key Vault Secret Object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="511da-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="511da-127">-InRemovedState</span></span>
<span data-ttu-id="511da-128">Se presente, rimuove definitivamente il segreto precedentemente eliminato.</span><span class="sxs-lookup"><span data-stu-id="511da-128">If present, removes the previously deleted secret permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511da-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="511da-129">-Name</span></span>
<span data-ttu-id="511da-130">Specifica il nome di un segreto.</span><span class="sxs-lookup"><span data-stu-id="511da-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="511da-131">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="511da-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="511da-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="511da-132">-PassThru</span></span>
<span data-ttu-id="511da-133">Indica che questo cmdlet restituisce un oggetto **Microsoft. Azure. Commands. DataVault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="511da-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="511da-134">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="511da-134">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511da-135">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="511da-135">-VaultName</span></span>
<span data-ttu-id="511da-136">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="511da-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="511da-137">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="511da-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="511da-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="511da-138">-Confirm</span></span>
<span data-ttu-id="511da-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511da-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511da-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511da-140">-WhatIf</span></span>
<span data-ttu-id="511da-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="511da-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="511da-142">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="511da-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="511da-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="511da-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511da-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511da-144">CommonParameters</span></span>
<span data-ttu-id="511da-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511da-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511da-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="511da-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511da-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="511da-147">INPUTS</span></span>

### <span data-ttu-id="511da-148">Stringa</span><span class="sxs-lookup"><span data-stu-id="511da-148">String</span></span>

## <span data-ttu-id="511da-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="511da-149">OUTPUTS</span></span>

### <span data-ttu-id="511da-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="511da-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>
<span data-ttu-id="511da-151">Questo cmdlet restituisce un valore solo se specifichi il parametro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="511da-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="511da-152">Note</span><span class="sxs-lookup"><span data-stu-id="511da-152">NOTES</span></span>

## <span data-ttu-id="511da-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="511da-153">RELATED LINKS</span></span>

[<span data-ttu-id="511da-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="511da-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="511da-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="511da-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="511da-156">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="511da-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

