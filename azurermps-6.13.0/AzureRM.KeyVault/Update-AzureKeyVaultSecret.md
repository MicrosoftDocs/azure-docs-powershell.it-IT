---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
ms.openlocfilehash: d895485354c33daa4eac57b699358ee0335905be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688110"
---
# <span data-ttu-id="57b12-101">Update-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57b12-101">Update-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="57b12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57b12-102">SYNOPSIS</span></span>
<span data-ttu-id="57b12-103">Aggiorna gli attributi di un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="57b12-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57b12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57b12-104">SYNTAX</span></span>

### <span data-ttu-id="57b12-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57b12-105">Default (Default)</span></span>
```
Update-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57b12-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="57b12-106">InputObject</span></span>
```
Update-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57b12-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57b12-107">DESCRIPTION</span></span>
<span data-ttu-id="57b12-108">Il cmdlet **Update-AzureKeyVaultSecret** aggiorna gli attributi modificabili di un segreto in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="57b12-108">The **Update-AzureKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="57b12-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57b12-109">EXAMPLES</span></span>

### <span data-ttu-id="57b12-110">Esempio 1: modificare gli attributi di un segreto</span><span class="sxs-lookup"><span data-stu-id="57b12-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="57b12-111">I primi quattro comandi definiscono gli attributi per la data di scadenza, la data NotBefore, i tag e il tipo di contesto e archiviano gli attributi nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="57b12-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="57b12-112">Il comando finale modifica gli attributi per il segreto denominato HR nel Vault chiave denominato ContosoVault, usando le variabili archiviate.</span><span class="sxs-lookup"><span data-stu-id="57b12-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="57b12-113">Esempio 2: eliminare i tag e il tipo di contenuto per un segreto</span><span class="sxs-lookup"><span data-stu-id="57b12-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="57b12-114">Questo comando Elimina i tag e il tipo di contenuto per la versione specificata del segreto denominato HR nel Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="57b12-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="57b12-115">Esempio 3: disabilitare la versione corrente dei segreti il cui nome inizia con esso</span><span class="sxs-lookup"><span data-stu-id="57b12-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzureKeyVaultSecret -Enable $False
```

<span data-ttu-id="57b12-116">Il primo comando Archivia il valore stringa Contoso nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="57b12-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="57b12-117">Il secondo comando Archivia il valore stringa nella variabile $Prefix.</span><span class="sxs-lookup"><span data-stu-id="57b12-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="57b12-118">Il terzo comando usa il cmdlet Get-AzureKeyVaultSecret per ottenere i segreti nell'archivio chiavi specificato, quindi passa questi segreti al cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="57b12-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="57b12-119">Il cmdlet **Where-Object** filtra i segreti per i nomi che iniziano con i caratteri.</span><span class="sxs-lookup"><span data-stu-id="57b12-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="57b12-120">Il comando consente di eseguire il piping dei segreti che corrispondono al filtro al cmdlet Update-AzureKeyVaultSecret, che li Disabilita.</span><span class="sxs-lookup"><span data-stu-id="57b12-120">The command pipes the secrets that match the filter to the Update-AzureKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="57b12-121">Esempio 4: impostare ContentType per tutte le versioni di un segreto</span><span class="sxs-lookup"><span data-stu-id="57b12-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzureKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="57b12-122">I primi tre comandi definiscono le variabili di stringa da usare per i parametri *VAULTNAME* , *Name* e *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="57b12-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="57b12-123">Il quarto comando usa il cmdlet Get-AzureKeyVaultKey per ottenere le chiavi specificate e convoglia le chiavi al cmdlet Update-AzureKeyVaultSecret per impostare il tipo di contenuto su XML.</span><span class="sxs-lookup"><span data-stu-id="57b12-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzureKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="57b12-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57b12-124">PARAMETERS</span></span>

### <span data-ttu-id="57b12-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="57b12-125">-ContentType</span></span>
<span data-ttu-id="57b12-126">Tipo di contenuto segreto.</span><span class="sxs-lookup"><span data-stu-id="57b12-126">Secret's content type.</span></span>
<span data-ttu-id="57b12-127">Se non viene specificato, il valore esistente del tipo di contenuto segreto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="57b12-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="57b12-128">Rimuovere il valore del tipo di contenuto esistente specificando una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="57b12-128">Remove the existing content type value by specifying an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b12-129">-DefaultProfile</span></span>
<span data-ttu-id="57b12-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57b12-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b12-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="57b12-131">-Enable</span></span>
<span data-ttu-id="57b12-132">Se presente, abilitare un segreto se value è vero.</span><span class="sxs-lookup"><span data-stu-id="57b12-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="57b12-133">Disabilitare un segreto se il valore è false.</span><span class="sxs-lookup"><span data-stu-id="57b12-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="57b12-134">Se non specificato, il valore esistente dello stato abilitato/disabilitato del segreto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="57b12-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-135">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="57b12-135">-Expires</span></span>
<span data-ttu-id="57b12-136">Data di scadenza di un segreto in ora UTC.</span><span class="sxs-lookup"><span data-stu-id="57b12-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="57b12-137">Se non viene specificato, il valore esistente della data di scadenza del segreto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="57b12-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57b12-138">-InputObject</span></span>
<span data-ttu-id="57b12-139">Oggetto segreto</span><span class="sxs-lookup"><span data-stu-id="57b12-139">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="57b12-140">-Name</span></span>
<span data-ttu-id="57b12-141">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="57b12-141">Secret name.</span></span>
<span data-ttu-id="57b12-142">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="57b12-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="57b12-143">-NotBefore</span></span>
<span data-ttu-id="57b12-144">Ora UTC prima della quale non è possibile usare il segreto.</span><span class="sxs-lookup"><span data-stu-id="57b12-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="57b12-145">Se non specificato, il valore esistente dell'attributo NotBefore del segreto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="57b12-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57b12-146">-PassThru</span></span>
<span data-ttu-id="57b12-147">Cmdlet non restituisce Object per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="57b12-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="57b12-148">Se questa opzione è specificata, restituire l'oggetto segreto.</span><span class="sxs-lookup"><span data-stu-id="57b12-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="57b12-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="57b12-149">-Tag</span></span>
<span data-ttu-id="57b12-150">Hashtable che rappresenta i tag segreti.</span><span class="sxs-lookup"><span data-stu-id="57b12-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="57b12-151">Se non specificato, i tag esistenti del segreto rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="57b12-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="57b12-152">Rimuovere un contrassegno specificando una tabella hash vuota.</span><span class="sxs-lookup"><span data-stu-id="57b12-152">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-153">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="57b12-153">-VaultName</span></span>
<span data-ttu-id="57b12-154">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="57b12-154">Vault name.</span></span>
<span data-ttu-id="57b12-155">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="57b12-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-156">-Versione</span><span class="sxs-lookup"><span data-stu-id="57b12-156">-Version</span></span>
<span data-ttu-id="57b12-157">Versione nascosta.</span><span class="sxs-lookup"><span data-stu-id="57b12-157">Secret version.</span></span>
<span data-ttu-id="57b12-158">Cmdlet costruisce l'FQDN di un segreto dal nome del Vault, l'ambiente attualmente selezionato, il nome segreto e la versione segreta.</span><span class="sxs-lookup"><span data-stu-id="57b12-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b12-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57b12-159">-Confirm</span></span>
<span data-ttu-id="57b12-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b12-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b12-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b12-161">-WhatIf</span></span>
<span data-ttu-id="57b12-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57b12-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57b12-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57b12-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b12-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b12-164">CommonParameters</span></span>
<span data-ttu-id="57b12-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b12-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b12-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57b12-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b12-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57b12-167">INPUTS</span></span>

### <span data-ttu-id="57b12-168">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57b12-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="57b12-169">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="57b12-169">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="57b12-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57b12-170">OUTPUTS</span></span>

### <span data-ttu-id="57b12-171">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="57b12-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="57b12-172">Note</span><span class="sxs-lookup"><span data-stu-id="57b12-172">NOTES</span></span>

## <span data-ttu-id="57b12-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57b12-173">RELATED LINKS</span></span>
