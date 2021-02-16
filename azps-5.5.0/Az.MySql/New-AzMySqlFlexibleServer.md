---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: c544ce2ea5f02d5c0b3b7aee41e19992a0dc356d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192111"
---
# <span data-ttu-id="ca805-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="ca805-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="ca805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca805-102">SYNOPSIS</span></span>
<span data-ttu-id="ca805-103">Crea un nuovo server flessibile MySQL.</span><span class="sxs-lookup"><span data-stu-id="ca805-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="ca805-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca805-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca805-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca805-105">DESCRIPTION</span></span>
<span data-ttu-id="ca805-106">Crea un nuovo server flessibile MySQL.</span><span class="sxs-lookup"><span data-stu-id="ca805-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="ca805-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca805-107">EXAMPLES</span></span>

### <span data-ttu-id="ca805-108">Esempio 1: Creare un nuovo server flessibile MySql con argomenti</span><span class="sxs-lookup"><span data-stu-id="ca805-108">Example 1: Create a new MySql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### <span data-ttu-id="ca805-109">Esempio 2: Creare un nuovo server flessibile MySql con impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="ca805-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="ca805-110">Questo cmdlet crea un server flessibile MySql con valori dei parametri predefiniti ed effettua il provisioning del server all'interno di una nuova rete virtuale e ha una subnet delegata al server.</span><span class="sxs-lookup"><span data-stu-id="ca805-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="ca805-111">Il valore predefinito per la posizione è Stati Uniti occidentali 2, SKU è Standard_B1ms, il livello SKU è a scatto sferzante e la dimensione di archiviazione è 10GiB.</span><span class="sxs-lookup"><span data-stu-id="ca805-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="ca805-112">Se si vuole trovare la password generata automaticamente per il server, usare ConvertFrom-SecureString per convertire la proprietà "SecuredPassword" in testo normale.</span><span class="sxs-lookup"><span data-stu-id="ca805-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="ca805-113">(Ad esempio, $server. SecuredPassword | ConvertFrom-SecureString -AsPtextText)</span><span class="sxs-lookup"><span data-stu-id="ca805-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="ca805-114">Esempio 3: Creare un nuovo server flessibile MySql con una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ca805-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="ca805-115">Questo cmdlet crea un server flessibile MySql con id vnet o nome vnet fornito da un utente.</span><span class="sxs-lookup"><span data-stu-id="ca805-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="ca805-116">Se la rete virtuale non esiste, il cmdlet ne crea una.</span><span class="sxs-lookup"><span data-stu-id="ca805-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="ca805-117">Esempio 4: Creare un nuovo server flessibile MySql con rete virtuale e nome subnet</span><span class="sxs-lookup"><span data-stu-id="ca805-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="ca805-118">Questo cmdlet crea un server flessibile MySql con nome vnet, nome subnet, prefisso vnet e prefisso della subnet.</span><span class="sxs-lookup"><span data-stu-id="ca805-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="ca805-119">Se la rete virtuale e la subnet non esistono, il cmdlet ne crea una.</span><span class="sxs-lookup"><span data-stu-id="ca805-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="ca805-120">Esempio 7: Creare un nuovo server flessibile MySql con accesso pubblico a tutti gli IP</span><span class="sxs-lookup"><span data-stu-id="ca805-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="ca805-121">Questo cmdlet crea un server flessibile MySql aperto a tutti gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="ca805-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="ca805-122">Esempio 8: Creare un nuovo server flessibile MySql con il firewall</span><span class="sxs-lookup"><span data-stu-id="ca805-122">Example 8: Create a new MySql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="ca805-123">Questo cmdlet crea un server flessibile MySql aperto agli indirizzi IP specificati.</span><span class="sxs-lookup"><span data-stu-id="ca805-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="ca805-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca805-124">PARAMETERS</span></span>

### <span data-ttu-id="ca805-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ca805-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ca805-126">Password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="ca805-126">The password of the administrator.</span></span>
<span data-ttu-id="ca805-127">Minimo 8 caratteri e massimo 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ca805-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="ca805-128">La password deve contenere caratteri di tre delle categorie seguenti: lettere maiuscole inglesi, lettere minuscole inglesi, numeri e caratteri non alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="ca805-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ca805-129">-AdministratorUserName</span></span>
<span data-ttu-id="ca805-130">Nome utente dell'amministratore per il server.</span><span class="sxs-lookup"><span data-stu-id="ca805-130">Administrator username for the server.</span></span>
<span data-ttu-id="ca805-131">Una volta impostata, non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="ca805-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="ca805-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca805-132">-AsJob</span></span>
<span data-ttu-id="ca805-133">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="ca805-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="ca805-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ca805-134">-BackupRetentionDay</span></span>
<span data-ttu-id="ca805-135">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="ca805-135">Backup retention days for the server.</span></span>
<span data-ttu-id="ca805-136">Il numero dei giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="ca805-136">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca805-137">-DefaultProfile</span></span>
<span data-ttu-id="ca805-138">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca805-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-139">-HighAvailability</span><span class="sxs-lookup"><span data-stu-id="ca805-139">-HighAvailability</span></span>
<span data-ttu-id="ca805-140">Abilitare o disabilitare la funzionalità disponibilità elevata.</span><span class="sxs-lookup"><span data-stu-id="ca805-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="ca805-141">Il valore predefinito è Disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ca805-141">Default value is Disabled.</span></span>
<span data-ttu-id="ca805-142">Impostazione predefinita: Disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ca805-142">Default: Disabled.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-143">-Location</span><span class="sxs-lookup"><span data-stu-id="ca805-143">-Location</span></span>
<span data-ttu-id="ca805-144">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca805-144">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ca805-145">-Name</span><span class="sxs-lookup"><span data-stu-id="ca805-145">-Name</span></span>
<span data-ttu-id="ca805-146">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ca805-146">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca805-147">-NoWait</span></span>
<span data-ttu-id="ca805-148">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="ca805-148">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ca805-149">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="ca805-149">-PublicAccess</span></span>
<span data-ttu-id="ca805-150">Determina l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="ca805-150">Determines the public access.</span></span>
<span data-ttu-id="ca805-151">Immettere un singolo o un intervallo di indirizzi IP da includere nell'elenco degli indirizzi IP consentiti.</span><span class="sxs-lookup"><span data-stu-id="ca805-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="ca805-152">Gli intervalli di indirizzi IP devono essere separati da trattini e non devono contenere spazi.</span><span class="sxs-lookup"><span data-stu-id="ca805-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="ca805-153">Se si specifica 0.0.0.0, l'accesso al server è possibile da qualsiasi risorsa distribuita in Azure.</span><span class="sxs-lookup"><span data-stu-id="ca805-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="ca805-154">Se si specifica nessun indirizzo IP, il server viene impostato in modalità di accesso pubblico, ma non viene creata una regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="ca805-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="ca805-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca805-155">-ResourceGroupName</span></span>
<span data-ttu-id="ca805-156">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ca805-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ca805-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="ca805-157">-Sku</span></span>
<span data-ttu-id="ca805-158">Il nome della sKU, in genere livello + famiglia + core, ad esempio Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="ca805-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="ca805-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ca805-159">-SkuTier</span></span>
<span data-ttu-id="ca805-160">Livello di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="ca805-160">Compute tier of the server.</span></span>
<span data-ttu-id="ca805-161">Valori accettati: Burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="ca805-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="ca805-162">Impostazione predefinita: a scatto a scatto pieno.</span><span class="sxs-lookup"><span data-stu-id="ca805-162">Default: Burstable.</span></span>

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

### <span data-ttu-id="ca805-163">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ca805-163">-StorageInMb</span></span>
<span data-ttu-id="ca805-164">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="ca805-164">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-165">-Subnet</span><span class="sxs-lookup"><span data-stu-id="ca805-165">-Subnet</span></span>
<span data-ttu-id="ca805-166">Nome o ID di una subnet esistente o nome di una nuova subnet da creare.</span><span class="sxs-lookup"><span data-stu-id="ca805-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="ca805-167">Tenere presente che la subnet verrà delegata a Microsoft.DBforMySQL/flexibleServers.</span><span class="sxs-lookup"><span data-stu-id="ca805-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="ca805-168">Dopo la delega, la subnet non può essere usata per altri tipi di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="ca805-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="ca805-169">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="ca805-169">-SubnetPrefix</span></span>
<span data-ttu-id="ca805-170">Prefisso dell'indirizzo IP subnet da usare quando si crea una nuova vnet in formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="ca805-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="ca805-171">Il valore predefinito è 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="ca805-171">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="ca805-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca805-172">-SubscriptionId</span></span>
<span data-ttu-id="ca805-173">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca805-173">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca805-174">-Tag</span></span>
<span data-ttu-id="ca805-175">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="ca805-175">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-176">-Version</span><span class="sxs-lookup"><span data-stu-id="ca805-176">-Version</span></span>
<span data-ttu-id="ca805-177">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="ca805-177">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-178">-Vnet</span><span class="sxs-lookup"><span data-stu-id="ca805-178">-Vnet</span></span>
<span data-ttu-id="ca805-179">Nome o ID di una rete virtuale esistente o nome di una nuova rete virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="ca805-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="ca805-180">Il nome deve contenere da 2 a 64 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ca805-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="ca805-181">Il nome deve iniziare con una lettera o un numero, terminare con una lettera, un numero o un carattere di sottolineatura e può contenere solo lettere, numeri, caratteri di sottolineatura, punti o trattini.</span><span class="sxs-lookup"><span data-stu-id="ca805-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="ca805-182">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="ca805-182">-VnetPrefix</span></span>
<span data-ttu-id="ca805-183">Prefisso dell'indirizzo IP da usare quando si crea una nuova vnet in formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="ca805-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="ca805-184">Il valore predefinito è 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="ca805-184">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="ca805-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca805-185">-Confirm</span></span>
<span data-ttu-id="ca805-186">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca805-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca805-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca805-187">-WhatIf</span></span>
<span data-ttu-id="ca805-188">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca805-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca805-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca805-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca805-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca805-190">CommonParameters</span></span>
<span data-ttu-id="ca805-191">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca805-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca805-192">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca805-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca805-193">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca805-193">INPUTS</span></span>

## <span data-ttu-id="ca805-194">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca805-194">OUTPUTS</span></span>

### <span data-ttu-id="ca805-195">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ca805-195">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="ca805-196">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca805-196">NOTES</span></span>

<span data-ttu-id="ca805-197">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca805-197">ALIASES</span></span>

## <span data-ttu-id="ca805-198">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca805-198">RELATED LINKS</span></span>

