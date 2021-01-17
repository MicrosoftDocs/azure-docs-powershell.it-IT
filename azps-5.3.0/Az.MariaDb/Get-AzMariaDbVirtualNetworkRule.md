---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476132"
---
# <span data-ttu-id="62057-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="62057-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="62057-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62057-102">SYNOPSIS</span></span>
<span data-ttu-id="62057-103">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="62057-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="62057-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62057-104">SYNTAX</span></span>

### <span data-ttu-id="62057-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62057-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="62057-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="62057-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="62057-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="62057-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="62057-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62057-108">DESCRIPTION</span></span>
<span data-ttu-id="62057-109">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="62057-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="62057-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62057-110">EXAMPLES</span></span>

### <span data-ttu-id="62057-111">Esempio 1: elencare tutte le regole di rete virtuale in un MariaDB</span><span class="sxs-lookup"><span data-stu-id="62057-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="62057-112">Questo comando elenca tutta la regola di rete virtuale in un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="62057-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="62057-113">Esempio 2: ottenere la regola di rete virtuale in un MariaDB</span><span class="sxs-lookup"><span data-stu-id="62057-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="62057-114">Questo comando ottiene la regola di rete virtuale in un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="62057-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="62057-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62057-115">PARAMETERS</span></span>

### <span data-ttu-id="62057-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62057-116">-DefaultProfile</span></span>
<span data-ttu-id="62057-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62057-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62057-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62057-118">-InputObject</span></span>
<span data-ttu-id="62057-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="62057-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="62057-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="62057-120">-Name</span></span>
<span data-ttu-id="62057-121">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="62057-121">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62057-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62057-122">-PassThru</span></span>
<span data-ttu-id="62057-123">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="62057-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="62057-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62057-124">-ResourceGroupName</span></span>
<span data-ttu-id="62057-125">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="62057-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="62057-126">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="62057-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="62057-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="62057-127">-ServerName</span></span>
<span data-ttu-id="62057-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="62057-128">The name of the server.</span></span>

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

### <span data-ttu-id="62057-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62057-129">-SubscriptionId</span></span>
<span data-ttu-id="62057-130">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="62057-130">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62057-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62057-131">CommonParameters</span></span>
<span data-ttu-id="62057-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62057-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62057-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62057-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62057-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62057-134">INPUTS</span></span>

### <span data-ttu-id="62057-135">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="62057-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="62057-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62057-136">OUTPUTS</span></span>

### <span data-ttu-id="62057-137">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="62057-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="62057-138">Note</span><span class="sxs-lookup"><span data-stu-id="62057-138">NOTES</span></span>

<span data-ttu-id="62057-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="62057-139">ALIASES</span></span>

<span data-ttu-id="62057-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62057-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62057-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="62057-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62057-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62057-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62057-143">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="62057-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="62057-144">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="62057-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="62057-145">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="62057-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="62057-146">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="62057-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="62057-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="62057-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="62057-148">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="62057-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="62057-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="62057-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="62057-150">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="62057-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="62057-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="62057-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="62057-152">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="62057-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="62057-153">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="62057-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="62057-154">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="62057-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="62057-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62057-155">RELATED LINKS</span></span>

