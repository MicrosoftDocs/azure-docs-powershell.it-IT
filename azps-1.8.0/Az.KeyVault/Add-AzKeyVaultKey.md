---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: f7447725e63634642f285b6a796a2b59b4d1d301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835799"
---
# <span data-ttu-id="108c6-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="108c6-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="108c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="108c6-102">SYNOPSIS</span></span>
<span data-ttu-id="108c6-103">Crea una chiave in un Vault chiave o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="108c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="108c6-104">SYNTAX</span></span>

### <span data-ttu-id="108c6-105">InteractiveCreate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="108c6-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108c6-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="108c6-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108c6-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="108c6-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108c6-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="108c6-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108c6-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="108c6-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="108c6-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="108c6-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="108c6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="108c6-111">DESCRIPTION</span></span>
<span data-ttu-id="108c6-112">Il cmdlet **Add-AzKeyVaultKey** crea una chiave in un Vault chiave in Azure Key Vault o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="108c6-113">Questo cmdlet consente di aggiungere chiavi utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="108c6-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="108c6-114">Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="108c6-115">Creare una chiave nel software nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="108c6-116">Importare una chiave da un modulo HSM (hardware Security Module) in HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="108c6-117">Importare una chiave da un file con estensione pfx nel computer.</span><span class="sxs-lookup"><span data-stu-id="108c6-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="108c6-118">Importare una chiave da un file PFX nel computer in moduli di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="108c6-119">Per ognuna di queste operazioni, è possibile specificare gli attributi chiave o accettare le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="108c6-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="108c6-120">Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel Vault chiave, la chiave originale viene aggiornata con i valori specificati per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="108c6-121">Puoi accedere ai valori precedenti usando l'URI specifico della versione per la versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="108c6-122">Per informazioni sulle versioni chiave e sulla struttura URI, vedere [informazioni sulle chiavi e i segreti](https://go.microsoft.com/fwlink/?linkid=518560) nella documentazione dell'API REST di Key Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-122">To learn about key versions and the URI structure, see [About Keys and Secrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="108c6-123">Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="108c6-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="108c6-124">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="108c6-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="108c6-125">Come procedura consigliata, eseguire il backup della chiave dopo la creazione o l'aggiornamento usando il cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="108c6-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="108c6-126">Non esiste alcuna funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non è recuperabile, a meno che non si disponga di un backup che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="108c6-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="108c6-127">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="108c6-127">EXAMPLES</span></span>

### <span data-ttu-id="108c6-128">Esempio 1: creare una chiave</span><span class="sxs-lookup"><span data-stu-id="108c6-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="108c6-129">Questo comando crea una chiave protetta dal software denominata ITSoftware nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="108c6-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="108c6-130">Esempio 2: creare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="108c6-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="108c6-131">Questo comando crea una chiave con protezione HSM nel Vault chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="108c6-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="108c6-132">Esempio 3: creare una chiave con valori non predefiniti</span><span class="sxs-lookup"><span data-stu-id="108c6-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="108c6-133">Con il primo comando vengono archiviati i valori decrittografati e verificati nella variabile $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="108c6-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="108c6-134">Il secondo comando crea un oggetto **DateTime** , definito in formato UTC, usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="108c6-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="108c6-135">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="108c6-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="108c6-136">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="108c6-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="108c6-137">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="108c6-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="108c6-138">Il terzo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="108c6-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="108c6-139">Tale oggetto specifica l'ora UTC corrente.</span><span class="sxs-lookup"><span data-stu-id="108c6-139">That object specifies current UTC time.</span></span> <span data-ttu-id="108c6-140">Il comando archivia tale data nella variabile $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="108c6-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="108c6-141">Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="108c6-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="108c6-142">Il comando specifica i valori per le operazioni chiave consentite archiviate $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="108c6-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="108c6-143">Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="108c6-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="108c6-144">La nuova chiave è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="108c6-144">The new key is disabled.</span></span> <span data-ttu-id="108c6-145">Puoi abilitarlo usando il cmdlet **set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="108c6-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="108c6-146">Esempio 4: importare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="108c6-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="108c6-147">Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *filePath* .</span><span class="sxs-lookup"><span data-stu-id="108c6-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="108c6-148">La chiave importata è una chiave con protezione HSM.</span><span class="sxs-lookup"><span data-stu-id="108c6-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="108c6-149">Per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="108c6-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="108c6-150">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="108c6-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="108c6-151">Esempio 5: importare una chiave protetta dal software</span><span class="sxs-lookup"><span data-stu-id="108c6-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="108c6-152">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="108c6-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="108c6-153">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="108c6-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="108c6-154">Il secondo comando crea una password software nel caveau della chiave contoso.</span><span class="sxs-lookup"><span data-stu-id="108c6-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="108c6-155">Il comando specifica la posizione per la chiave e la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="108c6-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="108c6-156">Esempio 6: importare una chiave e assegnare attributi</span><span class="sxs-lookup"><span data-stu-id="108c6-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="108c6-157">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="108c6-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="108c6-158">Il secondo comando crea un oggetto **DateTime** usando il cmdlet **get-date** e quindi archivia tale oggetto nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="108c6-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="108c6-159">Il terzo comando crea la variabile $tags per impostare i contrassegni per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="108c6-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="108c6-160">Il comando finale importa una chiave come chiave HSM dalla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="108c6-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="108c6-161">Il comando specifica la data di scadenza archiviata in $Expires e la password archiviata in $Password e applica i tag archiviati in $tags.</span><span class="sxs-lookup"><span data-stu-id="108c6-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="108c6-162">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="108c6-162">PARAMETERS</span></span>

### <span data-ttu-id="108c6-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108c6-163">-DefaultProfile</span></span>
<span data-ttu-id="108c6-164">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="108c6-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="108c6-165">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="108c6-165">-Destination</span></span>
<span data-ttu-id="108c6-166">Specifica se aggiungere la chiave come chiave protetta dal software o con una chiave protetta da HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="108c6-167">I valori validi sono: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="108c6-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="108c6-168">Nota: per usare HSM come destinazione, è necessario disporre di un Vault Key che supporti HSM.</span><span class="sxs-lookup"><span data-stu-id="108c6-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="108c6-169">Per altre informazioni sui livelli di servizio e sulle funzionalità per l'archiviazione delle chiavi di Azure, vedere il [sito Web di Azure Key Vault pricing](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="108c6-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="108c6-170">Questo parametro è obbligatorio quando si crea una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="108c6-171">Se si importa una chiave usando il parametro *filePath* , questo parametro è facoltativo:</span><span class="sxs-lookup"><span data-stu-id="108c6-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="108c6-172">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione Byok, questa viene importata come chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="108c6-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="108c6-173">Il cmdlet non può importare la chiave come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="108c6-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="108c6-174">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione pfx, la chiave viene importata come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="108c6-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-175">-Disable</span><span class="sxs-lookup"><span data-stu-id="108c6-175">-Disable</span></span>
<span data-ttu-id="108c6-176">Indica che la chiave che si sta aggiungendo è impostata su uno stato iniziale di disabled.</span><span class="sxs-lookup"><span data-stu-id="108c6-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="108c6-177">Qualsiasi tentativo di usare la chiave non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="108c6-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="108c6-178">Usare questo parametro se si precaricano le chiavi che si desidera abilitare in seguito.</span><span class="sxs-lookup"><span data-stu-id="108c6-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="108c6-179">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="108c6-179">-Expires</span></span>
<span data-ttu-id="108c6-180">Specifica la data di scadenza, come oggetto **DateTime** , per la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="108c6-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="108c6-181">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="108c6-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="108c6-182">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="108c6-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="108c6-183">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="108c6-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="108c6-184">Se non specifichi questo parametro, la chiave non scade.</span><span class="sxs-lookup"><span data-stu-id="108c6-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="108c6-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="108c6-185">-InputObject</span></span>
<span data-ttu-id="108c6-186">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-186">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="108c6-187">-KeyFilePassword</span></span>
<span data-ttu-id="108c6-188">Specifica una password per il file importato come oggetto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="108c6-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="108c6-189">Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="108c6-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="108c6-190">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="108c6-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="108c6-191">Devi specificare questa password per importare un file con estensione pfx.</span><span class="sxs-lookup"><span data-stu-id="108c6-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-192">-FilePath</span><span class="sxs-lookup"><span data-stu-id="108c6-192">-KeyFilePath</span></span>
<span data-ttu-id="108c6-193">Specifica il percorso di un file locale che contiene il materiale chiave importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="108c6-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="108c6-194">Le estensioni valide per i nomi di file sono Byok e PFX.</span><span class="sxs-lookup"><span data-stu-id="108c6-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="108c6-195">Se il file è un file con estensione Byok, la chiave viene protetta automaticamente da HSM dopo l'importazione e non è possibile eseguire l'override di questa impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="108c6-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="108c6-196">Se il file è un file PFX, la chiave viene automaticamente protetta dal software dopo l'importazione.</span><span class="sxs-lookup"><span data-stu-id="108c6-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="108c6-197">Per eseguire l'override di questo valore predefinito, imposta il parametro di *destinazione* su HSM in modo che la chiave sia protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="108c6-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="108c6-198">Quando specifichi questo parametro, il parametro di *destinazione* è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="108c6-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="108c6-199">-KeyOps</span></span>
<span data-ttu-id="108c6-200">Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="108c6-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="108c6-201">Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="108c6-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="108c6-202">I valori accettabili per questo parametro sono un elenco delimitato da virgole delle operazioni chiave definite dalla [specifica JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="108c6-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="108c6-203">Crittografare</span><span class="sxs-lookup"><span data-stu-id="108c6-203">Encrypt</span></span>
- <span data-ttu-id="108c6-204">Decrittografare</span><span class="sxs-lookup"><span data-stu-id="108c6-204">Decrypt</span></span>
- <span data-ttu-id="108c6-205">A capo</span><span class="sxs-lookup"><span data-stu-id="108c6-205">Wrap</span></span>
- <span data-ttu-id="108c6-206">Annullare</span><span class="sxs-lookup"><span data-stu-id="108c6-206">Unwrap</span></span>
- <span data-ttu-id="108c6-207">Segno</span><span class="sxs-lookup"><span data-stu-id="108c6-207">Sign</span></span>
- <span data-ttu-id="108c6-208">Verificare</span><span class="sxs-lookup"><span data-stu-id="108c6-208">Verify</span></span>

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

### <span data-ttu-id="108c6-209">-Nome</span><span class="sxs-lookup"><span data-stu-id="108c6-209">-Name</span></span>
<span data-ttu-id="108c6-210">Specifica il nome della chiave da aggiungere all'archivio della chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="108c6-211">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="108c6-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="108c6-212">Il nome deve essere una stringa da 1 a 63 caratteri di lunghezza che contiene solo 0-9, a-z, A-Z e-(il simbolo del trattino).</span><span class="sxs-lookup"><span data-stu-id="108c6-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="108c6-213">-NotBefore</span></span>
<span data-ttu-id="108c6-214">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="108c6-215">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="108c6-215">This parameter uses UTC.</span></span> <span data-ttu-id="108c6-216">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="108c6-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="108c6-217">Se non specifichi questo parametro, la chiave può essere usata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="108c6-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="108c6-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="108c6-218">-ResourceId</span></span>
<span data-ttu-id="108c6-219">ID risorsa del Vault.</span><span class="sxs-lookup"><span data-stu-id="108c6-219">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-220">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="108c6-220">-Size</span></span>
<span data-ttu-id="108c6-221">Dimensioni chiave RSA in bit.</span><span class="sxs-lookup"><span data-stu-id="108c6-221">RSA key size, in bits.</span></span> <span data-ttu-id="108c6-222">Se non viene specificato, il servizio fornirà un valore predefinito sicuro.</span><span class="sxs-lookup"><span data-stu-id="108c6-222">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-223">-Tag</span><span class="sxs-lookup"><span data-stu-id="108c6-223">-Tag</span></span>
<span data-ttu-id="108c6-224">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="108c6-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="108c6-225">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="108c6-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="108c6-226">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="108c6-226">-VaultName</span></span>
<span data-ttu-id="108c6-227">Specifica il nome del Vault chiave a cui questo cmdlet aggiunge la chiave.</span><span class="sxs-lookup"><span data-stu-id="108c6-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="108c6-228">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="108c6-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108c6-229">-Confermare</span><span class="sxs-lookup"><span data-stu-id="108c6-229">-Confirm</span></span>
<span data-ttu-id="108c6-230">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="108c6-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="108c6-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="108c6-231">-WhatIf</span></span>
<span data-ttu-id="108c6-232">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="108c6-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="108c6-233">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="108c6-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="108c6-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108c6-234">CommonParameters</span></span>
<span data-ttu-id="108c6-235">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108c6-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108c6-236">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="108c6-236">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108c6-237">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="108c6-237">INPUTS</span></span>

### <span data-ttu-id="108c6-238">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="108c6-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="108c6-239">System. String</span><span class="sxs-lookup"><span data-stu-id="108c6-239">System.String</span></span>

## <span data-ttu-id="108c6-240">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="108c6-240">OUTPUTS</span></span>

### <span data-ttu-id="108c6-241">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="108c6-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="108c6-242">Note</span><span class="sxs-lookup"><span data-stu-id="108c6-242">NOTES</span></span>

## <span data-ttu-id="108c6-243">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="108c6-243">RELATED LINKS</span></span>

[<span data-ttu-id="108c6-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="108c6-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="108c6-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="108c6-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="108c6-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="108c6-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="108c6-247">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="108c6-247">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
