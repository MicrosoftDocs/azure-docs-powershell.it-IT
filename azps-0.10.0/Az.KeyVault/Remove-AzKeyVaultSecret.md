---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: db46a3dd8669d5c8eeeb85aeafc25654faa8c107
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861246"
---
# <span data-ttu-id="d3698-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d3698-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="d3698-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3698-102">SYNOPSIS</span></span>
<span data-ttu-id="d3698-103">Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="d3698-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="d3698-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3698-104">SYNTAX</span></span>

```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3698-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3698-105">DESCRIPTION</span></span>
<span data-ttu-id="d3698-106">Il cmdlet Remove-AzKeyVaultSecret Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="d3698-106">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="d3698-107">Se il segreto è stato eliminato accidentalmente, il segreto può essere recuperato usando Undo-AzKeyVaultSecretRemoval da un utente con autorizzazioni di ripristino speciali.</span><span class="sxs-lookup"><span data-stu-id="d3698-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="d3698-108">Questo cmdlet ha un valore elevato per la proprietà **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="d3698-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="d3698-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3698-109">EXAMPLES</span></span>

### <span data-ttu-id="d3698-110">Esempio 1: rimuovere un segreto da un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="d3698-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="d3698-111">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="d3698-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="d3698-112">Esempio 2: rimuovere un segreto da un Vault chiave senza la conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="d3698-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="d3698-113">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="d3698-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="d3698-114">Il comando specifica i parametri *Force* e *Confirm* e, di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="d3698-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="d3698-115">Esempio 3: eliminare definitivamente il segreto eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="d3698-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="d3698-116">Questo comando Premove il segreto denominato FinanceSecret dal Vault chiave denominato Contoso in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="d3698-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="d3698-117">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="d3698-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="d3698-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3698-118">PARAMETERS</span></span>

### <span data-ttu-id="d3698-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3698-119">-DefaultProfile</span></span>
<span data-ttu-id="d3698-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d3698-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3698-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d3698-121">-Force</span></span>
<span data-ttu-id="d3698-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d3698-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d3698-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d3698-123">-InRemovedState</span></span>
<span data-ttu-id="d3698-124">Se presente, rimuove definitivamente il segreto precedentemente eliminato.</span><span class="sxs-lookup"><span data-stu-id="d3698-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="d3698-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3698-125">-Name</span></span>
<span data-ttu-id="d3698-126">Specifica il nome di un segreto.</span><span class="sxs-lookup"><span data-stu-id="d3698-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="d3698-127">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="d3698-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3698-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3698-128">-PassThru</span></span>
<span data-ttu-id="d3698-129">Indica che questo cmdlet restituisce un oggetto **Microsoft. Azure. Commands. DataVault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="d3698-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="d3698-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d3698-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3698-131">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="d3698-131">-VaultName</span></span>
<span data-ttu-id="d3698-132">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="d3698-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="d3698-133">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="d3698-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3698-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3698-134">-Confirm</span></span>
<span data-ttu-id="d3698-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3698-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3698-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3698-136">-WhatIf</span></span>
<span data-ttu-id="d3698-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3698-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3698-138">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3698-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3698-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3698-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3698-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3698-140">CommonParameters</span></span>
<span data-ttu-id="d3698-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3698-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3698-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3698-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3698-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3698-143">INPUTS</span></span>

### <span data-ttu-id="d3698-144">Stringa</span><span class="sxs-lookup"><span data-stu-id="d3698-144">String</span></span>

## <span data-ttu-id="d3698-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3698-145">OUTPUTS</span></span>

### <span data-ttu-id="d3698-146">Microsoft. Azure. Commands. Vault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="d3698-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="d3698-147">Questo cmdlet restituisce un valore solo se specifichi il parametro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="d3698-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="d3698-148">Note</span><span class="sxs-lookup"><span data-stu-id="d3698-148">NOTES</span></span>

## <span data-ttu-id="d3698-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3698-149">RELATED LINKS</span></span>

[<span data-ttu-id="d3698-150">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d3698-150">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="d3698-151">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d3698-151">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="d3698-152">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="d3698-152">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

