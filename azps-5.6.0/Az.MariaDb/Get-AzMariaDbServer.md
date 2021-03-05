---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: ac7ea6689b18c14cca2213e3856cb093f5f36287
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970653"
---
# <span data-ttu-id="9c968-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="9c968-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="9c968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c968-102">SYNOPSIS</span></span>
<span data-ttu-id="9c968-103">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="9c968-103">Gets information about a server.</span></span>

## <span data-ttu-id="9c968-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c968-104">SYNTAX</span></span>

### <span data-ttu-id="9c968-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c968-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c968-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9c968-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c968-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9c968-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9c968-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="9c968-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c968-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c968-109">DESCRIPTION</span></span>
<span data-ttu-id="9c968-110">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="9c968-110">Gets information about a server.</span></span>

## <span data-ttu-id="9c968-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c968-111">EXAMPLES</span></span>

### <span data-ttu-id="9c968-112">Esempio 1: Elencare tutte le mariaDB sotto un abbonamento</span><span class="sxs-lookup"><span data-stu-id="9c968-112">Example 1: List all MariaDB under a subscriptions</span></span>
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

<span data-ttu-id="9c968-113">Questo comando elenca tutti i database di MariaDB sotto un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9c968-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="9c968-114">Esempio 2: Elencare tutte le mariaDB in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9c968-114">Example 2: List all MariaDB under a resource group</span></span>
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

<span data-ttu-id="9c968-115">Questo comando elenca tutte le mariaDB in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c968-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="9c968-116">Esempio 3: Ottenere un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="9c968-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="9c968-117">Questo comando ottiene un oggetto Db.</span><span class="sxs-lookup"><span data-stu-id="9c968-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="9c968-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c968-118">PARAMETERS</span></span>

### <span data-ttu-id="9c968-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c968-119">-DefaultProfile</span></span>
<span data-ttu-id="9c968-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c968-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c968-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c968-121">-InputObject</span></span>
<span data-ttu-id="9c968-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9c968-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9c968-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9c968-123">-Name</span></span>
<span data-ttu-id="9c968-124">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="9c968-124">The name of the server.</span></span>

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

### <span data-ttu-id="9c968-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c968-125">-ResourceGroupName</span></span>
<span data-ttu-id="9c968-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c968-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9c968-127">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="9c968-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9c968-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c968-128">-SubscriptionId</span></span>
<span data-ttu-id="9c968-129">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c968-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="9c968-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c968-130">CommonParameters</span></span>
<span data-ttu-id="9c968-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c968-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c968-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c968-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c968-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c968-133">INPUTS</span></span>

### <span data-ttu-id="9c968-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="9c968-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="9c968-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c968-135">OUTPUTS</span></span>

### <span data-ttu-id="9c968-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="9c968-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="9c968-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c968-137">NOTES</span></span>

<span data-ttu-id="9c968-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9c968-138">ALIASES</span></span>

<span data-ttu-id="9c968-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="9c968-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c968-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9c968-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c968-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9c968-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c968-142">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9c968-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c968-143">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="9c968-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9c968-144">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="9c968-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9c968-145">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="9c968-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9c968-146">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="9c968-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c968-147">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="9c968-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9c968-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c968-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9c968-149">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="9c968-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9c968-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9c968-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9c968-151">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="9c968-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9c968-152">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9c968-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="9c968-153">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9c968-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9c968-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c968-154">RELATED LINKS</span></span>

