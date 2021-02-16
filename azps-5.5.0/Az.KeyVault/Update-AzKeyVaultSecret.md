---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185366"
---
# <span data-ttu-id="8c83b-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8c83b-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="8c83b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c83b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c83b-103">Aggiorna gli attributi di un segreto in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="8c83b-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="8c83b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c83b-104">SYNTAX</span></span>

### <span data-ttu-id="8c83b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c83b-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c83b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8c83b-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c83b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c83b-107">DESCRIPTION</span></span>
<span data-ttu-id="8c83b-108">Il cmdlet **Update-AzKeyVaultSecret** aggiorna gli attributi modificabili di un segreto in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="8c83b-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="8c83b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c83b-109">EXAMPLES</span></span>

### <span data-ttu-id="8c83b-110">Esempio 1: Modificare gli attributi di un segreto</span><span class="sxs-lookup"><span data-stu-id="8c83b-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="8c83b-111">I primi quattro comandi definiscono gli attributi per la data di scadenza, la data notBefore, i tag e il tipo di contesto e archiviano gli attributi nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="8c83b-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="8c83b-112">Il comando finale modifica gli attributi per il segreto denominato HR nella chiave vault denominata ContosoVault, usando le variabili archiviate.</span><span class="sxs-lookup"><span data-stu-id="8c83b-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="8c83b-113">Esempio 2: Eliminare i tag e il tipo di contenuto per un segreto</span><span class="sxs-lookup"><span data-stu-id="8c83b-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="8c83b-114">Questo comando elimina i tag e il tipo di contenuto per la versione specificata del segreto denominato HR nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="8c83b-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="8c83b-115">Esempio 3: Disabilitare la versione corrente dei segreti il cui nome inizia con l'IT</span><span class="sxs-lookup"><span data-stu-id="8c83b-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="8c83b-116">Il primo comando archivia il valore stringa Contoso nella $Vault variabile.</span><span class="sxs-lookup"><span data-stu-id="8c83b-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="8c83b-117">Il secondo comando archivia il valore stringa IT nella $Prefix variabile.</span><span class="sxs-lookup"><span data-stu-id="8c83b-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="8c83b-118">Il terzo comando usa il cmdlet Get-AzKeyVaultSecret per ottenere i segreti nel vault delle chiavi specificato e quindi passa tali informazioni al cmdlet **Where-Object.**</span><span class="sxs-lookup"><span data-stu-id="8c83b-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="8c83b-119">Il cmdlet **Where-Object** filtra i segreti per i nomi che iniziano con i caratteri IT.</span><span class="sxs-lookup"><span data-stu-id="8c83b-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="8c83b-120">Il comando consente di determinare i segreti che corrispondono al filtro Update-AzKeyVaultSecret cmdlet, disabilitandoli così.</span><span class="sxs-lookup"><span data-stu-id="8c83b-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="8c83b-121">Esempio 4: Impostare ContentType per tutte le versioni di un segreto</span><span class="sxs-lookup"><span data-stu-id="8c83b-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="8c83b-122">I primi tre comandi definiscono le variabili stringa da usare per i parametri *VaultName,* *Name* *e ContentType.*</span><span class="sxs-lookup"><span data-stu-id="8c83b-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="8c83b-123">Il quarto comando usa il cmdlet Get-AzKeyVaultKey per ottenere le chiavi specificate e le pipe al cmdlet Update-AzKeyVaultSecret per impostare il tipo di contenuto su XML.</span><span class="sxs-lookup"><span data-stu-id="8c83b-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="8c83b-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c83b-124">PARAMETERS</span></span>

### <span data-ttu-id="8c83b-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="8c83b-125">-ContentType</span></span>
<span data-ttu-id="8c83b-126">Tipo di contenuto segreto.</span><span class="sxs-lookup"><span data-stu-id="8c83b-126">Secret's content type.</span></span>
<span data-ttu-id="8c83b-127">Se non viene specificato, il valore esistente del tipo di contenuto del segreto rimarrà invariato.</span><span class="sxs-lookup"><span data-stu-id="8c83b-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="8c83b-128">Rimuovere il valore del tipo di contenuto esistente specificando una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8c83b-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="8c83b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c83b-129">-DefaultProfile</span></span>
<span data-ttu-id="8c83b-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c83b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c83b-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="8c83b-131">-Enable</span></span>
<span data-ttu-id="8c83b-132">Se presente, abilitare un segreto se il valore è vero.</span><span class="sxs-lookup"><span data-stu-id="8c83b-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="8c83b-133">Disabilitare un segreto se il valore è falso.</span><span class="sxs-lookup"><span data-stu-id="8c83b-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="8c83b-134">Se non viene specificato, il valore esistente dello stato abilitato/disabilitato del segreto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="8c83b-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="8c83b-135">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="8c83b-135">-Expires</span></span>
<span data-ttu-id="8c83b-136">Ora di scadenza di un segreto in ora UTC.</span><span class="sxs-lookup"><span data-stu-id="8c83b-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="8c83b-137">Se non viene specificato, il valore esistente della scadenza del segreto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="8c83b-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="8c83b-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c83b-138">-InputObject</span></span>
<span data-ttu-id="8c83b-139">Oggetto segreto</span><span class="sxs-lookup"><span data-stu-id="8c83b-139">Secret object</span></span>

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

### <span data-ttu-id="8c83b-140">-Name</span><span class="sxs-lookup"><span data-stu-id="8c83b-140">-Name</span></span>
<span data-ttu-id="8c83b-141">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="8c83b-141">Secret name.</span></span>
<span data-ttu-id="8c83b-142">Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato e il nome del segreto.</span><span class="sxs-lookup"><span data-stu-id="8c83b-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="8c83b-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="8c83b-143">-NotBefore</span></span>
<span data-ttu-id="8c83b-144">Ora UTC prima di cui non è possibile usare il segreto.</span><span class="sxs-lookup"><span data-stu-id="8c83b-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="8c83b-145">Se non viene specificato, il valore esistente dell'attributo NotBefore del segreto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="8c83b-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="8c83b-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c83b-146">-PassThru</span></span>
<span data-ttu-id="8c83b-147">Il cmdlet non restituisce l'oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8c83b-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="8c83b-148">Se questa opzione è specificata, restituisce l'oggetto Segreto.</span><span class="sxs-lookup"><span data-stu-id="8c83b-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="8c83b-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c83b-149">-Tag</span></span>
<span data-ttu-id="8c83b-150">Tabella hash che rappresenta i tag del segreto.</span><span class="sxs-lookup"><span data-stu-id="8c83b-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="8c83b-151">Se non viene specificato, i tag esistenti del segreto rimangono invariati.</span><span class="sxs-lookup"><span data-stu-id="8c83b-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="8c83b-152">Rimuovere un tag specificando una tabella hash vuota.</span><span class="sxs-lookup"><span data-stu-id="8c83b-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="8c83b-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8c83b-153">-VaultName</span></span>
<span data-ttu-id="8c83b-154">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="8c83b-154">Vault name.</span></span>
<span data-ttu-id="8c83b-155">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="8c83b-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8c83b-156">-Version</span><span class="sxs-lookup"><span data-stu-id="8c83b-156">-Version</span></span>
<span data-ttu-id="8c83b-157">Versione segreta.</span><span class="sxs-lookup"><span data-stu-id="8c83b-157">Secret version.</span></span>
<span data-ttu-id="8c83b-158">Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato, il nome segreto e la versione segreta.</span><span class="sxs-lookup"><span data-stu-id="8c83b-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="8c83b-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c83b-159">-Confirm</span></span>
<span data-ttu-id="8c83b-160">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c83b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c83b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c83b-161">-WhatIf</span></span>
<span data-ttu-id="8c83b-162">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c83b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c83b-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c83b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c83b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c83b-164">CommonParameters</span></span>
<span data-ttu-id="8c83b-165">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c83b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c83b-166">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c83b-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c83b-167">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c83b-167">INPUTS</span></span>

### <span data-ttu-id="8c83b-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8c83b-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="8c83b-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c83b-169">OUTPUTS</span></span>

### <span data-ttu-id="8c83b-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8c83b-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="8c83b-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c83b-171">NOTES</span></span>

## <span data-ttu-id="8c83b-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c83b-172">RELATED LINKS</span></span>
