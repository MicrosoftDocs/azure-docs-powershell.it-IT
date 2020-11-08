---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 8583a078e12be5da3a6bcbbe16bc3349f51b9bdb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033062"
---
# <span data-ttu-id="e5953-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5953-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="e5953-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5953-102">SYNOPSIS</span></span>
<span data-ttu-id="e5953-103">Crea una chiave in un Vault chiave o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="e5953-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5953-104">SYNTAX</span></span>

### <span data-ttu-id="e5953-105">InteractiveCreate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5953-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5953-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="e5953-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5953-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="e5953-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5953-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="e5953-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5953-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="e5953-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5953-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="e5953-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5953-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5953-111">DESCRIPTION</span></span>
<span data-ttu-id="e5953-112">Il cmdlet **Add-AzKeyVaultKey** crea una chiave in un Vault chiave in Azure Key Vault o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="e5953-113">Questo cmdlet consente di aggiungere chiavi utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5953-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="e5953-114">Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="e5953-115">Creare una chiave nel software nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="e5953-116">Importare una chiave da un modulo HSM (hardware Security Module) in HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="e5953-117">Importare una chiave da un file con estensione pfx nel computer.</span><span class="sxs-lookup"><span data-stu-id="e5953-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="e5953-118">Importare una chiave da un file PFX nel computer in moduli di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="e5953-119">Per ognuna di queste operazioni, è possibile specificare gli attributi chiave o accettare le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="e5953-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="e5953-120">Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel Vault chiave, la chiave originale viene aggiornata con i valori specificati per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="e5953-121">Puoi accedere ai valori precedenti usando l'URI specifico della versione per la versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="e5953-122">Per informazioni sulle versioni chiave e sulla struttura URI, vedere [informazioni sulle chiavi e i segreti](http://go.microsoft.com/fwlink/?linkid=518560) nella documentazione dell'API REST di Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="e5953-123">Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5953-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="e5953-124">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="e5953-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="e5953-125">Come procedura consigliata, eseguire il backup della chiave dopo la creazione o l'aggiornamento usando il cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="e5953-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="e5953-126">Non esiste alcuna funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non è recuperabile, a meno che non si disponga di un backup che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="e5953-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="e5953-127">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5953-127">EXAMPLES</span></span>

### <span data-ttu-id="e5953-128">Esempio 1: creare una chiave</span><span class="sxs-lookup"><span data-stu-id="e5953-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="e5953-129">Questo comando crea una chiave protetta dal software denominata ITSoftware nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="e5953-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="e5953-130">Esempio 2: creare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="e5953-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="e5953-131">Questo comando crea una chiave con protezione HSM nel Vault chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="e5953-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="e5953-132">Esempio 3: creare una chiave con valori non predefiniti</span><span class="sxs-lookup"><span data-stu-id="e5953-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="e5953-133">Con il primo comando vengono archiviati i valori decrittografati e verificati nella variabile $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="e5953-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="e5953-134">Il secondo comando crea un oggetto **DateTime** , definito in formato UTC, usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e5953-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="e5953-135">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="e5953-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="e5953-136">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="e5953-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="e5953-137">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e5953-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="e5953-138">Il terzo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e5953-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e5953-139">Tale oggetto specifica l'ora UTC corrente.</span><span class="sxs-lookup"><span data-stu-id="e5953-139">That object specifies current UTC time.</span></span> <span data-ttu-id="e5953-140">Il comando archivia tale data nella variabile $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="e5953-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="e5953-141">Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="e5953-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="e5953-142">Il comando specifica i valori per le operazioni chiave consentite archiviate $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="e5953-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="e5953-143">Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="e5953-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="e5953-144">La nuova chiave è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e5953-144">The new key is disabled.</span></span> <span data-ttu-id="e5953-145">Puoi abilitarlo usando il cmdlet **set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="e5953-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="e5953-146">Esempio 4: importare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="e5953-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="e5953-147">Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *filePath* .</span><span class="sxs-lookup"><span data-stu-id="e5953-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="e5953-148">La chiave importata è una chiave con protezione HSM.</span><span class="sxs-lookup"><span data-stu-id="e5953-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="e5953-149">Per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5953-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="e5953-150">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="e5953-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="e5953-151">Esempio 5: importare una chiave protetta dal software</span><span class="sxs-lookup"><span data-stu-id="e5953-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="e5953-152">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="e5953-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="e5953-153">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e5953-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="e5953-154">Il secondo comando crea una password software nel caveau della chiave contoso.</span><span class="sxs-lookup"><span data-stu-id="e5953-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="e5953-155">Il comando specifica la posizione per la chiave e la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="e5953-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="e5953-156">Esempio 6: importare una chiave e assegnare attributi</span><span class="sxs-lookup"><span data-stu-id="e5953-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="e5953-157">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="e5953-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="e5953-158">Il secondo comando crea un oggetto **DateTime** usando il cmdlet **get-date** e quindi archivia tale oggetto nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="e5953-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="e5953-159">Il terzo comando crea la variabile $tags per impostare i contrassegni per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="e5953-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="e5953-160">Il comando finale importa una chiave come chiave HSM dalla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="e5953-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="e5953-161">Il comando specifica la data di scadenza archiviata in $Expires e la password archiviata in $Password e applica i tag archiviati in $tags.</span><span class="sxs-lookup"><span data-stu-id="e5953-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="e5953-162">Esempio 7: generare una chiave di scambio chiave (KEK) per la caratteristica "porta la tua chiave" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="e5953-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="e5953-163">Genera una chiave, denominata chiave di scambio chiave (KEK).</span><span class="sxs-lookup"><span data-stu-id="e5953-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="e5953-164">La KEK deve essere una chiave RSA-HSM che contiene solo l'operazione chiave di importazione.</span><span class="sxs-lookup"><span data-stu-id="e5953-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="e5953-165">La sola SKU Key Vault Premium supporta le chiavi RSA-HSM.</span><span class="sxs-lookup"><span data-stu-id="e5953-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="e5953-166">Per altre informazioni, consulta https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="e5953-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="e5953-167">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5953-167">PARAMETERS</span></span>

### <span data-ttu-id="e5953-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5953-168">-DefaultProfile</span></span>
<span data-ttu-id="e5953-169">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5953-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5953-170">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="e5953-170">-Destination</span></span>
<span data-ttu-id="e5953-171">Specifica se aggiungere la chiave come chiave protetta dal software o con una chiave protetta da HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="e5953-172">I valori validi sono: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="e5953-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="e5953-173">Nota: per usare HSM come destinazione, è necessario disporre di un Vault Key che supporti HSM.</span><span class="sxs-lookup"><span data-stu-id="e5953-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="e5953-174">Per altre informazioni sui livelli di servizio e sulle funzionalità per l'archiviazione delle chiavi di Azure, vedere il [sito Web di Azure Key Vault pricing](http://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="e5953-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="e5953-175">Questo parametro è obbligatorio quando si crea una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="e5953-176">Se si importa una chiave usando il parametro *filePath* , questo parametro è facoltativo:</span><span class="sxs-lookup"><span data-stu-id="e5953-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="e5953-177">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione Byok, questa viene importata come chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="e5953-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="e5953-178">Il cmdlet non può importare la chiave come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="e5953-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="e5953-179">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione pfx, la chiave viene importata come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="e5953-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="e5953-180">-Disable</span><span class="sxs-lookup"><span data-stu-id="e5953-180">-Disable</span></span>
<span data-ttu-id="e5953-181">Indica che la chiave che si sta aggiungendo è impostata su uno stato iniziale di disabled.</span><span class="sxs-lookup"><span data-stu-id="e5953-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="e5953-182">Qualsiasi tentativo di usare la chiave non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="e5953-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="e5953-183">Usare questo parametro se si precaricano le chiavi che si desidera abilitare in seguito.</span><span class="sxs-lookup"><span data-stu-id="e5953-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="e5953-184">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="e5953-184">-Expires</span></span>
<span data-ttu-id="e5953-185">Specifica la data di scadenza, come oggetto **DateTime** , per la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5953-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="e5953-186">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="e5953-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e5953-187">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e5953-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e5953-188">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e5953-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="e5953-189">Se non specifichi questo parametro, la chiave non scade.</span><span class="sxs-lookup"><span data-stu-id="e5953-189">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="e5953-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5953-190">-InputObject</span></span>
<span data-ttu-id="e5953-191">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-191">Vault object.</span></span>

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

### <span data-ttu-id="e5953-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="e5953-192">-KeyFilePassword</span></span>
<span data-ttu-id="e5953-193">Specifica una password per il file importato come oggetto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="e5953-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="e5953-194">Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="e5953-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="e5953-195">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="e5953-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="e5953-196">Devi specificare questa password per importare un file con estensione pfx.</span><span class="sxs-lookup"><span data-stu-id="e5953-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="e5953-197">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e5953-197">-KeyFilePath</span></span>
<span data-ttu-id="e5953-198">Specifica il percorso di un file locale che contiene il materiale chiave importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5953-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="e5953-199">Le estensioni valide per i nomi di file sono Byok e PFX.</span><span class="sxs-lookup"><span data-stu-id="e5953-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="e5953-200">Se il file è un file con estensione Byok, la chiave viene protetta automaticamente da HSM dopo l'importazione e non è possibile eseguire l'override di questa impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e5953-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="e5953-201">Se il file è un file PFX, la chiave viene automaticamente protetta dal software dopo l'importazione.</span><span class="sxs-lookup"><span data-stu-id="e5953-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="e5953-202">Per eseguire l'override di questo valore predefinito, imposta il parametro di *destinazione* su HSM in modo che la chiave sia protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="e5953-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="e5953-203">Quando specifichi questo parametro, il parametro di *destinazione* è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e5953-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="e5953-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="e5953-204">-KeyOps</span></span>
<span data-ttu-id="e5953-205">Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5953-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="e5953-206">Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="e5953-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="e5953-207">I valori accettabili per questo parametro sono un elenco delimitato da virgole delle operazioni chiave definite dalla [specifica JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="e5953-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="e5953-208">crittografare</span><span class="sxs-lookup"><span data-stu-id="e5953-208">encrypt</span></span>
- <span data-ttu-id="e5953-209">decrittografare</span><span class="sxs-lookup"><span data-stu-id="e5953-209">decrypt</span></span>
- <span data-ttu-id="e5953-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="e5953-210">wrapKey</span></span>
- <span data-ttu-id="e5953-211">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="e5953-211">unwrapKey</span></span>
- <span data-ttu-id="e5953-212">segno</span><span class="sxs-lookup"><span data-stu-id="e5953-212">sign</span></span>
- <span data-ttu-id="e5953-213">verificare</span><span class="sxs-lookup"><span data-stu-id="e5953-213">verify</span></span>
- <span data-ttu-id="e5953-214">Importa (solo per KEK, Vedi l'esempio 7)</span><span class="sxs-lookup"><span data-stu-id="e5953-214">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="e5953-215">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5953-215">-Name</span></span>
<span data-ttu-id="e5953-216">Specifica il nome della chiave da aggiungere all'archivio della chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="e5953-217">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="e5953-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="e5953-218">Il nome deve essere una stringa da 1 a 63 caratteri di lunghezza che contiene solo 0-9, a-z, A-Z e-(il simbolo del trattino).</span><span class="sxs-lookup"><span data-stu-id="e5953-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="e5953-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="e5953-219">-NotBefore</span></span>
<span data-ttu-id="e5953-220">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="e5953-221">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="e5953-221">This parameter uses UTC.</span></span> <span data-ttu-id="e5953-222">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="e5953-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e5953-223">Se non specifichi questo parametro, la chiave può essere usata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="e5953-223">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="e5953-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5953-224">-ResourceId</span></span>
<span data-ttu-id="e5953-225">ID risorsa del Vault.</span><span class="sxs-lookup"><span data-stu-id="e5953-225">Vault Resource Id.</span></span>

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

### <span data-ttu-id="e5953-226">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="e5953-226">-Size</span></span>
<span data-ttu-id="e5953-227">Dimensioni chiave RSA in bit.</span><span class="sxs-lookup"><span data-stu-id="e5953-227">RSA key size, in bits.</span></span> <span data-ttu-id="e5953-228">Se non viene specificato, il servizio fornirà un valore predefinito sicuro.</span><span class="sxs-lookup"><span data-stu-id="e5953-228">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="e5953-229">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5953-229">-Tag</span></span>
<span data-ttu-id="e5953-230">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e5953-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5953-231">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e5953-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e5953-232">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e5953-232">-VaultName</span></span>
<span data-ttu-id="e5953-233">Specifica il nome del Vault chiave a cui questo cmdlet aggiunge la chiave.</span><span class="sxs-lookup"><span data-stu-id="e5953-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="e5953-234">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="e5953-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="e5953-235">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5953-235">-Confirm</span></span>
<span data-ttu-id="e5953-236">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5953-236">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5953-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5953-237">-WhatIf</span></span>
<span data-ttu-id="e5953-238">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5953-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5953-239">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5953-239">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5953-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5953-240">CommonParameters</span></span>
<span data-ttu-id="e5953-241">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5953-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5953-242">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5953-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5953-243">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5953-243">INPUTS</span></span>

### <span data-ttu-id="e5953-244">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e5953-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e5953-245">System. String</span><span class="sxs-lookup"><span data-stu-id="e5953-245">System.String</span></span>

## <span data-ttu-id="e5953-246">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5953-246">OUTPUTS</span></span>

### <span data-ttu-id="e5953-247">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5953-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="e5953-248">Note</span><span class="sxs-lookup"><span data-stu-id="e5953-248">NOTES</span></span>

## <span data-ttu-id="e5953-249">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5953-249">RELATED LINKS</span></span>

[<span data-ttu-id="e5953-250">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5953-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="e5953-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5953-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="e5953-252">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e5953-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="e5953-253">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="e5953-253">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
