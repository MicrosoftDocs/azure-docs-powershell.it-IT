---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863065"
---
# <span data-ttu-id="e6055-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e6055-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="e6055-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6055-102">SYNOPSIS</span></span>
<span data-ttu-id="e6055-103">Crea una chiave in un Vault chiave o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="e6055-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6055-104">SYNTAX</span></span>

### <span data-ttu-id="e6055-105">Crea (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6055-105">Create (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6055-106">Importazione</span><span class="sxs-lookup"><span data-stu-id="e6055-106">Import</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6055-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6055-107">DESCRIPTION</span></span>
<span data-ttu-id="e6055-108">Il cmdlet **Add-AzKeyVaultKey** crea una chiave in un Vault chiave in Azure Key Vault o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-108">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="e6055-109">Questo cmdlet consente di aggiungere chiavi utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6055-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="e6055-110">Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e6055-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="e6055-111">Creare una chiave nel software nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e6055-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="e6055-112">Importare una chiave da un modulo HSM (hardware Security Module) in HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e6055-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="e6055-113">Importare una chiave da un file con estensione pfx nel computer.</span><span class="sxs-lookup"><span data-stu-id="e6055-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="e6055-114">Importare una chiave da un file PFX nel computer in moduli di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e6055-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="e6055-115">Per ognuna di queste operazioni, è possibile specificare gli attributi chiave o accettare le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="e6055-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="e6055-116">Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel Vault chiave, la chiave originale viene aggiornata con i valori specificati per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="e6055-117">Puoi accedere ai valori precedenti usando l'URI specifico della versione per la versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="e6055-118">Per informazioni sulle versioni chiave e sulla struttura URI, vedere [informazioni sulle chiavi andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) nella documentazione dell'API REST di Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e6055-118">To learn about key versions and the URI structure, see [About Keys andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="e6055-119">Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6055-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="e6055-120">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="e6055-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="e6055-121">Come procedura consigliata, eseguire il backup della chiave dopo la creazione o l'aggiornamento usando il cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="e6055-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="e6055-122">Non esiste alcuna funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non è recuperabile, a meno che non si disponga di un backup che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="e6055-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="e6055-123">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6055-123">EXAMPLES</span></span>

### <span data-ttu-id="e6055-124">Esempio 1: creare una chiave</span><span class="sxs-lookup"><span data-stu-id="e6055-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="e6055-125">Questo comando crea una chiave protetta dal software denominata ITSoftware nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="e6055-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="e6055-126">Esempio 2: creare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="e6055-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="e6055-127">Questo comando crea una chiave con protezione HSM nel Vault chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="e6055-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="e6055-128">Esempio 3: creare una chiave con valori non predefiniti</span><span class="sxs-lookup"><span data-stu-id="e6055-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="e6055-129">Con il primo comando vengono archiviati i valori decrittografati e verificati nella variabile $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="e6055-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="e6055-130">Il secondo comando crea un oggetto **DateTime** , definito in formato UTC, usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e6055-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e6055-131">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="e6055-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="e6055-132">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="e6055-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="e6055-133">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e6055-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="e6055-134">Il terzo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e6055-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e6055-135">Tale oggetto specifica l'ora UTC corrente.</span><span class="sxs-lookup"><span data-stu-id="e6055-135">That object specifies current UTC time.</span></span> <span data-ttu-id="e6055-136">Il comando archivia tale data nella variabile $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="e6055-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="e6055-137">Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="e6055-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="e6055-138">Il comando specifica i valori per le operazioni chiave consentite archiviate $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="e6055-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="e6055-139">Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="e6055-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="e6055-140">La nuova chiave è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e6055-140">The new key is disabled.</span></span> <span data-ttu-id="e6055-141">Puoi abilitarlo usando il cmdlet **set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="e6055-141">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="e6055-142">Esempio 4: importare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="e6055-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="e6055-143">Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *filePath* .</span><span class="sxs-lookup"><span data-stu-id="e6055-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="e6055-144">La chiave importata è una chiave con protezione HSM.</span><span class="sxs-lookup"><span data-stu-id="e6055-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="e6055-145">Per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6055-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="e6055-146">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="e6055-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="e6055-147">Esempio 5: importare una chiave protetta dal software</span><span class="sxs-lookup"><span data-stu-id="e6055-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="e6055-148">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="e6055-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="e6055-149">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e6055-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="e6055-150">Il secondo comando crea una password software nel caveau della chiave contoso.</span><span class="sxs-lookup"><span data-stu-id="e6055-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="e6055-151">Il comando specifica la posizione per la chiave e la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="e6055-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="e6055-152">Esempio 6: importare una chiave e assegnare attributi</span><span class="sxs-lookup"><span data-stu-id="e6055-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="e6055-153">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="e6055-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="e6055-154">Il secondo comando crea un oggetto **DateTime** usando il cmdlet **get-date** e quindi archivia tale oggetto nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="e6055-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="e6055-155">Il terzo comando crea la variabile $tags per impostare i contrassegni per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="e6055-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="e6055-156">Il comando finale importa una chiave come chiave HSM dalla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="e6055-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="e6055-157">Il comando specifica la data di scadenza archiviata in $Expires e la password archiviata in $Password e applica i tag archiviati in $tags.</span><span class="sxs-lookup"><span data-stu-id="e6055-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="e6055-158">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6055-158">PARAMETERS</span></span>

### <span data-ttu-id="e6055-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6055-159">-DefaultProfile</span></span>
<span data-ttu-id="e6055-160">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e6055-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6055-161">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="e6055-161">-Destination</span></span>
<span data-ttu-id="e6055-162">Specifica se aggiungere la chiave come chiave protetta dal software o con una chiave protetta da HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e6055-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="e6055-163">I valori validi sono: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="e6055-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="e6055-164">Nota: per usare HSM come destinazione, è necessario disporre di un Vault Key che supporti HSM.</span><span class="sxs-lookup"><span data-stu-id="e6055-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="e6055-165">Per altre informazioni sui livelli di servizio e sulle funzionalità per l'archiviazione delle chiavi di Azure, vedere il [sito Web di Azure Key Vault pricing](http://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="e6055-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="e6055-166">Questo parametro è obbligatorio quando si crea una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="e6055-167">Se si importa una chiave usando il parametro *filePath* , questo parametro è facoltativo:</span><span class="sxs-lookup"><span data-stu-id="e6055-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="e6055-168">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione Byok, questa viene importata come chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="e6055-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="e6055-169">Il cmdlet non può importare la chiave come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="e6055-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="e6055-170">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione pfx, la chiave viene importata come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="e6055-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6055-171">-Disable</span><span class="sxs-lookup"><span data-stu-id="e6055-171">-Disable</span></span>
<span data-ttu-id="e6055-172">Indica che la chiave che si sta aggiungendo è impostata su uno stato iniziale di disabled.</span><span class="sxs-lookup"><span data-stu-id="e6055-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="e6055-173">Qualsiasi tentativo di usare la chiave non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="e6055-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="e6055-174">Usare questo parametro se si precaricano le chiavi che si desidera abilitare in seguito.</span><span class="sxs-lookup"><span data-stu-id="e6055-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="e6055-175">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="e6055-175">-Expires</span></span>
<span data-ttu-id="e6055-176">Specifica la data di scadenza, come oggetto **DateTime** , per la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6055-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="e6055-177">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="e6055-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e6055-178">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e6055-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e6055-179">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e6055-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="e6055-180">Se non specifichi questo parametro, la chiave non scade.</span><span class="sxs-lookup"><span data-stu-id="e6055-180">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="e6055-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="e6055-181">-KeyFilePassword</span></span>
<span data-ttu-id="e6055-182">Specifica una password per il file importato come oggetto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="e6055-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="e6055-183">Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="e6055-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="e6055-184">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e6055-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="e6055-185">Devi specificare questa password per importare un file con estensione pfx.</span><span class="sxs-lookup"><span data-stu-id="e6055-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6055-186">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e6055-186">-KeyFilePath</span></span>
<span data-ttu-id="e6055-187">Specifica il percorso di un file locale che contiene il materiale chiave importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6055-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="e6055-188">Le estensioni valide per i nomi di file sono Byok e PFX.</span><span class="sxs-lookup"><span data-stu-id="e6055-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="e6055-189">Se il file è un file con estensione Byok, la chiave viene protetta automaticamente da HSM dopo l'importazione e non è possibile eseguire l'override di questa impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e6055-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="e6055-190">Se il file è un file PFX, la chiave viene automaticamente protetta dal software dopo l'importazione.</span><span class="sxs-lookup"><span data-stu-id="e6055-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="e6055-191">Per eseguire l'override di questo valore predefinito, imposta il parametro di *destinazione* su HSM in modo che la chiave sia protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="e6055-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="e6055-192">Quando specifichi questo parametro, il parametro di *destinazione* è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e6055-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6055-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="e6055-193">-KeyOps</span></span>
<span data-ttu-id="e6055-194">Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6055-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="e6055-195">Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="e6055-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="e6055-196">I valori accettabili per questo parametro sono un elenco delimitato da virgole delle operazioni chiave definite dalla [specifica JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="e6055-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="e6055-197">Crittografare</span><span class="sxs-lookup"><span data-stu-id="e6055-197">Encrypt</span></span>
- <span data-ttu-id="e6055-198">Decrittografare</span><span class="sxs-lookup"><span data-stu-id="e6055-198">Decrypt</span></span>
- <span data-ttu-id="e6055-199">A capo</span><span class="sxs-lookup"><span data-stu-id="e6055-199">Wrap</span></span>
- <span data-ttu-id="e6055-200">Annullare</span><span class="sxs-lookup"><span data-stu-id="e6055-200">Unwrap</span></span>
- <span data-ttu-id="e6055-201">Segno</span><span class="sxs-lookup"><span data-stu-id="e6055-201">Sign</span></span>
- <span data-ttu-id="e6055-202">Verificare</span><span class="sxs-lookup"><span data-stu-id="e6055-202">Verify</span></span>

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

### <span data-ttu-id="e6055-203">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6055-203">-Name</span></span>
<span data-ttu-id="e6055-204">Specifica il nome della chiave da aggiungere all'archivio della chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="e6055-205">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="e6055-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="e6055-206">Il nome deve essere una stringa da 1 a 63 caratteri di lunghezza che contiene solo 0-9, a-z, A-Z e-(il simbolo del trattino).</span><span class="sxs-lookup"><span data-stu-id="e6055-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6055-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="e6055-207">-NotBefore</span></span>
<span data-ttu-id="e6055-208">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="e6055-209">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="e6055-209">This parameter uses UTC.</span></span> <span data-ttu-id="e6055-210">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e6055-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e6055-211">Se non specifichi questo parametro, la chiave può essere usata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e6055-211">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="e6055-212">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6055-212">-Tag</span></span>
<span data-ttu-id="e6055-213">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e6055-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e6055-214">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="e6055-214">For example:</span></span>

<span data-ttu-id="e6055-215">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e6055-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e6055-216">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e6055-216">-VaultName</span></span>
<span data-ttu-id="e6055-217">Specifica il nome del Vault chiave a cui questo cmdlet aggiunge la chiave.</span><span class="sxs-lookup"><span data-stu-id="e6055-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="e6055-218">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="e6055-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="e6055-219">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6055-219">-Confirm</span></span>
<span data-ttu-id="e6055-220">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6055-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6055-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6055-221">-WhatIf</span></span>
<span data-ttu-id="e6055-222">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6055-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6055-223">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6055-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6055-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6055-224">CommonParameters</span></span>
<span data-ttu-id="e6055-225">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6055-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6055-226">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6055-226">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6055-227">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6055-227">INPUTS</span></span>

### <span data-ttu-id="e6055-228">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6055-228">None</span></span>
<span data-ttu-id="e6055-229">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e6055-229">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6055-230">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6055-230">OUTPUTS</span></span>

### <span data-ttu-id="e6055-231">Microsoft. Azure. Commands. Vault. Models. bundle</span><span class="sxs-lookup"><span data-stu-id="e6055-231">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="e6055-232">Note</span><span class="sxs-lookup"><span data-stu-id="e6055-232">NOTES</span></span>

## <span data-ttu-id="e6055-233">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6055-233">RELATED LINKS</span></span>

[<span data-ttu-id="e6055-234">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e6055-234">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="e6055-235">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e6055-235">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="e6055-236">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e6055-236">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="e6055-237">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="e6055-237">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
