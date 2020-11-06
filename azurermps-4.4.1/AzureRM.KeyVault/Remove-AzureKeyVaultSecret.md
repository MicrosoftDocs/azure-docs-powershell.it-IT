---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520512"
---
# <span data-ttu-id="a515e-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a515e-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="a515e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a515e-102">SYNOPSIS</span></span>
<span data-ttu-id="a515e-103">Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="a515e-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a515e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a515e-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a515e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a515e-105">DESCRIPTION</span></span>
<span data-ttu-id="a515e-106">Il cmdlet Remove-AzureKeyVaultSecret Elimina un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="a515e-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="a515e-107">Se il segreto è stato eliminato accidentalmente, il segreto può essere recuperato usando Undo-AzureKeyVaultSecretRemoval da un utente con autorizzazioni di ripristino speciali.</span><span class="sxs-lookup"><span data-stu-id="a515e-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="a515e-108">Questo cmdlet ha un valore elevato per la proprietà **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="a515e-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="a515e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a515e-109">EXAMPLES</span></span>

### <span data-ttu-id="a515e-110">Esempio 1: rimuovere un segreto da un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="a515e-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="a515e-111">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="a515e-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="a515e-112">Esempio 2: rimuovere un segreto da un Vault chiave senza la conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="a515e-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="a515e-113">Questo comando rimuove il segreto denominato FinanceSecret dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="a515e-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="a515e-114">Il comando specifica i parametri *Force* e *Confirm* e, di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a515e-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a515e-115">Esempio 3: eliminare definitivamente il segreto eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="a515e-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="a515e-116">Questo comando Premove il segreto denominato FinanceSecret dal Vault chiave denominato Contoso in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="a515e-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="a515e-117">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a515e-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="a515e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a515e-118">PARAMETERS</span></span>

### <span data-ttu-id="a515e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a515e-119">-Force</span></span>
<span data-ttu-id="a515e-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a515e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a515e-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a515e-121">-InRemovedState</span></span>
<span data-ttu-id="a515e-122">Se presente, rimuove definitivamente il segreto precedentemente eliminato.</span><span class="sxs-lookup"><span data-stu-id="a515e-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="a515e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a515e-123">-Name</span></span>
<span data-ttu-id="a515e-124">Specifica il nome di un segreto.</span><span class="sxs-lookup"><span data-stu-id="a515e-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="a515e-125">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="a515e-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a515e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a515e-126">-PassThru</span></span>
<span data-ttu-id="a515e-127">Indica che questo cmdlet restituisce un oggetto **Microsoft. Azure. Commands. DataVault. Models. Secret** .</span><span class="sxs-lookup"><span data-stu-id="a515e-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="a515e-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a515e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a515e-129">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="a515e-129">-VaultName</span></span>
<span data-ttu-id="a515e-130">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="a515e-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="a515e-131">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="a515e-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="a515e-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a515e-132">-Confirm</span></span>
<span data-ttu-id="a515e-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a515e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a515e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a515e-134">-WhatIf</span></span>
<span data-ttu-id="a515e-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a515e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a515e-136">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a515e-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a515e-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a515e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a515e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a515e-138">-DefaultProfile</span></span>
<span data-ttu-id="a515e-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a515e-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a515e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a515e-140">CommonParameters</span></span>
<span data-ttu-id="a515e-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a515e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a515e-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a515e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a515e-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a515e-143">INPUTS</span></span>

### <span data-ttu-id="a515e-144">Stringa</span><span class="sxs-lookup"><span data-stu-id="a515e-144">String</span></span>

## <span data-ttu-id="a515e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a515e-145">OUTPUTS</span></span>

### <span data-ttu-id="a515e-146">Microsoft. Azure. Commands. Vault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="a515e-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="a515e-147">Questo cmdlet restituisce un valore solo se specifichi il parametro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="a515e-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="a515e-148">Note</span><span class="sxs-lookup"><span data-stu-id="a515e-148">NOTES</span></span>

## <span data-ttu-id="a515e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a515e-149">RELATED LINKS</span></span>

[<span data-ttu-id="a515e-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a515e-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="a515e-151">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a515e-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="a515e-152">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a515e-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

