---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
ms.openlocfilehash: e7daafc147775b128351a7fa9ffb7b4d807bfe17
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866508"
---
# <span data-ttu-id="083f6-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="083f6-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="083f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="083f6-102">SYNOPSIS</span></span>
<span data-ttu-id="083f6-103">Aggiorna gli attributi di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="083f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="083f6-104">SYNTAX</span></span>

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="083f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="083f6-105">DESCRIPTION</span></span>
<span data-ttu-id="083f6-106">Il cmdlet **set-AzureKeyVaultKeyAttribute** aggiorna gli attributi modificabili di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-106">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="083f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="083f6-107">EXAMPLES</span></span>

### <span data-ttu-id="083f6-108">Esempio 1: modificare una chiave per abilitarla e impostare la data di scadenza e i contrassegni</span><span class="sxs-lookup"><span data-stu-id="083f6-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="083f6-109">Il primo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="083f6-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="083f6-110">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="083f6-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="083f6-111">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="083f6-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="083f6-112">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="083f6-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="083f6-113">Il secondo comando crea una variabile per archiviare i valori di tag di elevata gravità e contabilità.</span><span class="sxs-lookup"><span data-stu-id="083f6-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="083f6-114">Il comando finale modifica una chiave denominata ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="083f6-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="083f6-115">Il comando Abilita la chiave, imposta la data di scadenza per l'ora archiviata in $Expires e imposta i tag archiviati in $Tags.</span><span class="sxs-lookup"><span data-stu-id="083f6-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="083f6-116">Esempio 2: modificare una chiave per eliminare tutti i tag</span><span class="sxs-lookup"><span data-stu-id="083f6-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="083f6-117">Questi comandi eliminano tutti i tag per una versione specifica di una chiave denominata ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="083f6-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="083f6-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="083f6-118">PARAMETERS</span></span>

### <span data-ttu-id="083f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083f6-119">-DefaultProfile</span></span>
<span data-ttu-id="083f6-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="083f6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="083f6-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="083f6-121">-Enable</span></span>
<span data-ttu-id="083f6-122">Specifica se abilitare o disabilitare una chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="083f6-123">Un valore di $True Abilita la chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-123">A value of $True enables the key.</span></span> <span data-ttu-id="083f6-124">Un valore di $False disabilita la chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-124">A value of $False disables the key.</span></span> <span data-ttu-id="083f6-125">Se non specifichi questo parametro, questo cmdlet non modifica lo stato della chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="083f6-126">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="083f6-126">-Expires</span></span>
<span data-ttu-id="083f6-127">Specifica la data di scadenza, come oggetto **DateTime** , per la chiave che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="083f6-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="083f6-128">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="083f6-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="083f6-129">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="083f6-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="083f6-130">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="083f6-130">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="083f6-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="083f6-131">-KeyOps</span></span>
<span data-ttu-id="083f6-132">Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083f6-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="083f6-133">Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="083f6-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="083f6-134">I valori accettabili per questo parametro sono un elenco delimitato da virgole di operazioni chiave definite dalla specifica della chiave Web JSON.</span><span class="sxs-lookup"><span data-stu-id="083f6-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="083f6-135">Questi valori (con distinzione tra maiuscole e minuscole) sono:</span><span class="sxs-lookup"><span data-stu-id="083f6-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="083f6-136">crittografare</span><span class="sxs-lookup"><span data-stu-id="083f6-136">encrypt</span></span>
- <span data-ttu-id="083f6-137">decrittografare</span><span class="sxs-lookup"><span data-stu-id="083f6-137">decrypt</span></span>
- <span data-ttu-id="083f6-138">a capo</span><span class="sxs-lookup"><span data-stu-id="083f6-138">wrap</span></span>
- <span data-ttu-id="083f6-139">annullare</span><span class="sxs-lookup"><span data-stu-id="083f6-139">unwrap</span></span>
- <span data-ttu-id="083f6-140">segno</span><span class="sxs-lookup"><span data-stu-id="083f6-140">sign</span></span>
- <span data-ttu-id="083f6-141">verificare</span><span class="sxs-lookup"><span data-stu-id="083f6-141">verify</span></span>
- <span data-ttu-id="083f6-142">backup</span><span class="sxs-lookup"><span data-stu-id="083f6-142">backup</span></span>
- <span data-ttu-id="083f6-143">ripristinare</span><span class="sxs-lookup"><span data-stu-id="083f6-143">restore</span></span>

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

### <span data-ttu-id="083f6-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="083f6-144">-Name</span></span>
<span data-ttu-id="083f6-145">Specifica il nome della chiave da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="083f6-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="083f6-146">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="083f6-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083f6-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="083f6-147">-NotBefore</span></span>
<span data-ttu-id="083f6-148">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="083f6-149">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="083f6-149">This parameter uses UTC.</span></span>
<span data-ttu-id="083f6-150">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="083f6-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="083f6-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="083f6-151">-PassThru</span></span>
<span data-ttu-id="083f6-152">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="083f6-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="083f6-153">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="083f6-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="083f6-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="083f6-154">-Tag</span></span>
<span data-ttu-id="083f6-155">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="083f6-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="083f6-156">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="083f6-156">For example:</span></span>

<span data-ttu-id="083f6-157">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="083f6-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="083f6-158">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="083f6-158">-VaultName</span></span>
<span data-ttu-id="083f6-159">Specifica il nome del Vault chiave in cui questo cmdlet modifica la chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="083f6-160">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="083f6-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="083f6-161">-Versione</span><span class="sxs-lookup"><span data-stu-id="083f6-161">-Version</span></span>
<span data-ttu-id="083f6-162">Specifica la versione chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-162">Specifies the key version.</span></span>
<span data-ttu-id="083f6-163">Questo cmdlet crea l'FQDN di una chiave in base al nome del Vault chiave, all'ambiente attualmente selezionato, al nome della chiave e alla versione chiave.</span><span class="sxs-lookup"><span data-stu-id="083f6-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="083f6-164">-Confermare</span><span class="sxs-lookup"><span data-stu-id="083f6-164">-Confirm</span></span>
<span data-ttu-id="083f6-165">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083f6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="083f6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="083f6-166">-WhatIf</span></span>
<span data-ttu-id="083f6-167">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="083f6-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="083f6-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="083f6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="083f6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083f6-169">CommonParameters</span></span>
<span data-ttu-id="083f6-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083f6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083f6-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083f6-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083f6-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="083f6-172">INPUTS</span></span>

## <span data-ttu-id="083f6-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="083f6-173">OUTPUTS</span></span>

### <span data-ttu-id="083f6-174">Microsoft. Azure. Commands. Vault. Models. bundle</span><span class="sxs-lookup"><span data-stu-id="083f6-174">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="083f6-175">Note</span><span class="sxs-lookup"><span data-stu-id="083f6-175">NOTES</span></span>

## <span data-ttu-id="083f6-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="083f6-176">RELATED LINKS</span></span>

[<span data-ttu-id="083f6-177">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="083f6-177">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="083f6-178">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="083f6-178">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="083f6-179">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="083f6-179">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
