---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202366"
---
# <span data-ttu-id="ca0ee-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="ca0ee-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="ca0ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ca0ee-103">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-103">Gets information about a server.</span></span>

## <span data-ttu-id="ca0ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca0ee-104">SYNTAX</span></span>

### <span data-ttu-id="ca0ee-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca0ee-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca0ee-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ca0ee-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca0ee-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca0ee-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca0ee-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="ca0ee-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca0ee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca0ee-109">DESCRIPTION</span></span>
<span data-ttu-id="ca0ee-110">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-110">Gets information about a server.</span></span>

## <span data-ttu-id="ca0ee-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca0ee-111">EXAMPLES</span></span>

### <span data-ttu-id="ca0ee-112">Esempio 1: elencare tutti i MariaDB in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ca0ee-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="ca0ee-113">Questo comando elenca tutti i MariaDB in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="ca0ee-114">Esempio 2: elencare tutti i MariaDB in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ca0ee-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="ca0ee-115">Questo comando elenca tutti i MariaDB in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="ca0ee-116">Esempio 3: ottenere un MariaDB</span><span class="sxs-lookup"><span data-stu-id="ca0ee-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="ca0ee-117">Questo comando ottiene un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="ca0ee-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca0ee-118">PARAMETERS</span></span>

### <span data-ttu-id="ca0ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca0ee-119">-DefaultProfile</span></span>
<span data-ttu-id="ca0ee-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca0ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca0ee-121">-InputObject</span></span>
<span data-ttu-id="ca0ee-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca0ee-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca0ee-123">-Name</span></span>
<span data-ttu-id="ca0ee-124">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-124">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca0ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca0ee-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ca0ee-127">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0ee-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca0ee-128">-SubscriptionId</span></span>
<span data-ttu-id="ca0ee-129">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-129">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca0ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca0ee-130">CommonParameters</span></span>
<span data-ttu-id="ca0ee-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca0ee-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca0ee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca0ee-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca0ee-133">INPUTS</span></span>

### <span data-ttu-id="ca0ee-134">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="ca0ee-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ca0ee-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca0ee-135">OUTPUTS</span></span>

### <span data-ttu-id="ca0ee-136">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="ca0ee-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ca0ee-137">Note</span><span class="sxs-lookup"><span data-stu-id="ca0ee-137">NOTES</span></span>

<span data-ttu-id="ca0ee-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca0ee-138">ALIASES</span></span>

<span data-ttu-id="ca0ee-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca0ee-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca0ee-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca0ee-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca0ee-142">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ca0ee-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca0ee-143">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ca0ee-144">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ca0ee-145">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ca0ee-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ca0ee-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca0ee-147">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ca0ee-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ca0ee-149">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ca0ee-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ca0ee-151">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ca0ee-152">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ca0ee-153">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca0ee-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ca0ee-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca0ee-154">RELATED LINKS</span></span>

