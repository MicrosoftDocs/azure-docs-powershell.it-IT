---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476174"
---
# <span data-ttu-id="7acdb-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7acdb-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="7acdb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7acdb-102">SYNOPSIS</span></span>
<span data-ttu-id="7acdb-103">Aggiorna gli attributi di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="7acdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7acdb-104">SYNTAX</span></span>

### <span data-ttu-id="7acdb-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7acdb-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7acdb-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="7acdb-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7acdb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7acdb-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7acdb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7acdb-108">DESCRIPTION</span></span>
<span data-ttu-id="7acdb-109">Il cmdlet **Update-AzKeyVaultKey** aggiorna gli attributi modificabili di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="7acdb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7acdb-110">EXAMPLES</span></span>

### <span data-ttu-id="7acdb-111">Esempio 1: modificare una chiave per abilitarla e impostare la data di scadenza e i contrassegni</span><span class="sxs-lookup"><span data-stu-id="7acdb-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="7acdb-112">Il primo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="7acdb-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="7acdb-113">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="7acdb-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="7acdb-114">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="7acdb-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="7acdb-115">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7acdb-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="7acdb-116">Il secondo comando crea una variabile per archiviare i valori di tag di elevata gravità e contabilità.</span><span class="sxs-lookup"><span data-stu-id="7acdb-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="7acdb-117">Il comando finale modifica una chiave denominata ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="7acdb-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="7acdb-118">Il comando Abilita la chiave, imposta la data di scadenza per l'ora archiviata in $Expires e imposta i tag archiviati in $Tags.</span><span class="sxs-lookup"><span data-stu-id="7acdb-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="7acdb-119">Esempio 2: modificare una chiave per eliminare tutti i tag</span><span class="sxs-lookup"><span data-stu-id="7acdb-119">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="7acdb-120">Questi comandi eliminano tutti i tag per una versione specifica di una chiave denominata ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="7acdb-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="7acdb-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7acdb-121">PARAMETERS</span></span>

### <span data-ttu-id="7acdb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acdb-122">-DefaultProfile</span></span>
<span data-ttu-id="7acdb-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7acdb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7acdb-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="7acdb-124">-Enable</span></span>
<span data-ttu-id="7acdb-125">Il valore true abilita la chiave e il valore di false disabilita la chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="7acdb-126">Se non viene specificato, lo stato abilitato/disabilitato esistente rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="7acdb-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="7acdb-127">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="7acdb-127">-Expires</span></span>
<span data-ttu-id="7acdb-128">Ora di scadenza di una chiave in ora UTC.</span><span class="sxs-lookup"><span data-stu-id="7acdb-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="7acdb-129">Se non viene specificato, il tempo di scadenza esistente della chiave rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="7acdb-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="7acdb-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7acdb-130">-HsmName</span></span>
<span data-ttu-id="7acdb-131">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="7acdb-131">HSM name.</span></span> <span data-ttu-id="7acdb-132">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="7acdb-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acdb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7acdb-133">-InputObject</span></span>
<span data-ttu-id="7acdb-134">Oggetto chiave</span><span class="sxs-lookup"><span data-stu-id="7acdb-134">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7acdb-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="7acdb-135">-KeyOps</span></span>
<span data-ttu-id="7acdb-136">Le operazioni che è possibile eseguire con la chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="7acdb-137">Se non specificato, le operazioni chiave esistenti della chiave rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="7acdb-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acdb-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="7acdb-138">-Name</span></span>
<span data-ttu-id="7acdb-139">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-139">Key name.</span></span>
<span data-ttu-id="7acdb-140">Cmdlet costruisce il nome di dominio completo di una chiave dal nome del Vault, l'ambiente selezionato e il cognome della chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acdb-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="7acdb-141">-NotBefore</span></span>
<span data-ttu-id="7acdb-142">Ora UTC prima della quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="7acdb-143">Se non specificato, l'attributo NotBefore esistente della chiave rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="7acdb-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="7acdb-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7acdb-144">-PassThru</span></span>
<span data-ttu-id="7acdb-145">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7acdb-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7acdb-146">Se questa opzione è specificata, restituisce l'oggetto bundle Key aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7acdb-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="7acdb-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="7acdb-147">-Tag</span></span>
<span data-ttu-id="7acdb-148">Un Hashtable rappresenta i tag chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="7acdb-149">Se non viene specificato, i tag esistenti della chiave rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="7acdb-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="7acdb-150">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="7acdb-150">-VaultName</span></span>
<span data-ttu-id="7acdb-151">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="7acdb-151">Vault name.</span></span>
<span data-ttu-id="7acdb-152">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="7acdb-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7acdb-153">-Versione</span><span class="sxs-lookup"><span data-stu-id="7acdb-153">-Version</span></span>
<span data-ttu-id="7acdb-154">Versione chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-154">Key version.</span></span>
<span data-ttu-id="7acdb-155">Cmdlet crea l'FQDN di una chiave dal nome del Vault, l'ambiente attualmente selezionato, il nome della chiave e la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="7acdb-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7acdb-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7acdb-156">-Confirm</span></span>
<span data-ttu-id="7acdb-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7acdb-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7acdb-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7acdb-158">-WhatIf</span></span>
<span data-ttu-id="7acdb-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7acdb-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7acdb-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7acdb-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7acdb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acdb-161">CommonParameters</span></span>
<span data-ttu-id="7acdb-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acdb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acdb-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7acdb-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acdb-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7acdb-164">INPUTS</span></span>

### <span data-ttu-id="7acdb-165">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7acdb-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="7acdb-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7acdb-166">OUTPUTS</span></span>

### <span data-ttu-id="7acdb-167">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7acdb-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="7acdb-168">Note</span><span class="sxs-lookup"><span data-stu-id="7acdb-168">NOTES</span></span>

## <span data-ttu-id="7acdb-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7acdb-169">RELATED LINKS</span></span>
