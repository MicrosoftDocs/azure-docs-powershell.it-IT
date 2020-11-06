---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://go.microsoft.com/fwlink/?LinkId=690299
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: b5f2917da71e8c4539660dbb91dd81f3fb5d7959
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520519"
---
# <span data-ttu-id="27cca-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27cca-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="27cca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27cca-102">SYNOPSIS</span></span>
<span data-ttu-id="27cca-103">Elimina una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="27cca-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27cca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27cca-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27cca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27cca-105">DESCRIPTION</span></span>
<span data-ttu-id="27cca-106">Il cmdlet Remove-AzureKeyVaultKey Elimina una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="27cca-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="27cca-107">Se la chiave è stata eliminata accidentalmente, la chiave può essere recuperata usando Undo-AzureKeyVaultKeyRemoval da un utente con autorizzazioni di ripristino speciali.</span><span class="sxs-lookup"><span data-stu-id="27cca-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="27cca-108">Questo cmdlet ha un valore elevato per la proprietà **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="27cca-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="27cca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27cca-109">EXAMPLES</span></span>

### <span data-ttu-id="27cca-110">Esempio 1: rimuovere una chiave da un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="27cca-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="27cca-111">Questo comando rimuove la chiave denominata ITSoftware dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="27cca-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="27cca-112">Esempio 2: rimuovere una chiave senza la conferma dell'utente</span><span class="sxs-lookup"><span data-stu-id="27cca-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="27cca-113">Questo comando rimuove la chiave denominata ITSoftware dal Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="27cca-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="27cca-114">Il comando specifica i parametri *Force* e *Confirm* e, di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="27cca-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="27cca-115">Esempio 3: eliminare definitivamente una chiave eliminata dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="27cca-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="27cca-116">Questo comando rimuove la chiave denominata ITSoftware dal Vault chiave denominato Contoso in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="27cca-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="27cca-117">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente per questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="27cca-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="27cca-118">Esempio 4: rimuovere le chiavi usando l'operatore pipeline</span><span class="sxs-lookup"><span data-stu-id="27cca-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="27cca-119">Questo comando consente di ottenere tutte le chiavi nel Vault chiave denominato Contoso e di passarle al cmdlet **Where-Object** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="27cca-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="27cca-120">Questo cmdlet passa le chiavi che hanno un valore di $False per l'attributo **Enabled** al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="27cca-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="27cca-121">Questo cmdlet consente di rimuovere le chiavi.</span><span class="sxs-lookup"><span data-stu-id="27cca-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="27cca-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27cca-122">PARAMETERS</span></span>

### <span data-ttu-id="27cca-123">-Force</span><span class="sxs-lookup"><span data-stu-id="27cca-123">-Force</span></span>
<span data-ttu-id="27cca-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="27cca-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27cca-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="27cca-125">-InRemovedState</span></span>
<span data-ttu-id="27cca-126">Rimuovere definitivamente la chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="27cca-126">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="27cca-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="27cca-127">-Name</span></span>
<span data-ttu-id="27cca-128">Specifica il nome della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="27cca-128">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="27cca-129">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="27cca-129">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27cca-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27cca-130">-PassThru</span></span>
<span data-ttu-id="27cca-131">Indica che questo cmdlet restituisce un oggetto **Microsoft. Azure. Commands. DataVault. Models. bundle** .</span><span class="sxs-lookup"><span data-stu-id="27cca-131">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="27cca-132">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="27cca-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="27cca-133">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="27cca-133">-VaultName</span></span>
<span data-ttu-id="27cca-134">Specifica il nome del Vault chiave da cui rimuovere la chiave.</span><span class="sxs-lookup"><span data-stu-id="27cca-134">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="27cca-135">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="27cca-135">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="27cca-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27cca-136">-Confirm</span></span>
<span data-ttu-id="27cca-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27cca-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27cca-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27cca-138">-WhatIf</span></span>
<span data-ttu-id="27cca-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27cca-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27cca-140">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27cca-140">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27cca-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27cca-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27cca-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cca-142">-DefaultProfile</span></span>
<span data-ttu-id="27cca-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27cca-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27cca-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cca-144">CommonParameters</span></span>
<span data-ttu-id="27cca-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27cca-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cca-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27cca-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cca-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27cca-147">INPUTS</span></span>

### <span data-ttu-id="27cca-148">Stringa</span><span class="sxs-lookup"><span data-stu-id="27cca-148">String</span></span>

## <span data-ttu-id="27cca-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27cca-149">OUTPUTS</span></span>

### <span data-ttu-id="27cca-150">Microsoft. Azure. Commands. Vault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="27cca-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="27cca-151">Questo cmdlet restituisce un valore solo se specifichi il parametro *PassThru* .</span><span class="sxs-lookup"><span data-stu-id="27cca-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="27cca-152">Note</span><span class="sxs-lookup"><span data-stu-id="27cca-152">NOTES</span></span>

## <span data-ttu-id="27cca-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27cca-153">RELATED LINKS</span></span>

[<span data-ttu-id="27cca-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27cca-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="27cca-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27cca-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="27cca-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="27cca-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="27cca-157">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="27cca-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

