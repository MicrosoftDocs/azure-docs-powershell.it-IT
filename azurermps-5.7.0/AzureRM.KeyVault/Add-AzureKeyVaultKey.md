---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 153cd3099b750732e281992e98cdafb173a71276
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518996"
---
# <span data-ttu-id="43719-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43719-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="43719-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43719-102">SYNOPSIS</span></span>
<span data-ttu-id="43719-103">Crea una chiave in un Vault chiave o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43719-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43719-104">SYNTAX</span></span>

### <span data-ttu-id="43719-105">InteractiveCreate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43719-105">InteractiveCreate (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43719-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="43719-106">InteractiveImport</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43719-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="43719-107">InputObjectCreate</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43719-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="43719-108">InputObjectImport</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43719-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43719-109">DESCRIPTION</span></span>
<span data-ttu-id="43719-110">Il cmdlet **Add-AzureKeyVaultKey** crea una chiave in un Vault chiave in Azure Key Vault o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-110">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="43719-111">Questo cmdlet consente di aggiungere chiavi utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="43719-111">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="43719-112">Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="43719-112">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="43719-113">Creare una chiave nel software nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="43719-113">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="43719-114">Importare una chiave da un modulo HSM (hardware Security Module) in HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="43719-114">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="43719-115">Importare una chiave da un file con estensione pfx nel computer.</span><span class="sxs-lookup"><span data-stu-id="43719-115">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="43719-116">Importare una chiave da un file PFX nel computer in moduli di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="43719-116">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="43719-117">Per ognuna di queste operazioni, è possibile specificare gli attributi chiave o accettare le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="43719-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="43719-118">Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel Vault chiave, la chiave originale viene aggiornata con i valori specificati per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-118">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="43719-119">Puoi accedere ai valori precedenti usando l'URI specifico della versione per la versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="43719-120">Per informazioni sulle versioni chiave e sulla struttura URI, vedere [informazioni sulle chiavi andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) nella documentazione dell'API REST di Key Vault.</span><span class="sxs-lookup"><span data-stu-id="43719-120">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="43719-121">Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="43719-121">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="43719-122">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="43719-122">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="43719-123">Come procedura consigliata, eseguire il backup della chiave dopo la creazione o l'aggiornamento usando il cmdlet Backup-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="43719-123">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="43719-124">Non esiste alcuna funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non è recuperabile, a meno che non si disponga di un backup che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="43719-124">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="43719-125">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43719-125">EXAMPLES</span></span>

### <span data-ttu-id="43719-126">Esempio 1: creare una chiave</span><span class="sxs-lookup"><span data-stu-id="43719-126">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="43719-127">Questo comando crea una chiave protetta dal software denominata ITSoftware nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="43719-127">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="43719-128">Esempio 2: creare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="43719-128">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="43719-129">Questo comando crea una chiave con protezione HSM nel Vault chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="43719-129">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="43719-130">Esempio 3: creare una chiave con valori non predefiniti</span><span class="sxs-lookup"><span data-stu-id="43719-130">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="43719-131">Con il primo comando vengono archiviati i valori decrittografati e verificati nella variabile $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="43719-131">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="43719-132">Il secondo comando crea un oggetto **DateTime** , definito in formato UTC, usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="43719-132">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="43719-133">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="43719-133">That object specifies a time two years in the future.</span></span> <span data-ttu-id="43719-134">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="43719-134">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="43719-135">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="43719-135">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="43719-136">Il terzo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="43719-136">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="43719-137">Tale oggetto specifica l'ora UTC corrente.</span><span class="sxs-lookup"><span data-stu-id="43719-137">That object specifies current UTC time.</span></span> <span data-ttu-id="43719-138">Il comando archivia tale data nella variabile $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="43719-138">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="43719-139">Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="43719-139">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="43719-140">Il comando specifica i valori per le operazioni chiave consentite archiviate $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="43719-140">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="43719-141">Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="43719-141">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="43719-142">La nuova chiave è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="43719-142">The new key is disabled.</span></span> <span data-ttu-id="43719-143">Puoi abilitarlo usando il cmdlet **set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="43719-143">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="43719-144">Esempio 4: importare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="43719-144">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="43719-145">Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *filePath* .</span><span class="sxs-lookup"><span data-stu-id="43719-145">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="43719-146">La chiave importata è una chiave con protezione HSM.</span><span class="sxs-lookup"><span data-stu-id="43719-146">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="43719-147">Per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="43719-147">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="43719-148">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="43719-148">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="43719-149">Esempio 5: importare una chiave protetta dal software</span><span class="sxs-lookup"><span data-stu-id="43719-149">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="43719-150">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="43719-150">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="43719-151">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="43719-151">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="43719-152">Il secondo comando crea una password software nel caveau della chiave contoso.</span><span class="sxs-lookup"><span data-stu-id="43719-152">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="43719-153">Il comando specifica la posizione per la chiave e la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="43719-153">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="43719-154">Esempio 6: importare una chiave e assegnare attributi</span><span class="sxs-lookup"><span data-stu-id="43719-154">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="43719-155">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="43719-155">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="43719-156">Il secondo comando crea un oggetto **DateTime** usando il cmdlet **get-date** e quindi archivia tale oggetto nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="43719-156">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="43719-157">Il terzo comando crea la variabile $tags per impostare i contrassegni per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="43719-157">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="43719-158">Il comando finale importa una chiave come chiave HSM dalla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="43719-158">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="43719-159">Il comando specifica la data di scadenza archiviata in $Expires e la password archiviata in $Password e applica i tag archiviati in $tags.</span><span class="sxs-lookup"><span data-stu-id="43719-159">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="43719-160">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43719-160">PARAMETERS</span></span>

### <span data-ttu-id="43719-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43719-161">-DefaultProfile</span></span>
<span data-ttu-id="43719-162">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="43719-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43719-163">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="43719-163">-Destination</span></span>
<span data-ttu-id="43719-164">Specifica se aggiungere la chiave come chiave protetta dal software o con una chiave protetta da HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="43719-164">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="43719-165">I valori validi sono: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="43719-165">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="43719-166">Nota: per usare HSM come destinazione, è necessario disporre di un Vault Key che supporti HSM.</span><span class="sxs-lookup"><span data-stu-id="43719-166">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="43719-167">Per altre informazioni sui livelli di servizio e sulle funzionalità per l'archiviazione delle chiavi di Azure, vedere il [sito Web di Azure Key Vault pricing](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="43719-167">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="43719-168">Questo parametro è obbligatorio quando si crea una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-168">This parameter is required when you create a new key.</span></span> <span data-ttu-id="43719-169">Se si importa una chiave usando il parametro *filePath* , questo parametro è facoltativo:</span><span class="sxs-lookup"><span data-stu-id="43719-169">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="43719-170">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione Byok, questa viene importata come chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="43719-170">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="43719-171">Il cmdlet non può importare la chiave come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="43719-171">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="43719-172">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione pfx, la chiave viene importata come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="43719-172">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InputObjectCreate
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
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43719-173">-Disable</span><span class="sxs-lookup"><span data-stu-id="43719-173">-Disable</span></span>
<span data-ttu-id="43719-174">Indica che la chiave che si sta aggiungendo è impostata su uno stato iniziale di disabled.</span><span class="sxs-lookup"><span data-stu-id="43719-174">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="43719-175">Qualsiasi tentativo di usare la chiave non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="43719-175">Any attempt to use the key will fail.</span></span> <span data-ttu-id="43719-176">Usare questo parametro se si precaricano le chiavi che si desidera abilitare in seguito.</span><span class="sxs-lookup"><span data-stu-id="43719-176">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="43719-177">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="43719-177">-Expires</span></span>
<span data-ttu-id="43719-178">Specifica la data di scadenza, come oggetto **DateTime** , per la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43719-178">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="43719-179">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="43719-179">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="43719-180">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="43719-180">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="43719-181">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="43719-181">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="43719-182">Se non specifichi questo parametro, la chiave non scade.</span><span class="sxs-lookup"><span data-stu-id="43719-182">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="43719-183">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43719-183">-InputObject</span></span>
<span data-ttu-id="43719-184">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="43719-184">Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43719-185">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="43719-185">-KeyFilePassword</span></span>
<span data-ttu-id="43719-186">Specifica una password per il file importato come oggetto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="43719-186">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="43719-187">Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="43719-187">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="43719-188">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="43719-188">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="43719-189">Devi specificare questa password per importare un file con estensione pfx.</span><span class="sxs-lookup"><span data-stu-id="43719-189">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43719-190">-FilePath</span><span class="sxs-lookup"><span data-stu-id="43719-190">-KeyFilePath</span></span>
<span data-ttu-id="43719-191">Specifica il percorso di un file locale che contiene il materiale chiave importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43719-191">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="43719-192">Le estensioni valide per i nomi di file sono Byok e PFX.</span><span class="sxs-lookup"><span data-stu-id="43719-192">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="43719-193">Se il file è un file con estensione Byok, la chiave viene protetta automaticamente da HSM dopo l'importazione e non è possibile eseguire l'override di questa impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="43719-193">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="43719-194">Se il file è un file PFX, la chiave viene automaticamente protetta dal software dopo l'importazione.</span><span class="sxs-lookup"><span data-stu-id="43719-194">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="43719-195">Per eseguire l'override di questo valore predefinito, imposta il parametro di *destinazione* su HSM in modo che la chiave sia protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="43719-195">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="43719-196">Quando specifichi questo parametro, il parametro di *destinazione* è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="43719-196">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43719-197">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="43719-197">-KeyOps</span></span>
<span data-ttu-id="43719-198">Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43719-198">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="43719-199">Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="43719-199">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="43719-200">I valori accettabili per questo parametro sono un elenco delimitato da virgole delle operazioni chiave definite dalla [specifica JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="43719-200">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="43719-201">Crittografare</span><span class="sxs-lookup"><span data-stu-id="43719-201">Encrypt</span></span>
- <span data-ttu-id="43719-202">Decrittografare</span><span class="sxs-lookup"><span data-stu-id="43719-202">Decrypt</span></span>
- <span data-ttu-id="43719-203">A capo</span><span class="sxs-lookup"><span data-stu-id="43719-203">Wrap</span></span>
- <span data-ttu-id="43719-204">Annullare</span><span class="sxs-lookup"><span data-stu-id="43719-204">Unwrap</span></span>
- <span data-ttu-id="43719-205">Segno</span><span class="sxs-lookup"><span data-stu-id="43719-205">Sign</span></span>
- <span data-ttu-id="43719-206">Verificare</span><span class="sxs-lookup"><span data-stu-id="43719-206">Verify</span></span>

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

### <span data-ttu-id="43719-207">-Nome</span><span class="sxs-lookup"><span data-stu-id="43719-207">-Name</span></span>
<span data-ttu-id="43719-208">Specifica il nome della chiave da aggiungere all'archivio della chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-208">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="43719-209">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="43719-209">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="43719-210">Il nome deve essere una stringa da 1 a 63 caratteri di lunghezza che contiene solo 0-9, a-z, A-Z e-(il simbolo del trattino).</span><span class="sxs-lookup"><span data-stu-id="43719-210">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="43719-211">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="43719-211">-NotBefore</span></span>
<span data-ttu-id="43719-212">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-212">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="43719-213">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="43719-213">This parameter uses UTC.</span></span> <span data-ttu-id="43719-214">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="43719-214">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="43719-215">Se non specifichi questo parametro, la chiave può essere usata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="43719-215">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="43719-216">-Tag</span><span class="sxs-lookup"><span data-stu-id="43719-216">-Tag</span></span>
<span data-ttu-id="43719-217">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="43719-217">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="43719-218">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="43719-218">For example:</span></span>

<span data-ttu-id="43719-219">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="43719-219">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="43719-220">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="43719-220">-VaultName</span></span>
<span data-ttu-id="43719-221">Specifica il nome del Vault chiave a cui questo cmdlet aggiunge la chiave.</span><span class="sxs-lookup"><span data-stu-id="43719-221">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="43719-222">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="43719-222">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43719-223">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43719-223">-Confirm</span></span>
<span data-ttu-id="43719-224">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43719-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43719-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43719-225">-WhatIf</span></span>
<span data-ttu-id="43719-226">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43719-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43719-227">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43719-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43719-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43719-228">CommonParameters</span></span>
<span data-ttu-id="43719-229">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43719-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43719-230">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43719-230">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43719-231">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43719-231">INPUTS</span></span>

### <span data-ttu-id="43719-232">Nessuno</span><span class="sxs-lookup"><span data-stu-id="43719-232">None</span></span>
<span data-ttu-id="43719-233">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="43719-233">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43719-234">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43719-234">OUTPUTS</span></span>

### <span data-ttu-id="43719-235">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43719-235">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="43719-236">Note</span><span class="sxs-lookup"><span data-stu-id="43719-236">NOTES</span></span>

## <span data-ttu-id="43719-237">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43719-237">RELATED LINKS</span></span>

[<span data-ttu-id="43719-238">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43719-238">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="43719-239">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43719-239">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="43719-240">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43719-240">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="43719-241">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="43719-241">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
