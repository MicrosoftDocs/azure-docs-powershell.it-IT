---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515668"
---
# <span data-ttu-id="ad4df-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="ad4df-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="ad4df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad4df-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4df-103">Aggiorna gli attributi di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad4df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad4df-104">SYNTAX</span></span>

### <span data-ttu-id="ad4df-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad4df-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad4df-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad4df-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4df-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad4df-107">DESCRIPTION</span></span>
<span data-ttu-id="ad4df-108">Il cmdlet **set-AzureKeyVaultKeyAttribute** aggiorna gli attributi modificabili di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="ad4df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad4df-109">EXAMPLES</span></span>

### <span data-ttu-id="ad4df-110">Esempio 1: modificare una chiave per abilitarla e impostare la data di scadenza e i contrassegni</span><span class="sxs-lookup"><span data-stu-id="ad4df-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="ad4df-111">Il primo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="ad4df-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ad4df-112">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="ad4df-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="ad4df-113">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="ad4df-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="ad4df-114">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ad4df-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="ad4df-115">Il secondo comando crea una variabile per archiviare i valori di tag di elevata gravità e contabilità.</span><span class="sxs-lookup"><span data-stu-id="ad4df-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="ad4df-116">Il comando finale modifica una chiave denominata ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="ad4df-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="ad4df-117">Il comando Abilita la chiave, imposta la data di scadenza per l'ora archiviata in $Expires e imposta i tag archiviati in $Tags.</span><span class="sxs-lookup"><span data-stu-id="ad4df-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="ad4df-118">Esempio 2: modificare una chiave per eliminare tutti i tag</span><span class="sxs-lookup"><span data-stu-id="ad4df-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="ad4df-119">Questi comandi eliminano tutti i tag per una versione specifica di una chiave denominata ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="ad4df-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="ad4df-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad4df-120">PARAMETERS</span></span>

### <span data-ttu-id="ad4df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4df-121">-DefaultProfile</span></span>
<span data-ttu-id="ad4df-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad4df-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad4df-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="ad4df-123">-Enable</span></span>
<span data-ttu-id="ad4df-124">Specifica se abilitare o disabilitare una chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="ad4df-125">Un valore di $True Abilita la chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-125">A value of $True enables the key.</span></span> <span data-ttu-id="ad4df-126">Un valore di $False disabilita la chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-126">A value of $False disables the key.</span></span> <span data-ttu-id="ad4df-127">Se non specifichi questo parametro, questo cmdlet non modifica lo stato della chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="ad4df-128">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="ad4df-128">-Expires</span></span>
<span data-ttu-id="ad4df-129">Specifica la data di scadenza, come oggetto **DateTime** , per la chiave che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="ad4df-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="ad4df-130">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="ad4df-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="ad4df-131">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="ad4df-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ad4df-132">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ad4df-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="ad4df-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad4df-133">-InputObject</span></span>
<span data-ttu-id="ad4df-134">Oggetto chiave</span><span class="sxs-lookup"><span data-stu-id="ad4df-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4df-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="ad4df-135">-KeyOps</span></span>
<span data-ttu-id="ad4df-136">Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4df-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="ad4df-137">Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="ad4df-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="ad4df-138">I valori accettabili per questo parametro sono un elenco delimitato da virgole di operazioni chiave definite dalla specifica della chiave Web JSON.</span><span class="sxs-lookup"><span data-stu-id="ad4df-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="ad4df-139">Questi valori (con distinzione tra maiuscole e minuscole) sono:</span><span class="sxs-lookup"><span data-stu-id="ad4df-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="ad4df-140">crittografare</span><span class="sxs-lookup"><span data-stu-id="ad4df-140">encrypt</span></span>
- <span data-ttu-id="ad4df-141">decrittografare</span><span class="sxs-lookup"><span data-stu-id="ad4df-141">decrypt</span></span>
- <span data-ttu-id="ad4df-142">a capo</span><span class="sxs-lookup"><span data-stu-id="ad4df-142">wrap</span></span>
- <span data-ttu-id="ad4df-143">annullare</span><span class="sxs-lookup"><span data-stu-id="ad4df-143">unwrap</span></span>
- <span data-ttu-id="ad4df-144">segno</span><span class="sxs-lookup"><span data-stu-id="ad4df-144">sign</span></span>
- <span data-ttu-id="ad4df-145">verificare</span><span class="sxs-lookup"><span data-stu-id="ad4df-145">verify</span></span>
- <span data-ttu-id="ad4df-146">backup</span><span class="sxs-lookup"><span data-stu-id="ad4df-146">backup</span></span>
- <span data-ttu-id="ad4df-147">ripristinare</span><span class="sxs-lookup"><span data-stu-id="ad4df-147">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4df-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad4df-148">-Name</span></span>
<span data-ttu-id="ad4df-149">Specifica il nome della chiave da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ad4df-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="ad4df-150">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="ad4df-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4df-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ad4df-151">-NotBefore</span></span>
<span data-ttu-id="ad4df-152">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="ad4df-153">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="ad4df-153">This parameter uses UTC.</span></span>
<span data-ttu-id="ad4df-154">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="ad4df-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="ad4df-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad4df-155">-PassThru</span></span>
<span data-ttu-id="ad4df-156">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ad4df-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ad4df-157">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ad4df-157">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad4df-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad4df-158">-Tag</span></span>
<span data-ttu-id="ad4df-159">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ad4df-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ad4df-160">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="ad4df-160">For example:</span></span>

<span data-ttu-id="ad4df-161">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ad4df-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ad4df-162">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ad4df-162">-VaultName</span></span>
<span data-ttu-id="ad4df-163">Specifica il nome del Vault chiave in cui questo cmdlet modifica la chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="ad4df-164">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="ad4df-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="ad4df-165">-Versione</span><span class="sxs-lookup"><span data-stu-id="ad4df-165">-Version</span></span>
<span data-ttu-id="ad4df-166">Specifica la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-166">Specifies the key version.</span></span>
<span data-ttu-id="ad4df-167">Questo cmdlet crea l'FQDN di una chiave in base al nome del Vault chiave, all'ambiente attualmente selezionato, al nome della chiave e alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="ad4df-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4df-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad4df-168">-Confirm</span></span>
<span data-ttu-id="ad4df-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4df-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4df-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4df-170">-WhatIf</span></span>
<span data-ttu-id="ad4df-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad4df-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad4df-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad4df-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4df-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4df-173">CommonParameters</span></span>
<span data-ttu-id="ad4df-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4df-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4df-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4df-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4df-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad4df-176">INPUTS</span></span>

### <span data-ttu-id="ad4df-177">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ad4df-177">None</span></span>
<span data-ttu-id="ad4df-178">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ad4df-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad4df-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad4df-179">OUTPUTS</span></span>

### <span data-ttu-id="ad4df-180">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad4df-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="ad4df-181">Note</span><span class="sxs-lookup"><span data-stu-id="ad4df-181">NOTES</span></span>

## <span data-ttu-id="ad4df-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad4df-182">RELATED LINKS</span></span>

[<span data-ttu-id="ad4df-183">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad4df-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="ad4df-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad4df-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="ad4df-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ad4df-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
