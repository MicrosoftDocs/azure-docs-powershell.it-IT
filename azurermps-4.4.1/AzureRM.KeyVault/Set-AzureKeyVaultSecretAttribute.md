---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://go.microsoft.com/fwlink/?LinkId=690305
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: 9d9bd8a14b3a24d6001a7f1c2663b05a1e427f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521211"
---
# <span data-ttu-id="9a509-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="9a509-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="9a509-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a509-102">SYNOPSIS</span></span>
<span data-ttu-id="9a509-103">Aggiorna gli attributi di un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="9a509-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a509-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a509-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a509-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a509-105">DESCRIPTION</span></span>
<span data-ttu-id="9a509-106">Il cmdlet **set-AzureKeyVaultSecretAttribute** aggiorna gli attributi modificabili di un segreto in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="9a509-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="9a509-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a509-107">EXAMPLES</span></span>

### <span data-ttu-id="9a509-108">Esempio 1: modificare gli attributi di un segreto</span><span class="sxs-lookup"><span data-stu-id="9a509-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="9a509-109">I primi quattro comandi definiscono gli attributi per la data di scadenza, la data NotBefore, i tag e il tipo di contesto e archiviano gli attributi nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="9a509-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="9a509-110">Il comando finale modifica gli attributi per il segreto denominato HR nel Vault chiave denominato ContosoVault, usando le variabili archiviate.</span><span class="sxs-lookup"><span data-stu-id="9a509-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="9a509-111">Esempio 2: eliminare i tag e il tipo di contenuto per un segreto</span><span class="sxs-lookup"><span data-stu-id="9a509-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="9a509-112">Questo comando Elimina i tag e il tipo di contenuto per la versione specificata del segreto denominato HR nel Vault chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9a509-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="9a509-113">Esempio 3: disabilitare la versione corrente dei segreti il cui nome inizia con esso</span><span class="sxs-lookup"><span data-stu-id="9a509-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="9a509-114">Il primo comando Archivia il valore stringa Contoso nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="9a509-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="9a509-115">Il secondo comando Archivia il valore stringa nella variabile $Prefix.</span><span class="sxs-lookup"><span data-stu-id="9a509-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="9a509-116">Il terzo comando usa il cmdlet Get-AzureKeyVaultSecret per ottenere i segreti nell'archivio chiavi specificato, quindi passa questi segreti al cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="9a509-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="9a509-117">Il cmdlet **Where-Object** filtra i segreti per i nomi che iniziano con i caratteri.</span><span class="sxs-lookup"><span data-stu-id="9a509-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="9a509-118">Il comando consente di eseguire il piping dei segreti che corrispondono al filtro al cmdlet Set-AzureKeyVaultSecretAttribute, che li Disabilita.</span><span class="sxs-lookup"><span data-stu-id="9a509-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="9a509-119">Esempio 4: impostare ContentType per tutte le versioni di un segreto</span><span class="sxs-lookup"><span data-stu-id="9a509-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="9a509-120">I primi tre comandi definiscono le variabili di stringa da usare per i parametri *VAULTNAME* , *Name* e *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="9a509-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="9a509-121">Il quarto comando usa il cmdlet Get-AzureKeyVaultKey per ottenere le chiavi specificate e convoglia le chiavi al cmdlet Set-AzureKeyVaultSecretAttribute per impostare il tipo di contenuto su XML.</span><span class="sxs-lookup"><span data-stu-id="9a509-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="9a509-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a509-122">PARAMETERS</span></span>

### <span data-ttu-id="9a509-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a509-123">-Confirm</span></span>
<span data-ttu-id="9a509-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a509-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a509-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="9a509-125">-ContentType</span></span>
<span data-ttu-id="9a509-126">Specifica il tipo di contenuto di un segreto.</span><span class="sxs-lookup"><span data-stu-id="9a509-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="9a509-127">Se non specifichi questo parametro, il tipo di contenuto del segreto corrente non cambia.</span><span class="sxs-lookup"><span data-stu-id="9a509-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="9a509-128">Per rimuovere il tipo di contenuto esistente, specificare una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="9a509-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a509-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="9a509-129">-Enable</span></span>
<span data-ttu-id="9a509-130">Indica se abilitare un segreto.</span><span class="sxs-lookup"><span data-stu-id="9a509-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="9a509-131">Specificare $False per disabilitare un segreto o $True per abilitare un segreto.</span><span class="sxs-lookup"><span data-stu-id="9a509-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="9a509-132">Se non specifichi questo parametro, non c'è alcun cambiamento nello stato abilitato o disabilitato del segreto corrente.</span><span class="sxs-lookup"><span data-stu-id="9a509-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="9a509-133">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="9a509-133">-Expires</span></span>
<span data-ttu-id="9a509-134">Specifica la data e l'ora di scadenza di un segreto.</span><span class="sxs-lookup"><span data-stu-id="9a509-134">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a509-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a509-135">-Name</span></span>
<span data-ttu-id="9a509-136">Specifica il nome di un segreto.</span><span class="sxs-lookup"><span data-stu-id="9a509-136">Specifies the name of a secret.</span></span> <span data-ttu-id="9a509-137">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="9a509-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="9a509-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="9a509-138">-NotBefore</span></span>
<span data-ttu-id="9a509-139">Specifica l'ora UTC (Coordinated Universal Time) prima della quale non è possibile usare il segreto.</span><span class="sxs-lookup"><span data-stu-id="9a509-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="9a509-140">Se non specifichi questo parametro, non c'è alcuna modifica all'attributo NotBefore del segreto corrente.</span><span class="sxs-lookup"><span data-stu-id="9a509-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a509-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a509-141">-PassThru</span></span>
<span data-ttu-id="9a509-142">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9a509-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a509-143">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9a509-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a509-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a509-144">-Tag</span></span>
<span data-ttu-id="9a509-145">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9a509-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9a509-146">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="9a509-146">For example:</span></span>

<span data-ttu-id="9a509-147">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9a509-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a509-148">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="9a509-148">-VaultName</span></span>
<span data-ttu-id="9a509-149">Specifica il nome del Vault della chiave da modificare.</span><span class="sxs-lookup"><span data-stu-id="9a509-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="9a509-150">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="9a509-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="9a509-151">-Versione</span><span class="sxs-lookup"><span data-stu-id="9a509-151">-Version</span></span>
<span data-ttu-id="9a509-152">Specifica la versione di un segreto.</span><span class="sxs-lookup"><span data-stu-id="9a509-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="9a509-153">Questo cmdlet crea l'FQDN di un segreto in base al nome del Vault chiave, all'ambiente selezionato, al nome segreto e alla versione segreta.</span><span class="sxs-lookup"><span data-stu-id="9a509-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a509-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a509-154">-WhatIf</span></span>
<span data-ttu-id="9a509-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a509-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a509-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a509-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a509-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a509-157">-DefaultProfile</span></span>
<span data-ttu-id="9a509-158">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a509-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a509-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a509-159">CommonParameters</span></span>
<span data-ttu-id="9a509-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a509-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a509-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a509-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a509-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a509-162">INPUTS</span></span>

## <span data-ttu-id="9a509-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a509-163">OUTPUTS</span></span>

### <span data-ttu-id="9a509-164">Microsoft. Azure. Commands. Vault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="9a509-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="9a509-165">Restituisce l'oggetto Microsoft. Azure. Commands. DataVault. Models. Secret se viene specificato PassThru.</span><span class="sxs-lookup"><span data-stu-id="9a509-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="9a509-166">In caso contrario, restituisce Nothing.</span><span class="sxs-lookup"><span data-stu-id="9a509-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="9a509-167">Note</span><span class="sxs-lookup"><span data-stu-id="9a509-167">NOTES</span></span>

## <span data-ttu-id="9a509-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a509-168">RELATED LINKS</span></span>

[<span data-ttu-id="9a509-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9a509-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="9a509-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9a509-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="9a509-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9a509-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
