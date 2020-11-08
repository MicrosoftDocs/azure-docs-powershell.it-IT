---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193266"
---
# <span data-ttu-id="98e73-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98e73-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="98e73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98e73-102">SYNOPSIS</span></span>
<span data-ttu-id="98e73-103">Ottiene le chiavi HSM gestite.</span><span class="sxs-lookup"><span data-stu-id="98e73-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="98e73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98e73-104">SYNTAX</span></span>

### <span data-ttu-id="98e73-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98e73-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="98e73-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="98e73-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="98e73-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="98e73-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="98e73-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="98e73-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="98e73-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e73-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="98e73-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98e73-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98e73-114">DESCRIPTION</span></span>
<span data-ttu-id="98e73-115">Il cmdlet **Get-AzManagedHsmKey** ottiene le chiavi HSM gestite da Azure.</span><span class="sxs-lookup"><span data-stu-id="98e73-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="98e73-116">Questo cmdlet consente di ottenere uno specifico **Microsoft. Azure. Commands. DataVault. Models. bundle** o un elenco di tutti gli oggetti del **portapacchi** in un HSM gestito o per versione.</span><span class="sxs-lookup"><span data-stu-id="98e73-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="98e73-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98e73-117">EXAMPLES</span></span>

### <span data-ttu-id="98e73-118">Esempio 1: ottenere tutte le chiavi in un HSM gestito</span><span class="sxs-lookup"><span data-stu-id="98e73-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="98e73-119">Vault/HSM nome: testmhsm nome: testkey001 versione: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled: true scade: not before: created: 10/14/2020 3:39:16 am updated: 10/14/2020 3:39:16 am livello di recupero: Recoverable + Purgeable Tags:</span><span class="sxs-lookup"><span data-stu-id="98e73-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="98e73-120">Vault/HSM nome: testmhsm nome: testkey002 versione: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled: false scade: 10/14/2022 8:13:29 non sono prima: 10/14/2020 8:13:33 am created: 10/14/2020 8:14:01 am updated: 10/14/2020 8:14:01 am livello di recupero: reversibile + Purgeable Tag: valore nome gravità alto Accounting vero</span><span class="sxs-lookup"><span data-stu-id="98e73-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="98e73-121">Questo comando consente di ottenere tutte le chiavi nell'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98e73-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="98e73-122">Esempio 2: ottenere la versione corrente di una chiave</span><span class="sxs-lookup"><span data-stu-id="98e73-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
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

<span data-ttu-id="98e73-123">Questo comando ottiene la versione corrente della chiave denominata testkey001 nell'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98e73-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="98e73-124">Nota: il nome HSM può essere ottenuto tramite $hsm. VaultName</span><span class="sxs-lookup"><span data-stu-id="98e73-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="98e73-125">Esempio 3: ottenere tutte le versioni di una chiave</span><span class="sxs-lookup"><span data-stu-id="98e73-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
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

<span data-ttu-id="98e73-126">Questo comando consente di ottenere tutte le versioni della chiave denominata testkey001 nell'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98e73-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="98e73-127">Esempio 4: ottenere una versione specifica di una chiave</span><span class="sxs-lookup"><span data-stu-id="98e73-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98e73-128">Questo comando ottiene una versione specifica della chiave denominata TestKey nell'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98e73-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="98e73-129">Dopo aver eseguito questo comando, è possibile esaminare varie proprietà della chiave spostando l'oggetto $Key.</span><span class="sxs-lookup"><span data-stu-id="98e73-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="98e73-130">Esempio 5: ottenere tutte le chiavi eliminate ma non eliminate per questo HSM gestito</span><span class="sxs-lookup"><span data-stu-id="98e73-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="98e73-131">Questo comando ottiene tutte le chiavi che sono state eliminate in precedenza, ma non eliminate, nell'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98e73-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="98e73-132">Esempio 6: ottiene la chiave TestKey che è stata eliminata ma non eliminata per questo HSM gestito</span><span class="sxs-lookup"><span data-stu-id="98e73-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="98e73-133">Questo comando ottiene la chiave TestKey che è stata eliminata in precedenza, ma non eliminata, nell'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98e73-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="98e73-134">Questo comando restituirà metadati, ad esempio la data di eliminazione, e la data di eliminazione pianificata di questa chiave eliminata.</span><span class="sxs-lookup"><span data-stu-id="98e73-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="98e73-135">Esempio 7: ottenere tutte le chiavi in un HSM gestito usando il filtro</span><span class="sxs-lookup"><span data-stu-id="98e73-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98e73-136">Questo comando consente di ottenere tutte le chiavi nell'HSM gestito denominato testmhsm che iniziano con "test".</span><span class="sxs-lookup"><span data-stu-id="98e73-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="98e73-137">Esempio 8: scaricare una chiave pubblica come file con estensione PEM</span><span class="sxs-lookup"><span data-stu-id="98e73-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98e73-138">È possibile scaricare la chiave pubblica di una chiave RSA specificando il `-OutFile` parametro.</span><span class="sxs-lookup"><span data-stu-id="98e73-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="98e73-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98e73-139">PARAMETERS</span></span>

### <span data-ttu-id="98e73-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e73-140">-DefaultProfile</span></span>
<span data-ttu-id="98e73-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98e73-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e73-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="98e73-142">-HsmName</span></span>
<span data-ttu-id="98e73-143">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="98e73-143">HSM name.</span></span> <span data-ttu-id="98e73-144">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="98e73-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e73-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="98e73-145">-IncludeVersions</span></span>
<span data-ttu-id="98e73-146">Specifica se includere le versioni della chiave nell'output.</span><span class="sxs-lookup"><span data-stu-id="98e73-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e73-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98e73-147">-InputObject</span></span>
<span data-ttu-id="98e73-148">Oggetto HSM.</span><span class="sxs-lookup"><span data-stu-id="98e73-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98e73-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="98e73-149">-InRemovedState</span></span>
<span data-ttu-id="98e73-150">Specifica se visualizzare le chiavi eliminate in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="98e73-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e73-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="98e73-151">-Name</span></span>
<span data-ttu-id="98e73-152">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="98e73-152">Key name.</span></span>
<span data-ttu-id="98e73-153">Cmdlet costruisce il nome di dominio completo di una chiave dal nome di HSM gestito, dall'ambiente selezionato e dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="98e73-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e73-154">-Outfile</span><span class="sxs-lookup"><span data-stu-id="98e73-154">-OutFile</span></span>
<span data-ttu-id="98e73-155">Specifica il file di output per cui questo cmdlet salva la chiave.</span><span class="sxs-lookup"><span data-stu-id="98e73-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="98e73-156">La chiave pubblica viene salvata in formato PEM per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="98e73-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="98e73-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98e73-157">-ResourceId</span></span>
<span data-ttu-id="98e73-158">ID risorsa HSM.</span><span class="sxs-lookup"><span data-stu-id="98e73-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98e73-159">-Versione</span><span class="sxs-lookup"><span data-stu-id="98e73-159">-Version</span></span>
<span data-ttu-id="98e73-160">Versione chiave.</span><span class="sxs-lookup"><span data-stu-id="98e73-160">Key version.</span></span>
<span data-ttu-id="98e73-161">Cmdlet costruisce il nome di dominio completo di una chiave da Name HSM gestito, ambiente attualmente selezionato, nome chiave e versione chiave.</span><span class="sxs-lookup"><span data-stu-id="98e73-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e73-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e73-162">CommonParameters</span></span>
<span data-ttu-id="98e73-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e73-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e73-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98e73-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e73-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98e73-165">INPUTS</span></span>

### <span data-ttu-id="98e73-166">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98e73-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98e73-167">System. String</span><span class="sxs-lookup"><span data-stu-id="98e73-167">System.String</span></span>

## <span data-ttu-id="98e73-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98e73-168">OUTPUTS</span></span>

### <span data-ttu-id="98e73-169">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98e73-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98e73-170">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98e73-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="98e73-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98e73-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="98e73-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="98e73-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="98e73-173">Note</span><span class="sxs-lookup"><span data-stu-id="98e73-173">NOTES</span></span>

## <span data-ttu-id="98e73-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98e73-174">RELATED LINKS</span></span>

[<span data-ttu-id="98e73-175">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98e73-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="98e73-176">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98e73-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="98e73-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98e73-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="98e73-178">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="98e73-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="98e73-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98e73-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="98e73-180">Ripristinare-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98e73-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)