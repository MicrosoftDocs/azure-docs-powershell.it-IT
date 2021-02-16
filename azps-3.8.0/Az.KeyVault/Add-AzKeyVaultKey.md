---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 3d0f7267d1dbe899de0e0414c52a395985f09bfd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412538"
---
# <span data-ttu-id="66013-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="66013-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="66013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66013-102">SYNOPSIS</span></span>
<span data-ttu-id="66013-103">Crea una chiave in un vault delle chiavi o importa una chiave in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="66013-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66013-104">SYNTAX</span></span>

### <span data-ttu-id="66013-105">InteractiveCreate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66013-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66013-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="66013-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66013-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="66013-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66013-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="66013-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66013-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="66013-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66013-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="66013-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66013-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="66013-111">DESCRIPTION</span></span>
<span data-ttu-id="66013-112">Il cmdlet **Add-AzKeyVaultKey** crea una chiave in un vault delle chiavi nel Vault delle chiavi di Azure oppure importa una chiave in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="66013-113">Usare questo cmdlet per aggiungere le chiavi usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66013-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="66013-114">Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="66013-115">Creare una chiave nel software nel servizio Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="66013-116">Importare una chiave dal proprio modulo di sicurezza hardware (HSM) a un sistema HMS nel servizio Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="66013-117">Importare una chiave da un file PFX nel computer.</span><span class="sxs-lookup"><span data-stu-id="66013-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="66013-118">Importare una chiave da un file PFX nel computer nei moduli di sicurezza hardware (HMS) nel servizio Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="66013-119">Per una di queste operazioni, è possibile fornire attributi chiave o accettare le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="66013-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="66013-120">Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel vault delle chiavi, la chiave originale viene aggiornata con i valori specificati per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="66013-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="66013-121">È possibile accedere ai valori precedenti usando l'URI specifico della versione per tale versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="66013-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="66013-122">Per informazioni sulle versioni principali e sulla struttura DELL'URI, vedere [Informazioni sulle](http://go.microsoft.com/fwlink/?linkid=518560) chiavi e i segreti nella documentazione dell'API REST del Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="66013-123">Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario generare prima un pacchetto BYOK (un file con estensione byok) usando il set di strumenti BYOK del Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="66013-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="66013-124">Per altre informazioni, vedere Come generare e trasferire le chiavi HSM-Protected [per il Vault delle chiavi di Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="66013-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="66013-125">Come procedura consigliata, eseguire il backup della chiave dopo che è stata creata o aggiornata, usando il cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="66013-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="66013-126">Non sono disponibili funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non può essere recuperata a meno che non si abbia un backup che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="66013-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="66013-127">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66013-127">EXAMPLES</span></span>

### <span data-ttu-id="66013-128">Esempio 1: Creare una chiave</span><span class="sxs-lookup"><span data-stu-id="66013-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="66013-129">Questo comando crea una chiave protetta da software denominata ITSoftware nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="66013-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="66013-130">Esempio 2: Creare una chiave protetta da HSM</span><span class="sxs-lookup"><span data-stu-id="66013-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="66013-131">Questo comando crea una chiave protetta da HSM nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="66013-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="66013-132">Esempio 3: Creare una chiave con valori non predefiniti</span><span class="sxs-lookup"><span data-stu-id="66013-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="66013-133">Il primo comando archivia i valori decrittografa e verifica nella $KeyOperations variabile.</span><span class="sxs-lookup"><span data-stu-id="66013-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="66013-134">Il secondo comando crea un **oggetto DateTime,** definito in UTC, usando il cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="66013-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="66013-135">L'oggetto specifica un periodo di tempo futuro di due anni.</span><span class="sxs-lookup"><span data-stu-id="66013-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="66013-136">Il comando archivia tale data nella $Expires variabile.</span><span class="sxs-lookup"><span data-stu-id="66013-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="66013-137">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="66013-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="66013-138">Il terzo comando crea un **oggetto DateTime** usando il cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="66013-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="66013-139">Questo oggetto specifica l'ora UTC corrente.</span><span class="sxs-lookup"><span data-stu-id="66013-139">That object specifies current UTC time.</span></span> <span data-ttu-id="66013-140">Il comando archivia tale data nella $NotBefore variabile.</span><span class="sxs-lookup"><span data-stu-id="66013-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="66013-141">Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="66013-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="66013-142">Il comando specifica i valori per le operazioni chiave consentite $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="66013-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="66013-143">Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per un livello di gravità elevato e per l'IT.</span><span class="sxs-lookup"><span data-stu-id="66013-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="66013-144">La nuova chiave viene disabilitata.</span><span class="sxs-lookup"><span data-stu-id="66013-144">The new key is disabled.</span></span> <span data-ttu-id="66013-145">È possibile abilitarla usando il cmdlet **Set-AzKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="66013-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="66013-146">Esempio 4: Importare una chiave protetta da HSM</span><span class="sxs-lookup"><span data-stu-id="66013-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="66013-147">Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *KeyFilePath.*</span><span class="sxs-lookup"><span data-stu-id="66013-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="66013-148">La chiave importata è una chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="66013-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="66013-149">Per importare una chiave dal proprio modulo di sicurezza hardware, è necessario generare prima un pacchetto BYOK (un file con estensione byok) usando il set di strumenti BYOK del Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="66013-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="66013-150">Per altre informazioni, vedere Come generare e trasferire le chiavi HSM-Protected [per il Vault delle chiavi di Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="66013-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="66013-151">Esempio 5: Importare una chiave protetta da software</span><span class="sxs-lookup"><span data-stu-id="66013-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="66013-152">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="66013-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="66013-153">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="66013-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="66013-154">Il secondo comando crea una password software nel vault della chiave Contoso.</span><span class="sxs-lookup"><span data-stu-id="66013-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="66013-155">Il comando specifica il percorso della chiave e la password archiviati nel $Password.</span><span class="sxs-lookup"><span data-stu-id="66013-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="66013-156">Esempio 6: Importare una chiave e assegnare attributi</span><span class="sxs-lookup"><span data-stu-id="66013-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="66013-157">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="66013-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="66013-158">Il secondo comando crea un **oggetto DateTime** usando il cmdlet **Get-Date** e quindi archivia l'oggetto nella $Expires variabile.</span><span class="sxs-lookup"><span data-stu-id="66013-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="66013-159">Il terzo comando crea la $tags variabile per impostare tag di gravità elevata e it.</span><span class="sxs-lookup"><span data-stu-id="66013-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="66013-160">Il comando finale importa una chiave come chiave HSM dalla posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="66013-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="66013-161">Il comando specifica la scadenza archiviata in $Expires e la password archiviati in $Password e applica i tag archiviati in $tags.</span><span class="sxs-lookup"><span data-stu-id="66013-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="66013-162">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66013-162">PARAMETERS</span></span>

### <span data-ttu-id="66013-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66013-163">-DefaultProfile</span></span>
<span data-ttu-id="66013-164">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="66013-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66013-165">-Destination</span><span class="sxs-lookup"><span data-stu-id="66013-165">-Destination</span></span>
<span data-ttu-id="66013-166">Specifica se aggiungere la chiave come chiave protetta dal software o come chiave protetta da HSM nel servizio Vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="66013-167">I valori validi sono HSM e Software.</span><span class="sxs-lookup"><span data-stu-id="66013-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="66013-168">Nota: per usare HSM come destinazione, è necessario avere un vault delle chiavi che supporti gli HMS.</span><span class="sxs-lookup"><span data-stu-id="66013-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="66013-169">Per altre informazioni sui livelli di servizio e sulle funzionalità per il Vault delle chiavi di Azure, vedere il sito [Web prezzi del Vault delle chiavi di Azure.](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="66013-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="66013-170">Questo parametro è obbligatorio quando si crea una nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="66013-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="66013-171">Se si importa una chiave usando il *parametro KeyFilePath,* questo parametro è facoltativo:</span><span class="sxs-lookup"><span data-stu-id="66013-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="66013-172">Se non si specifica questo parametro e questo cmdlet importa una chiave con estensione byok, la importa come chiave protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="66013-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="66013-173">Il cmdlet non può importare la chiave come chiave protetta da software.</span><span class="sxs-lookup"><span data-stu-id="66013-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="66013-174">Se non si specifica questo parametro e questo cmdlet importa una chiave con estensione pfx, la importa come chiave protetta dal software.</span><span class="sxs-lookup"><span data-stu-id="66013-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="66013-175">-Disable</span><span class="sxs-lookup"><span data-stu-id="66013-175">-Disable</span></span>
<span data-ttu-id="66013-176">Indica che la chiave che si sta aggiungendo è impostata sullo stato iniziale Disabilitato.</span><span class="sxs-lookup"><span data-stu-id="66013-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="66013-177">Qualsiasi tentativo di usare la chiave non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="66013-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="66013-178">Usare questo parametro se si precaricano chiavi che si intende abilitare in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="66013-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="66013-179">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="66013-179">-Expires</span></span>
<span data-ttu-id="66013-180">Specifica la scadenza, come oggetto **DateTime,** per la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66013-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="66013-181">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="66013-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="66013-182">Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="66013-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="66013-183">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="66013-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="66013-184">Se non si specifica questo parametro, la chiave non scade.</span><span class="sxs-lookup"><span data-stu-id="66013-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="66013-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66013-185">-InputObject</span></span>
<span data-ttu-id="66013-186">Oggetto Vault.</span><span class="sxs-lookup"><span data-stu-id="66013-186">Vault object.</span></span>

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

### <span data-ttu-id="66013-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="66013-187">-KeyFilePassword</span></span>
<span data-ttu-id="66013-188">Specifica una password per il file importato come **oggetto SecureString.**</span><span class="sxs-lookup"><span data-stu-id="66013-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="66013-189">Per ottenere un **oggetto SecureString,** usare il cmdlet **ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="66013-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="66013-190">Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="66013-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="66013-191">È necessario specificare questa password per importare un file con estensione pfx.</span><span class="sxs-lookup"><span data-stu-id="66013-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="66013-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="66013-192">-KeyFilePath</span></span>
<span data-ttu-id="66013-193">Specifica il percorso di un file locale che contiene il materiale chiave importato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66013-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="66013-194">Le estensioni di file valide sono byok e pfx.</span><span class="sxs-lookup"><span data-stu-id="66013-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="66013-195">Se il file è byok, la chiave viene protetta automaticamente dai messaggi hMS dopo l'importazione e non è possibile ignorare questa impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="66013-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="66013-196">Se il file è un file PFX, la chiave viene protetta automaticamente dal software dopo l'importazione.</span><span class="sxs-lookup"><span data-stu-id="66013-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="66013-197">Per ignorare questa impostazione predefinita, impostare *il parametro Destination* su HSM in modo che la chiave sia protetta da HSM.</span><span class="sxs-lookup"><span data-stu-id="66013-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="66013-198">Quando si specifica questo parametro, *il parametro Destination* è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66013-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="66013-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="66013-199">-KeyOps</span></span>
<span data-ttu-id="66013-200">Specifica una matrice di operazioni che possono essere eseguite usando la chiave aggiunta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66013-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="66013-201">Se non si specifica questo parametro, è possibile eseguire tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="66013-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="66013-202">I valori accettabili per questo parametro sono un elenco di operazioni chiave separate da virgole, come definito dalla specifica della chiave [Web JSON (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)</span><span class="sxs-lookup"><span data-stu-id="66013-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="66013-203">Crittografa</span><span class="sxs-lookup"><span data-stu-id="66013-203">Encrypt</span></span>
- <span data-ttu-id="66013-204">Decrittografa</span><span class="sxs-lookup"><span data-stu-id="66013-204">Decrypt</span></span>
- <span data-ttu-id="66013-205">Ritorno a capo</span><span class="sxs-lookup"><span data-stu-id="66013-205">Wrap</span></span>
- <span data-ttu-id="66013-206">Unwrap</span><span class="sxs-lookup"><span data-stu-id="66013-206">Unwrap</span></span>
- <span data-ttu-id="66013-207">Firma</span><span class="sxs-lookup"><span data-stu-id="66013-207">Sign</span></span>
- <span data-ttu-id="66013-208">Verifica</span><span class="sxs-lookup"><span data-stu-id="66013-208">Verify</span></span>

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

### <span data-ttu-id="66013-209">-Name</span><span class="sxs-lookup"><span data-stu-id="66013-209">-Name</span></span>
<span data-ttu-id="66013-210">Specifica il nome della chiave da aggiungere al vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="66013-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="66013-211">Questo cmdlet crea il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, al nome del vault delle chiavi e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="66013-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="66013-212">La lunghezza del nome deve essere di un massimo di 1 e 63 caratteri, contenente solo i caratteri 0-9, a-z, A-Z e - (il trattino).</span><span class="sxs-lookup"><span data-stu-id="66013-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="66013-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="66013-213">-NotBefore</span></span>
<span data-ttu-id="66013-214">Specifica l'ora, come oggetto **DateTime,** prima della quale non è possibile usare il tasto.</span><span class="sxs-lookup"><span data-stu-id="66013-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="66013-215">Questo parametro usa utc.</span><span class="sxs-lookup"><span data-stu-id="66013-215">This parameter uses UTC.</span></span> <span data-ttu-id="66013-216">Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="66013-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="66013-217">Se non si specifica questo parametro, la chiave può essere usata immediatamente.</span><span class="sxs-lookup"><span data-stu-id="66013-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="66013-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66013-218">-ResourceId</span></span>
<span data-ttu-id="66013-219">ID risorsa Vault.</span><span class="sxs-lookup"><span data-stu-id="66013-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="66013-220">-Size</span><span class="sxs-lookup"><span data-stu-id="66013-220">-Size</span></span>
<span data-ttu-id="66013-221">Dimensioni della chiave RSA, in bit.</span><span class="sxs-lookup"><span data-stu-id="66013-221">RSA key size, in bits.</span></span> <span data-ttu-id="66013-222">Se non è specificato, il servizio fornirà un valore predefinito sicuro.</span><span class="sxs-lookup"><span data-stu-id="66013-222">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="66013-223">-Tag</span><span class="sxs-lookup"><span data-stu-id="66013-223">-Tag</span></span>
<span data-ttu-id="66013-224">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="66013-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66013-225">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="66013-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="66013-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="66013-226">-VaultName</span></span>
<span data-ttu-id="66013-227">Specifica il nome del vault della chiave a cui il cmdlet aggiunge la chiave.</span><span class="sxs-lookup"><span data-stu-id="66013-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="66013-228">Questo cmdlet crea l'FQDN di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="66013-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="66013-229">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66013-229">-Confirm</span></span>
<span data-ttu-id="66013-230">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66013-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66013-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66013-231">-WhatIf</span></span>
<span data-ttu-id="66013-232">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66013-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66013-233">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66013-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66013-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66013-234">CommonParameters</span></span>
<span data-ttu-id="66013-235">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66013-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66013-236">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66013-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66013-237">INPUT</span><span class="sxs-lookup"><span data-stu-id="66013-237">INPUTS</span></span>

### <span data-ttu-id="66013-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="66013-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="66013-239">System.String</span><span class="sxs-lookup"><span data-stu-id="66013-239">System.String</span></span>

## <span data-ttu-id="66013-240">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66013-240">OUTPUTS</span></span>

### <span data-ttu-id="66013-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="66013-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="66013-242">NOTE</span><span class="sxs-lookup"><span data-stu-id="66013-242">NOTES</span></span>

## <span data-ttu-id="66013-243">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66013-243">RELATED LINKS</span></span>

[<span data-ttu-id="66013-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="66013-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="66013-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="66013-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="66013-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="66013-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

