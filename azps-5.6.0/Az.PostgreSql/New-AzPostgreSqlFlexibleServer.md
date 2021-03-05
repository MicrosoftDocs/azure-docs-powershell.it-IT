---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c40f8ad000bca3026860ebc328be57e6931a1546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987697"
---
# <span data-ttu-id="b3c9e-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="b3c9e-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="b3c9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c9e-103">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-103">Creates a new server.</span></span>

## <span data-ttu-id="b3c9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3c9e-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-Zone <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b3c9e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3c9e-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c9e-106">Crea un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-106">Creates a new server.</span></span>

## <span data-ttu-id="b3c9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3c9e-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c9e-108">Esempio 1: Creare un nuovo server flessibile PostgreSql con argomenti</span><span class="sxs-lookup"><span data-stu-id="b3c9e-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="b3c9e-109">Esempio 2: Creare un nuovo server flessibile PostgreSql con impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="b3c9e-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="b3c9e-110">Questo cmdlet crea un server flessibile PostgreSql con valori dei parametri predefiniti ed effettua il provisioning del server all'interno di una nuova rete virtuale e ha una subnet delegata al server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="b3c9e-111">Il valore predefinito per la posizione è Stati Uniti occidentali 2, SKU è Standard_D2s_v3, il livello SKU è GeneralPurpose e le dimensioni di archiviazione sono 128GiB.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="b3c9e-112">Se si vuole trovare la password generata automaticamente per il server, usare ConvertFrom-SecureString per convertire la proprietà "SecuredPassword" in testo normale.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="b3c9e-113">(Ad esempio, $server. SecuredPassword | ConvertFrom-SecureString -AsPtextText)</span><span class="sxs-lookup"><span data-stu-id="b3c9e-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="b3c9e-114">Esempio 3: Creare un nuovo server flessibile PostgreSql con una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b3c9e-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="b3c9e-115">Questo cmdlet crea un server flessibile PostgreSql con id vnet o nome vnet fornito da un utente.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="b3c9e-116">Se la rete virtuale non esiste, il cmdlet ne crea una.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="b3c9e-117">Esempio 4: Creare un nuovo server flessibile PostgreSql con rete virtuale e nome subnet</span><span class="sxs-lookup"><span data-stu-id="b3c9e-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="b3c9e-118">Questo cmdlet crea un server flessibile PostgreSql con nome vnet, nome subnet, prefisso vnet e prefisso subnet.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="b3c9e-119">Se la rete virtuale e la subnet non esistono, il cmdlet ne crea una.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="b3c9e-120">Esempio 7: Creare un nuovo server flessibile PostgreSql con accesso pubblico a tutti gli IP</span><span class="sxs-lookup"><span data-stu-id="b3c9e-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="b3c9e-121">Questo cmdlet crea un server flessibile PostgreSql aperto a tutti gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="b3c9e-122">Esempio 8: Creare un nuovo server flessibile PostgreSql con il firewall</span><span class="sxs-lookup"><span data-stu-id="b3c9e-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="b3c9e-123">Questo cmdlet crea un server flessibile PostgreSql aperto agli indirizzi IP specificati.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="b3c9e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3c9e-124">PARAMETERS</span></span>

### <span data-ttu-id="b3c9e-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b3c9e-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b3c9e-126">Password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-126">The password of the administrator.</span></span>
<span data-ttu-id="b3c9e-127">Minimo 8 caratteri e massimo 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b3c9e-128">La password deve contenere caratteri di tre delle categorie seguenti: lettere maiuscole inglesi, lettere minuscole inglesi, numeri e caratteri non alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="b3c9e-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b3c9e-129">-AdministratorUserName</span></span>
<span data-ttu-id="b3c9e-130">Nome utente dell'amministratore per il server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-130">Administrator username for the server.</span></span>
<span data-ttu-id="b3c9e-131">Una volta impostata, non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b3c9e-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3c9e-132">-AsJob</span></span>
<span data-ttu-id="b3c9e-133">Eseguire il comando come processo.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="b3c9e-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b3c9e-134">-BackupRetentionDay</span></span>
<span data-ttu-id="b3c9e-135">Giorni di conservazione del backup per il server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-135">Backup retention days for the server.</span></span>
<span data-ttu-id="b3c9e-136">Il numero dei giorni è compreso tra 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="b3c9e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c9e-137">-DefaultProfile</span></span>
<span data-ttu-id="b3c9e-138">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c9e-139">-Location</span><span class="sxs-lookup"><span data-stu-id="b3c9e-139">-Location</span></span>
<span data-ttu-id="b3c9e-140">Posizione in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b3c9e-141">-Name</span><span class="sxs-lookup"><span data-stu-id="b3c9e-141">-Name</span></span>
<span data-ttu-id="b3c9e-142">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-142">The name of the server.</span></span>

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

### <span data-ttu-id="b3c9e-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3c9e-143">-NoWait</span></span>
<span data-ttu-id="b3c9e-144">Eseguire il comando in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b3c9e-145">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="b3c9e-145">-PublicAccess</span></span>
<span data-ttu-id="b3c9e-146">Determina l'accesso pubblico.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-146">Determines the public access.</span></span>
<span data-ttu-id="b3c9e-147">Immettere un singolo o un intervallo di indirizzi IP da includere nell'elenco degli indirizzi IP consentiti.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="b3c9e-148">Gli intervalli di indirizzi IP devono essere separati da trattini e non devono contenere spazi.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="b3c9e-149">Se si specifica 0.0.0.0, l'accesso al server è possibile da qualsiasi risorsa distribuita in Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="b3c9e-150">Se si specifica nessun indirizzo IP, il server viene impostato in modalità di accesso pubblico, ma non viene creata una regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="b3c9e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c9e-151">-ResourceGroupName</span></span>
<span data-ttu-id="b3c9e-152">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b3c9e-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="b3c9e-153">-Sku</span></span>
<span data-ttu-id="b3c9e-154">Il nome della sKU, in genere livello + famiglia + core, ad esempio Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="b3c9e-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b3c9e-155">-SkuTier</span></span>
<span data-ttu-id="b3c9e-156">Livello di calcolo del server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-156">Compute tier of the server.</span></span>
<span data-ttu-id="b3c9e-157">Valori accettati: Burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="b3c9e-158">Impostazione predefinita: esplosa.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="b3c9e-159">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b3c9e-159">-StorageInMb</span></span>
<span data-ttu-id="b3c9e-160">Spazio di archiviazione massimo consentito per un server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-160">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="b3c9e-161">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b3c9e-161">-Subnet</span></span>
<span data-ttu-id="b3c9e-162">Nome o ID di una subnet esistente o nome di una nuova subnet da creare.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="b3c9e-163">Tenere presente che la subnet verrà delegata a Microsoft.DBforPostgreSQL/flexibleServers.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="b3c9e-164">Dopo la delega, la subnet non può essere usata per altri tipi di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="b3c9e-165">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="b3c9e-165">-SubnetPrefix</span></span>
<span data-ttu-id="b3c9e-166">Prefisso dell'indirizzo IP subnet da usare quando si crea una nuova vnet in formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="b3c9e-167">Il valore predefinito è 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="b3c9e-168">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3c9e-168">-SubscriptionId</span></span>
<span data-ttu-id="b3c9e-169">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-169">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b3c9e-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3c9e-170">-Tag</span></span>
<span data-ttu-id="b3c9e-171">Metadati specifici dell'applicazione sotto forma di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-171">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="b3c9e-172">-Version</span><span class="sxs-lookup"><span data-stu-id="b3c9e-172">-Version</span></span>
<span data-ttu-id="b3c9e-173">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-173">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c9e-174">-Vnet</span><span class="sxs-lookup"><span data-stu-id="b3c9e-174">-Vnet</span></span>
<span data-ttu-id="b3c9e-175">Nome o ID di una rete virtuale esistente o nome di una nuova rete virtuale da creare.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="b3c9e-176">Il nome deve contenere da 2 a 64 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="b3c9e-177">Il nome deve iniziare con una lettera o un numero, terminare con una lettera, un numero o un carattere di sottolineatura e può contenere solo lettere, numeri, caratteri di sottolineatura, punti o trattini.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="b3c9e-178">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="b3c9e-178">-VnetPrefix</span></span>
<span data-ttu-id="b3c9e-179">Prefisso dell'indirizzo IP da usare quando si crea una nuova vnet in formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="b3c9e-180">Il valore predefinito è 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="b3c9e-181">-Zone</span><span class="sxs-lookup"><span data-stu-id="b3c9e-181">-Zone</span></span>
<span data-ttu-id="b3c9e-182">Area di disponibilità in cui effettuare il provisioning della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-182">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="b3c9e-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3c9e-183">-Confirm</span></span>
<span data-ttu-id="b3c9e-184">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3c9e-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3c9e-185">-WhatIf</span></span>
<span data-ttu-id="b3c9e-186">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3c9e-187">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3c9e-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c9e-188">CommonParameters</span></span>
<span data-ttu-id="b3c9e-189">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c9e-190">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3c9e-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c9e-191">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3c9e-191">INPUTS</span></span>

## <span data-ttu-id="b3c9e-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3c9e-192">OUTPUTS</span></span>

### <span data-ttu-id="b3c9e-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b3c9e-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="b3c9e-194">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3c9e-194">NOTES</span></span>

<span data-ttu-id="b3c9e-195">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b3c9e-195">ALIASES</span></span>

## <span data-ttu-id="b3c9e-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3c9e-196">RELATED LINKS</span></span>

