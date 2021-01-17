---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 6cea7f2584de3a27be2cee36c3f32fd792564160
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487016"
---
# <span data-ttu-id="1f9e6-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1f9e6-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="1f9e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9e6-103">Crea una chiave in un Vault chiave o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="1f9e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f9e6-104">SYNTAX</span></span>

### <span data-ttu-id="1f9e6-105">InteractiveCreate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f9e6-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="1f9e6-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="1f9e6-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="1f9e6-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="1f9e6-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="1f9e6-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="1f9e6-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="1f9e6-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="1f9e6-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="1f9e6-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="1f9e6-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9e6-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="1f9e6-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f9e6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f9e6-117">DESCRIPTION</span></span>
<span data-ttu-id="1f9e6-118">Il cmdlet **Add-AzKeyVaultKey** crea una chiave in un Vault chiave in Azure Key Vault o importa una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="1f9e6-119">Questo cmdlet consente di aggiungere chiavi utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f9e6-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="1f9e6-120">Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="1f9e6-121">Creare una chiave nel software nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="1f9e6-122">Importare una chiave da un modulo HSM (hardware Security Module) in HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="1f9e6-123">Importare una chiave da un file con estensione pfx nel computer.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="1f9e6-124">Importare una chiave da un file PFX nel computer in moduli di sicurezza hardware (HSM) nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="1f9e6-125">Per ognuna di queste operazioni, è possibile specificare gli attributi chiave o accettare le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="1f9e6-126">Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel Vault chiave, la chiave originale viene aggiornata con i valori specificati per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="1f9e6-127">Puoi accedere ai valori precedenti usando l'URI specifico della versione per la versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="1f9e6-128">Per informazioni sulle versioni chiave e sulla struttura URI, vedere [informazioni sulle chiavi e i segreti](http://go.microsoft.com/fwlink/?linkid=518560) nella documentazione dell'API REST di Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="1f9e6-129">Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="1f9e6-130">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="1f9e6-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="1f9e6-131">Come procedura consigliata, eseguire il backup della chiave dopo la creazione o l'aggiornamento usando il cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="1f9e6-132">Non esiste alcuna funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non è recuperabile, a meno che non si disponga di un backup che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="1f9e6-133">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f9e6-133">EXAMPLES</span></span>

### <span data-ttu-id="1f9e6-134">Esempio 1: creare una chiave</span><span class="sxs-lookup"><span data-stu-id="1f9e6-134">Example 1: Create a key</span></span>
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

<span data-ttu-id="1f9e6-135">Questo comando crea una chiave protetta dal software denominata ITSoftware nel caveau della chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="1f9e6-136">Esempio 2: creare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="1f9e6-136">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="1f9e6-137">Questo comando crea una chiave con protezione HSM nel Vault chiave denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="1f9e6-138">Esempio 3: creare una chiave con valori non predefiniti</span><span class="sxs-lookup"><span data-stu-id="1f9e6-138">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="1f9e6-139">Con il primo comando vengono archiviati i valori decrittografati e verificati nella variabile $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="1f9e6-140">Il secondo comando crea un oggetto **DateTime** , definito in formato UTC, usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="1f9e6-141">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="1f9e6-142">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="1f9e6-143">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1f9e6-144">Il terzo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1f9e6-145">Tale oggetto specifica l'ora UTC corrente.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-145">That object specifies current UTC time.</span></span> <span data-ttu-id="1f9e6-146">Il comando archivia tale data nella variabile $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="1f9e6-147">Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="1f9e6-148">Il comando specifica i valori per le operazioni chiave consentite archiviate $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="1f9e6-149">Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="1f9e6-150">La nuova chiave è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-150">The new key is disabled.</span></span> <span data-ttu-id="1f9e6-151">Puoi abilitarlo usando il cmdlet **set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="1f9e6-152">Esempio 4: importare un tasto protetto da HSM</span><span class="sxs-lookup"><span data-stu-id="1f9e6-152">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="1f9e6-153">Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *filePath* .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="1f9e6-154">La chiave importata è una chiave con protezione HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="1f9e6-155">Per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="1f9e6-156">Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="1f9e6-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="1f9e6-157">Esempio 5: importare una chiave protetta dal software</span><span class="sxs-lookup"><span data-stu-id="1f9e6-157">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="1f9e6-158">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="1f9e6-159">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1f9e6-160">Il secondo comando crea una password software nel caveau della chiave contoso.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="1f9e6-161">Il comando specifica la posizione per la chiave e la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="1f9e6-162">Esempio 6: importare una chiave e assegnare attributi</span><span class="sxs-lookup"><span data-stu-id="1f9e6-162">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="1f9e6-163">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="1f9e6-164">Il secondo comando crea un oggetto **DateTime** usando il cmdlet **get-date** e quindi archivia tale oggetto nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="1f9e6-165">Il terzo comando crea la variabile $tags per impostare i contrassegni per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="1f9e6-166">Il comando finale importa una chiave come chiave HSM dalla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="1f9e6-167">Il comando specifica la data di scadenza archiviata in $Expires e la password archiviata in $Password e applica i tag archiviati in $tags.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="1f9e6-168">Esempio 7: generare una chiave di scambio chiave (KEK) per la caratteristica "porta la tua chiave" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="1f9e6-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="1f9e6-169">Genera una chiave, denominata chiave di scambio chiave (KEK).</span><span class="sxs-lookup"><span data-stu-id="1f9e6-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="1f9e6-170">La KEK deve essere una chiave RSA-HSM che contiene solo l'operazione chiave di importazione.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="1f9e6-171">La sola SKU Key Vault Premium supporta le chiavi RSA-HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="1f9e6-172">Per altre informazioni, consulta https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="1f9e6-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="1f9e6-173">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f9e6-173">PARAMETERS</span></span>

### <span data-ttu-id="1f9e6-174">-Curvename</span><span class="sxs-lookup"><span data-stu-id="1f9e6-174">-CurveName</span></span>
<span data-ttu-id="1f9e6-175">Specifica il nome della curva della crittografia a curva ellittica, questo valore è valido quando il tipo di pulsante è EC.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9e6-176">-DefaultProfile</span></span>
<span data-ttu-id="1f9e6-177">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f9e6-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f9e6-178">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="1f9e6-178">-Destination</span></span>
<span data-ttu-id="1f9e6-179">Specifica se aggiungere la chiave come chiave protetta dal software o con una chiave protetta da HSM nel servizio Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="1f9e6-180">I valori validi sono: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="1f9e6-181">Nota: per usare HSM come destinazione, è necessario disporre di un Vault Key che supporti HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="1f9e6-182">Per altre informazioni sui livelli di servizio e sulle funzionalità per l'archiviazione delle chiavi di Azure, vedere il [sito Web di Azure Key Vault pricing](http://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="1f9e6-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="1f9e6-183">Questo parametro è obbligatorio quando si crea una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="1f9e6-184">Se si importa una chiave usando il parametro *filePath* , questo parametro è facoltativo:</span><span class="sxs-lookup"><span data-stu-id="1f9e6-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="1f9e6-185">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione Byok, questa viene importata come chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="1f9e6-186">Il cmdlet non può importare la chiave come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="1f9e6-187">Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione pfx, la chiave viene importata come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="1f9e6-188">-Disable</span><span class="sxs-lookup"><span data-stu-id="1f9e6-188">-Disable</span></span>
<span data-ttu-id="1f9e6-189">Indica che la chiave che si sta aggiungendo è impostata su uno stato iniziale di disabled.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="1f9e6-190">Qualsiasi tentativo di usare la chiave non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="1f9e6-191">Usare questo parametro se si precaricano le chiavi che si desidera abilitare in seguito.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="1f9e6-192">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="1f9e6-192">-Expires</span></span>
<span data-ttu-id="1f9e6-193">Specifica la data di scadenza, come oggetto **DateTime** , per la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="1f9e6-194">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="1f9e6-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1f9e6-195">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1f9e6-196">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="1f9e6-197">Se non specifichi questo parametro, la chiave non scade.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-197">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="1f9e6-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="1f9e6-198">-HsmName</span></span>
<span data-ttu-id="1f9e6-199">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-199">HSM name.</span></span> <span data-ttu-id="1f9e6-200">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="1f9e6-201">-HsmObject</span></span>
<span data-ttu-id="1f9e6-202">Oggetto HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9e6-203">-HsmResourceId</span></span>
<span data-ttu-id="1f9e6-204">ID risorsa dell'HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f9e6-205">-InputObject</span></span>
<span data-ttu-id="1f9e6-206">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-206">Vault object.</span></span>

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

### <span data-ttu-id="1f9e6-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="1f9e6-207">-KeyFilePassword</span></span>
<span data-ttu-id="1f9e6-208">Specifica una password per il file importato come oggetto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="1f9e6-209">Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="1f9e6-210">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="1f9e6-211">Devi specificare questa password per importare un file con estensione pfx.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-212">-FilePath</span><span class="sxs-lookup"><span data-stu-id="1f9e6-212">-KeyFilePath</span></span>
<span data-ttu-id="1f9e6-213">Specifica il percorso di un file locale che contiene il materiale chiave importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="1f9e6-214">Le estensioni valide per i nomi di file sono Byok e PFX.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="1f9e6-215">Se il file è un file con estensione Byok, la chiave viene protetta automaticamente da HSM dopo l'importazione e non è possibile eseguire l'override di questa impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="1f9e6-216">Se il file è un file PFX, la chiave viene automaticamente protetta dal software dopo l'importazione.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="1f9e6-217">Per eseguire l'override di questo valore predefinito, imposta il parametro di *destinazione* su HSM in modo che la chiave sia protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="1f9e6-218">Quando specifichi questo parametro, il parametro di *destinazione* è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="1f9e6-219">-KeyOps</span></span>
<span data-ttu-id="1f9e6-220">Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="1f9e6-221">Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="1f9e6-222">I valori accettabili per questo parametro sono un elenco delimitato da virgole delle operazioni chiave definite dalla [specifica JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="1f9e6-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="1f9e6-223">crittografare</span><span class="sxs-lookup"><span data-stu-id="1f9e6-223">encrypt</span></span>
- <span data-ttu-id="1f9e6-224">decrittografare</span><span class="sxs-lookup"><span data-stu-id="1f9e6-224">decrypt</span></span>
- <span data-ttu-id="1f9e6-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="1f9e6-225">wrapKey</span></span>
- <span data-ttu-id="1f9e6-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="1f9e6-226">unwrapKey</span></span>
- <span data-ttu-id="1f9e6-227">segno</span><span class="sxs-lookup"><span data-stu-id="1f9e6-227">sign</span></span>
- <span data-ttu-id="1f9e6-228">verificare</span><span class="sxs-lookup"><span data-stu-id="1f9e6-228">verify</span></span>
- <span data-ttu-id="1f9e6-229">Importa (solo per KEK, Vedi l'esempio 7)</span><span class="sxs-lookup"><span data-stu-id="1f9e6-229">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="1f9e6-230">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="1f9e6-230">-KeyType</span></span>
<span data-ttu-id="1f9e6-231">Specifica il tipo di chiave di questa chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-231">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-232">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f9e6-232">-Name</span></span>
<span data-ttu-id="1f9e6-233">Specifica il nome della chiave da aggiungere all'archivio della chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-233">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="1f9e6-234">Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-234">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="1f9e6-235">Il nome deve essere una stringa da 1 a 63 caratteri di lunghezza che contiene solo 0-9, a-z, A-Z e-(il simbolo del trattino).</span><span class="sxs-lookup"><span data-stu-id="1f9e6-235">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="1f9e6-236">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1f9e6-236">-NotBefore</span></span>
<span data-ttu-id="1f9e6-237">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-237">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="1f9e6-238">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-238">This parameter uses UTC.</span></span> <span data-ttu-id="1f9e6-239">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="1f9e6-239">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1f9e6-240">Se non specifichi questo parametro, la chiave può essere usata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-240">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="1f9e6-241">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9e6-241">-ResourceId</span></span>
<span data-ttu-id="1f9e6-242">ID risorsa del Vault.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-242">Vault Resource Id.</span></span>

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

### <span data-ttu-id="1f9e6-243">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="1f9e6-243">-Size</span></span>
<span data-ttu-id="1f9e6-244">Dimensioni chiave RSA in bit.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-244">RSA key size, in bits.</span></span> <span data-ttu-id="1f9e6-245">Se non viene specificato, il servizio fornirà un valore predefinito sicuro.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-245">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9e6-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f9e6-246">-Tag</span></span>
<span data-ttu-id="1f9e6-247">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-247">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1f9e6-248">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1f9e6-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1f9e6-249">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="1f9e6-249">-VaultName</span></span>
<span data-ttu-id="1f9e6-250">Specifica il nome del Vault chiave a cui questo cmdlet aggiunge la chiave.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-250">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="1f9e6-251">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-251">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="1f9e6-252">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f9e6-252">-Confirm</span></span>
<span data-ttu-id="1f9e6-253">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-253">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f9e6-254">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f9e6-254">-WhatIf</span></span>
<span data-ttu-id="1f9e6-255">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-255">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f9e6-256">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-256">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f9e6-257">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9e6-257">CommonParameters</span></span>
<span data-ttu-id="1f9e6-258">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f9e6-258">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9e6-259">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f9e6-259">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9e6-260">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f9e6-260">INPUTS</span></span>

### <span data-ttu-id="1f9e6-261">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1f9e6-261">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1f9e6-262">System. String</span><span class="sxs-lookup"><span data-stu-id="1f9e6-262">System.String</span></span>

## <span data-ttu-id="1f9e6-263">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f9e6-263">OUTPUTS</span></span>

### <span data-ttu-id="1f9e6-264">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1f9e6-264">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="1f9e6-265">Note</span><span class="sxs-lookup"><span data-stu-id="1f9e6-265">NOTES</span></span>

## <span data-ttu-id="1f9e6-266">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f9e6-266">RELATED LINKS</span></span>

[<span data-ttu-id="1f9e6-267">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1f9e6-267">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="1f9e6-268">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1f9e6-268">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="1f9e6-269">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1f9e6-269">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1f9e6-270">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="1f9e6-270">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
