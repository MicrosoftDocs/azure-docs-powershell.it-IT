---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203695"
---
# <span data-ttu-id="80029-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="80029-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="80029-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80029-102">SYNOPSIS</span></span>
<span data-ttu-id="80029-103">Crea una chiave in un HSM gestito o importa una chiave in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="80029-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="80029-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80029-104">SYNTAX</span></span>

### <span data-ttu-id="80029-105">InteractiveCreate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80029-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80029-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="80029-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80029-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="80029-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80029-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="80029-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80029-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="80029-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80029-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="80029-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80029-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80029-111">DESCRIPTION</span></span>
<span data-ttu-id="80029-112">Il cmdlet **Add-AzManagedHsmKey** crea una chiave in un HSM gestito in Azure Managed HSM o importa una chiave in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="80029-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="80029-113">Questo cmdlet consente di aggiungere chiavi utilizzando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="80029-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="80029-114">Creare una chiave con attributi chiave predefiniti</span><span class="sxs-lookup"><span data-stu-id="80029-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="80029-115">Creare una chiave con attributi chiave specificati</span><span class="sxs-lookup"><span data-stu-id="80029-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="80029-116">Importare una chiave da un file con estensione pfx nel computer.</span><span class="sxs-lookup"><span data-stu-id="80029-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="80029-117">Per ognuna di queste operazioni, è possibile specificare gli attributi chiave o accettare le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="80029-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="80029-118">Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nell'HSM gestito, la chiave originale viene aggiornata con i valori specificati per la nuova chiave.</span><span class="sxs-lookup"><span data-stu-id="80029-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="80029-119">Puoi accedere ai valori precedenti usando l'URI specifico della versione per la versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="80029-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="80029-120">Per informazioni sulle versioni chiave e sulla struttura URI, vedere [informazioni sulle chiavi e i segreti](http://go.microsoft.com/fwlink/?linkid=518560) nella documentazione dell'API REST di HSM gestita.</span><span class="sxs-lookup"><span data-stu-id="80029-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="80029-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80029-121">EXAMPLES</span></span>

### <span data-ttu-id="80029-122">Esempio 1: creare una chiave RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="80029-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="80029-123">Questo comando crea una chiave RSA-HSM denominata TestKey nel TestKey gestito di HSM denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="80029-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="80029-124">Esempio 2: creare un codice EC-HSM</span><span class="sxs-lookup"><span data-stu-id="80029-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="80029-125">Questo comando crea una chiave EC-HSM denominata TestKey usando la curva P-256 nel TestKey gestito di HSM denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="80029-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="80029-126">Esempio 3: creare una chiave Oct-HSM con valori non predefiniti</span><span class="sxs-lookup"><span data-stu-id="80029-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="80029-127">Con il primo comando vengono archiviati i valori decrittografati e verificati nella variabile $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="80029-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="80029-128">Il secondo comando crea un oggetto **DateTime** , definito in formato UTC, usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="80029-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="80029-129">L'oggetto specifica un periodo di due anni nel futuro.</span><span class="sxs-lookup"><span data-stu-id="80029-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="80029-130">Il comando archivia tale data nella variabile $Expires.</span><span class="sxs-lookup"><span data-stu-id="80029-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="80029-131">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="80029-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="80029-132">Il terzo comando crea un oggetto **DateTime** usando il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="80029-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="80029-133">Tale oggetto specifica l'ora UTC corrente.</span><span class="sxs-lookup"><span data-stu-id="80029-133">That object specifies current UTC time.</span></span> <span data-ttu-id="80029-134">Il comando archivia tale data nella variabile $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="80029-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="80029-135">Il comando finale crea una chiave denominata TestKey che è una chiave di Oct-HSM.</span><span class="sxs-lookup"><span data-stu-id="80029-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="80029-136">Il comando specifica i valori per le operazioni chiave consentite archiviate $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="80029-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="80029-137">Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per l'elevata gravità.</span><span class="sxs-lookup"><span data-stu-id="80029-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="80029-138">La nuova chiave è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="80029-138">The new key is disabled.</span></span> <span data-ttu-id="80029-139">Puoi abilitarlo usando il cmdlet **Update-AzManagedHsmKey** .</span><span class="sxs-lookup"><span data-stu-id="80029-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="80029-140">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80029-140">PARAMETERS</span></span>

### <span data-ttu-id="80029-141">-Curvename</span><span class="sxs-lookup"><span data-stu-id="80029-141">-CurveName</span></span>
<span data-ttu-id="80029-142">Specifica il nome della curva della crittografia a curva ellittica, questo valore è valido quando il tipo di pulsante è EC.</span><span class="sxs-lookup"><span data-stu-id="80029-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80029-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80029-143">-DefaultProfile</span></span>
<span data-ttu-id="80029-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80029-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80029-145">-Disable</span><span class="sxs-lookup"><span data-stu-id="80029-145">-Disable</span></span>
<span data-ttu-id="80029-146">Indica che la chiave che si sta aggiungendo è impostata su uno stato iniziale di disabled.</span><span class="sxs-lookup"><span data-stu-id="80029-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="80029-147">Qualsiasi tentativo di usare la chiave non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="80029-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="80029-148">Usare questo parametro se si precaricano le chiavi che si desidera abilitare in seguito.</span><span class="sxs-lookup"><span data-stu-id="80029-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="80029-149">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="80029-149">-Expires</span></span>
<span data-ttu-id="80029-150">Specifica la data di scadenza della chiave in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="80029-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="80029-151">Se non viene specificato, Key non scadrà.</span><span class="sxs-lookup"><span data-stu-id="80029-151">If not specified, key will not expire.</span></span>

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

### <span data-ttu-id="80029-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="80029-152">-HsmName</span></span>
<span data-ttu-id="80029-153">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="80029-153">HSM name.</span></span> <span data-ttu-id="80029-154">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="80029-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="80029-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80029-155">-InputObject</span></span>
<span data-ttu-id="80029-156">Oggetto HSM.</span><span class="sxs-lookup"><span data-stu-id="80029-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80029-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="80029-157">-KeyFilePassword</span></span>
<span data-ttu-id="80029-158">Password del file locale contenente il materiale chiave da importare.</span><span class="sxs-lookup"><span data-stu-id="80029-158">Password of the local file containing the key material to be imported.</span></span>

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

### <span data-ttu-id="80029-159">-FilePath</span><span class="sxs-lookup"><span data-stu-id="80029-159">-KeyFilePath</span></span>
<span data-ttu-id="80029-160">Percorso del file locale contenente il materiale della chiave da importare.</span><span class="sxs-lookup"><span data-stu-id="80029-160">Path to the local file containing the key material to be imported.</span></span>

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

### <span data-ttu-id="80029-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="80029-161">-KeyOps</span></span>
<span data-ttu-id="80029-162">Le operazioni che è possibile eseguire con la chiave.</span><span class="sxs-lookup"><span data-stu-id="80029-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="80029-163">Se non è presente, è possibile eseguire tutte le operazioni.</span><span class="sxs-lookup"><span data-stu-id="80029-163">If not present, all operations can be performed.</span></span>

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

### <span data-ttu-id="80029-164">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="80029-164">-KeyType</span></span>
<span data-ttu-id="80029-165">Specifica il tipo di chiave di questa chiave.</span><span class="sxs-lookup"><span data-stu-id="80029-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80029-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="80029-166">-Name</span></span>
<span data-ttu-id="80029-167">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="80029-167">Key name.</span></span>
<span data-ttu-id="80029-168">Cmdlet costruisce il nome di dominio completo di una chiave dal nome di HSM gestito, dall'ambiente selezionato e dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="80029-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="80029-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="80029-169">-NotBefore</span></span>
<span data-ttu-id="80029-170">Ora UTC prima della quale non è possibile usare il tasto.</span><span class="sxs-lookup"><span data-stu-id="80029-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="80029-171">Se non è specificato, non ci sono limitazioni.</span><span class="sxs-lookup"><span data-stu-id="80029-171">If not specified, there is no limitation.</span></span>

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

### <span data-ttu-id="80029-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80029-172">-ResourceId</span></span>
<span data-ttu-id="80029-173">ID risorsa HSM.</span><span class="sxs-lookup"><span data-stu-id="80029-173">HSM Resource Id.</span></span>

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

### <span data-ttu-id="80029-174">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="80029-174">-Size</span></span>
<span data-ttu-id="80029-175">Dimensioni chiave RSA in bit.</span><span class="sxs-lookup"><span data-stu-id="80029-175">RSA key size, in bits.</span></span>
<span data-ttu-id="80029-176">Se non viene specificato, il servizio fornirà un valore predefinito sicuro.</span><span class="sxs-lookup"><span data-stu-id="80029-176">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="80029-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="80029-177">-Tag</span></span>
<span data-ttu-id="80029-178">Hashtable che rappresenta i tag chiave.</span><span class="sxs-lookup"><span data-stu-id="80029-178">A hashtable representing key tags.</span></span>

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

### <span data-ttu-id="80029-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80029-179">-Confirm</span></span>
<span data-ttu-id="80029-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80029-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80029-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80029-181">-WhatIf</span></span>
<span data-ttu-id="80029-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80029-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80029-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80029-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80029-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80029-184">CommonParameters</span></span>
<span data-ttu-id="80029-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80029-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80029-186">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80029-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80029-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80029-187">INPUTS</span></span>

### <span data-ttu-id="80029-188">Microsoft. Azure. Commands. Vault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="80029-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="80029-189">System. String</span><span class="sxs-lookup"><span data-stu-id="80029-189">System.String</span></span>

## <span data-ttu-id="80029-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80029-190">OUTPUTS</span></span>

### <span data-ttu-id="80029-191">Microsoft. Azure. Commands. Vault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="80029-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="80029-192">Note</span><span class="sxs-lookup"><span data-stu-id="80029-192">NOTES</span></span>

## <span data-ttu-id="80029-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80029-193">RELATED LINKS</span></span>

[<span data-ttu-id="80029-194">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="80029-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="80029-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="80029-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="80029-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="80029-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="80029-197">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="80029-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="80029-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="80029-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="80029-199">Ripristinare-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="80029-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
