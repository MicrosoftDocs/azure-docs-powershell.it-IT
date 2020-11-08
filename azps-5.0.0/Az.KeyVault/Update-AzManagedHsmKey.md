---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202500"
---
# <span data-ttu-id="68c37-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="68c37-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="68c37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68c37-102">SYNOPSIS</span></span>
<span data-ttu-id="68c37-103">Aggiorna gli attributi di una chiave in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="68c37-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="68c37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68c37-104">SYNTAX</span></span>

### <span data-ttu-id="68c37-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68c37-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68c37-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="68c37-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68c37-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68c37-107">DESCRIPTION</span></span>
<span data-ttu-id="68c37-108">Il cmdlet **Update-AzManagedHsmKey** aggiorna gli attributi modificabili di una chiave in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="68c37-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="68c37-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68c37-109">EXAMPLES</span></span>

### <span data-ttu-id="68c37-110">Esempio 1: modificare una chiave per abilitarla e impostare la data di scadenza e i contrassegni</span><span class="sxs-lookup"><span data-stu-id="68c37-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="68c37-111">Il primo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="68c37-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="68c37-112">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="68c37-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="68c37-113">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="68c37-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="68c37-114">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="68c37-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="68c37-115">Il secondo comando crea una variabile per archiviare i valori di tag di elevata gravità e contabilità.</span><span class="sxs-lookup"><span data-stu-id="68c37-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="68c37-116">Il comando finale modifica una chiave denominata testkey001.</span><span class="sxs-lookup"><span data-stu-id="68c37-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="68c37-117">Il comando Abilita la chiave, imposta la data di scadenza per l'ora archiviata in $Expires e imposta i tag archiviati in $Tags.</span><span class="sxs-lookup"><span data-stu-id="68c37-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="68c37-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68c37-118">PARAMETERS</span></span>

### <span data-ttu-id="68c37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c37-119">-DefaultProfile</span></span>
<span data-ttu-id="68c37-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68c37-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68c37-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="68c37-121">-Enable</span></span>
<span data-ttu-id="68c37-122">Il valore true abilita la chiave e il valore di false disabilita la chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="68c37-123">Se non viene specificato, lo stato abilitato/disabilitato esistente rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="68c37-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="68c37-124">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="68c37-124">-Expires</span></span>
<span data-ttu-id="68c37-125">Ora di scadenza di una chiave in ora UTC.</span><span class="sxs-lookup"><span data-stu-id="68c37-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="68c37-126">Se non viene specificato, il tempo di scadenza esistente della chiave rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="68c37-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="68c37-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="68c37-127">-HsmName</span></span>
<span data-ttu-id="68c37-128">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="68c37-128">HSM name.</span></span> <span data-ttu-id="68c37-129">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="68c37-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="68c37-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68c37-130">-InputObject</span></span>
<span data-ttu-id="68c37-131">Oggetto chiave</span><span class="sxs-lookup"><span data-stu-id="68c37-131">Key object</span></span>

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

### <span data-ttu-id="68c37-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="68c37-132">-KeyOps</span></span>
<span data-ttu-id="68c37-133">Le operazioni che è possibile eseguire con la chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="68c37-134">Se non specificato, le operazioni chiave esistenti della chiave rimarranno invariate.</span><span class="sxs-lookup"><span data-stu-id="68c37-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="68c37-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="68c37-135">-Name</span></span>
<span data-ttu-id="68c37-136">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-136">Key name.</span></span>
<span data-ttu-id="68c37-137">Cmdlet costruisce il nome di dominio completo di una chiave dal nome di HSM gestito, dall'ambiente selezionato e dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68c37-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="68c37-138">-NotBefore</span></span>
<span data-ttu-id="68c37-139">Ora UTC prima della quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="68c37-140">Se non specificato, l'attributo NotBefore esistente della chiave rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="68c37-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="68c37-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68c37-141">-PassThru</span></span>
<span data-ttu-id="68c37-142">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="68c37-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="68c37-143">Se questa opzione è specificata, restituisce l'oggetto bundle Key aggiornato.</span><span class="sxs-lookup"><span data-stu-id="68c37-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="68c37-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="68c37-144">-Tag</span></span>
<span data-ttu-id="68c37-145">Un Hashtable rappresenta i tag chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="68c37-146">Se non viene specificato, i tag esistenti della chiave rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="68c37-146">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="68c37-147">-Versione</span><span class="sxs-lookup"><span data-stu-id="68c37-147">-Version</span></span>
<span data-ttu-id="68c37-148">Versione chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-148">Key version.</span></span>
<span data-ttu-id="68c37-149">Cmdlet costruisce il nome di dominio completo di una chiave da Name HSM gestito, ambiente attualmente selezionato, nome chiave e versione chiave.</span><span class="sxs-lookup"><span data-stu-id="68c37-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="68c37-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68c37-150">-Confirm</span></span>
<span data-ttu-id="68c37-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68c37-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68c37-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68c37-152">-WhatIf</span></span>
<span data-ttu-id="68c37-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68c37-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68c37-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68c37-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68c37-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c37-155">CommonParameters</span></span>
<span data-ttu-id="68c37-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68c37-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c37-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68c37-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c37-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68c37-158">INPUTS</span></span>

### <span data-ttu-id="68c37-159">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="68c37-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="68c37-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68c37-160">OUTPUTS</span></span>

### <span data-ttu-id="68c37-161">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="68c37-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="68c37-162">Note</span><span class="sxs-lookup"><span data-stu-id="68c37-162">NOTES</span></span>

## <span data-ttu-id="68c37-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68c37-163">RELATED LINKS</span></span>

[<span data-ttu-id="68c37-164">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="68c37-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="68c37-165">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="68c37-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="68c37-166">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="68c37-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="68c37-167">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="68c37-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="68c37-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="68c37-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="68c37-169">Ripristinare-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="68c37-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)