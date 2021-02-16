---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190239"
---
# <span data-ttu-id="94f18-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="94f18-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="94f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f18-102">SYNOPSIS</span></span>
<span data-ttu-id="94f18-103">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="94f18-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="94f18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94f18-104">SYNTAX</span></span>

### <span data-ttu-id="94f18-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94f18-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="94f18-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="94f18-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="94f18-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94f18-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="94f18-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94f18-108">DESCRIPTION</span></span>
<span data-ttu-id="94f18-109">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="94f18-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="94f18-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94f18-110">EXAMPLES</span></span>

### <span data-ttu-id="94f18-111">Esempio 1: Elencare tutte le regole di rete virtuale in un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="94f18-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="94f18-112">Questo comando elenca tutte le regole di rete virtuale in un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="94f18-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="94f18-113">Esempio 2: Ottenere una regola di rete virtuale in un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="94f18-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="94f18-114">Questo comando recupera la regola della rete virtuale in un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="94f18-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="94f18-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94f18-115">PARAMETERS</span></span>

### <span data-ttu-id="94f18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f18-116">-DefaultProfile</span></span>
<span data-ttu-id="94f18-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94f18-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f18-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94f18-118">-InputObject</span></span>
<span data-ttu-id="94f18-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="94f18-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94f18-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94f18-120">-Name</span></span>
<span data-ttu-id="94f18-121">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="94f18-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="94f18-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94f18-122">-PassThru</span></span>
<span data-ttu-id="94f18-123">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="94f18-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="94f18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f18-124">-ResourceGroupName</span></span>
<span data-ttu-id="94f18-125">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="94f18-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="94f18-126">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="94f18-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="94f18-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="94f18-127">-ServerName</span></span>
<span data-ttu-id="94f18-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="94f18-128">The name of the server.</span></span>

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

### <span data-ttu-id="94f18-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94f18-129">-SubscriptionId</span></span>
<span data-ttu-id="94f18-130">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="94f18-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="94f18-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f18-131">CommonParameters</span></span>
<span data-ttu-id="94f18-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f18-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f18-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94f18-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f18-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="94f18-134">INPUTS</span></span>

### <span data-ttu-id="94f18-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="94f18-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="94f18-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94f18-136">OUTPUTS</span></span>

### <span data-ttu-id="94f18-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="94f18-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="94f18-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="94f18-138">NOTES</span></span>

<span data-ttu-id="94f18-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="94f18-139">ALIASES</span></span>

<span data-ttu-id="94f18-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="94f18-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94f18-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="94f18-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94f18-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94f18-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94f18-143">INPUTOBJECT <IMariaDbIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="94f18-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94f18-144">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="94f18-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="94f18-145">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="94f18-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="94f18-146">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="94f18-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="94f18-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="94f18-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94f18-148">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="94f18-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="94f18-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="94f18-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="94f18-150">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="94f18-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="94f18-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="94f18-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="94f18-152">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="94f18-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="94f18-153">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="94f18-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="94f18-154">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="94f18-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="94f18-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94f18-155">RELATED LINKS</span></span>

