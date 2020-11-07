---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688167"
---
# <span data-ttu-id="6ce30-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="6ce30-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="6ce30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ce30-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce30-103">Aggiorna gli attributi di un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="6ce30-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ce30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ce30-104">SYNTAX</span></span>

### <span data-ttu-id="6ce30-105">Predefinita</span><span class="sxs-lookup"><span data-stu-id="6ce30-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce30-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ce30-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce30-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ce30-107">DESCRIPTION</span></span>
<span data-ttu-id="6ce30-108">Il cmdlet **set-AzureKeyVaultSecretAttribute** aggiorna gli attributi modificabili di un segreto in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6ce30-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="6ce30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ce30-109">EXAMPLES</span></span>

### <span data-ttu-id="6ce30-110">Esempio 1: modificare gli attributi di un segreto</span><span class="sxs-lookup"><span data-stu-id="6ce30-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="6ce30-111">I primi quattro comandi definiscono gli attributi per la data di scadenza, la data NotBefore, i tag e il tipo di contesto e archiviano gli attributi nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="6ce30-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="6ce30-112">Il comando finale modifica gli attributi per il segreto denominato HR nel Vault chiave denominato ContosoVault, usando le variabili archiviate.</span><span class="sxs-lookup"><span data-stu-id="6ce30-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="6ce30-113">Esempio 2: eliminare i tag e il tipo di contenuto per un segreto</span><span class="sxs-lookup"><span data-stu-id="6ce30-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="6ce30-114">Questo comando Elimina i tag e il tipo di contenuto per la versione specificata del segreto denominato HR nel Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="6ce30-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="6ce30-115">Esempio 3: disabilitare la versione corrente dei segreti il cui nome inizia con esso</span><span class="sxs-lookup"><span data-stu-id="6ce30-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="6ce30-116">Il primo comando Archivia il valore stringa Contoso nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="6ce30-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="6ce30-117">Il secondo comando Archivia il valore stringa nella variabile $Prefix.</span><span class="sxs-lookup"><span data-stu-id="6ce30-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="6ce30-118">Il terzo comando usa il cmdlet Get-AzureKeyVaultSecret per ottenere i segreti nell'archivio chiavi specificato, quindi passa questi segreti al cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="6ce30-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="6ce30-119">Il cmdlet **Where-Object** filtra i segreti per i nomi che iniziano con i caratteri.</span><span class="sxs-lookup"><span data-stu-id="6ce30-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="6ce30-120">Il comando consente di eseguire il piping dei segreti che corrispondono al filtro al cmdlet Set-AzureKeyVaultSecretAttribute, che li Disabilita.</span><span class="sxs-lookup"><span data-stu-id="6ce30-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="6ce30-121">Esempio 4: impostare ContentType per tutte le versioni di un segreto</span><span class="sxs-lookup"><span data-stu-id="6ce30-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="6ce30-122">I primi tre comandi definiscono le variabili di stringa da usare per i parametri *VAULTNAME* , *Name* e *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="6ce30-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="6ce30-123">Il quarto comando usa il cmdlet Get-AzureKeyVaultKey per ottenere le chiavi specificate e convoglia le chiavi al cmdlet Set-AzureKeyVaultSecretAttribute per impostare il tipo di contenuto su XML.</span><span class="sxs-lookup"><span data-stu-id="6ce30-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="6ce30-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ce30-124">PARAMETERS</span></span>

### <span data-ttu-id="6ce30-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6ce30-125">-ContentType</span></span>
<span data-ttu-id="6ce30-126">Specifica il tipo di contenuto di un segreto.</span><span class="sxs-lookup"><span data-stu-id="6ce30-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="6ce30-127">Se non specifichi questo parametro, il tipo di contenuto del segreto corrente non cambia.</span><span class="sxs-lookup"><span data-stu-id="6ce30-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="6ce30-128">Per rimuovere il tipo di contenuto esistente, specificare una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="6ce30-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce30-129">-DefaultProfile</span></span>
<span data-ttu-id="6ce30-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6ce30-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ce30-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="6ce30-131">-Enable</span></span>
<span data-ttu-id="6ce30-132">Indica se abilitare un segreto.</span><span class="sxs-lookup"><span data-stu-id="6ce30-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="6ce30-133">Specificare $False per disabilitare un segreto o $True per abilitare un segreto.</span><span class="sxs-lookup"><span data-stu-id="6ce30-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="6ce30-134">Se non specifichi questo parametro, non c'è alcun cambiamento nello stato abilitato o disabilitato del segreto corrente.</span><span class="sxs-lookup"><span data-stu-id="6ce30-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-135">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="6ce30-135">-Expires</span></span>
<span data-ttu-id="6ce30-136">Specifica la data e l'ora di scadenza di un segreto.</span><span class="sxs-lookup"><span data-stu-id="6ce30-136">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ce30-137">-InputObject</span></span>
<span data-ttu-id="6ce30-138">Oggetto segreto</span><span class="sxs-lookup"><span data-stu-id="6ce30-138">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ce30-139">-Name</span></span>
<span data-ttu-id="6ce30-140">Specifica il nome di un segreto.</span><span class="sxs-lookup"><span data-stu-id="6ce30-140">Specifies the name of a secret.</span></span> <span data-ttu-id="6ce30-141">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="6ce30-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="6ce30-142">-NotBefore</span></span>
<span data-ttu-id="6ce30-143">Specifica l'ora UTC (Coordinated Universal Time) prima della quale non è possibile usare il segreto.</span><span class="sxs-lookup"><span data-stu-id="6ce30-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="6ce30-144">Se non specifichi questo parametro, non c'è alcuna modifica all'attributo NotBefore del segreto corrente.</span><span class="sxs-lookup"><span data-stu-id="6ce30-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ce30-145">-PassThru</span></span>
<span data-ttu-id="6ce30-146">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="6ce30-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6ce30-147">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6ce30-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ce30-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ce30-148">-Tag</span></span>
<span data-ttu-id="6ce30-149">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6ce30-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ce30-150">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="6ce30-150">For example:</span></span>

<span data-ttu-id="6ce30-151">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6ce30-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-152">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="6ce30-152">-VaultName</span></span>
<span data-ttu-id="6ce30-153">Specifica il nome del Vault della chiave da modificare.</span><span class="sxs-lookup"><span data-stu-id="6ce30-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="6ce30-154">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="6ce30-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-155">-Versione</span><span class="sxs-lookup"><span data-stu-id="6ce30-155">-Version</span></span>
<span data-ttu-id="6ce30-156">Specifica la versione di un segreto.</span><span class="sxs-lookup"><span data-stu-id="6ce30-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="6ce30-157">Questo cmdlet crea l'FQDN di un segreto in base al nome del Vault chiave, all'ambiente selezionato, al nome segreto e alla versione segreta.</span><span class="sxs-lookup"><span data-stu-id="6ce30-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ce30-158">-Confirm</span></span>
<span data-ttu-id="6ce30-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ce30-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce30-160">-WhatIf</span></span>
<span data-ttu-id="6ce30-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ce30-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce30-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ce30-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce30-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce30-163">CommonParameters</span></span>
<span data-ttu-id="6ce30-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce30-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce30-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce30-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce30-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ce30-166">INPUTS</span></span>

### <span data-ttu-id="6ce30-167">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6ce30-167">None</span></span>
<span data-ttu-id="6ce30-168">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6ce30-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ce30-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ce30-169">OUTPUTS</span></span>

### <span data-ttu-id="6ce30-170">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ce30-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="6ce30-171">Restituisce l'oggetto Microsoft. Azure. Commands. DataVault. Models. Secret se viene specificato PassThru.</span><span class="sxs-lookup"><span data-stu-id="6ce30-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="6ce30-172">In caso contrario, restituisce Nothing.</span><span class="sxs-lookup"><span data-stu-id="6ce30-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="6ce30-173">Note</span><span class="sxs-lookup"><span data-stu-id="6ce30-173">NOTES</span></span>

## <span data-ttu-id="6ce30-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ce30-174">RELATED LINKS</span></span>

[<span data-ttu-id="6ce30-175">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6ce30-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="6ce30-176">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ce30-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="6ce30-177">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ce30-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
