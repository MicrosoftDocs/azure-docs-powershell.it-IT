---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 8756626488dcc1f5f2a41a06d30581a67db74bb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184902"
---
# <span data-ttu-id="e0c2c-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e0c2c-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="e0c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c2c-103">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="e0c2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0c2c-104">SYNTAX</span></span>

### <span data-ttu-id="e0c2c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0c2c-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e0c2c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e0c2c-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e0c2c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e0c2c-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e0c2c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0c2c-108">DESCRIPTION</span></span>
<span data-ttu-id="e0c2c-109">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="e0c2c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0c2c-110">EXAMPLES</span></span>

### <span data-ttu-id="e0c2c-111">Esempio 1: Elenca tutte le regole di rete virtuale nel server MySql specificato</span><span class="sxs-lookup"><span data-stu-id="e0c2c-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="e0c2c-112">Questo cmdlet elenca tutte le regole di rete virtuale nel server MySql specificato.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="e0c2c-113">Esempio 2: Ottenere la regola della rete virtuale in base al nome</span><span class="sxs-lookup"><span data-stu-id="e0c2c-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="e0c2c-114">Questo cmdlet ottiene la regola della rete virtuale in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="e0c2c-115">Esempio 3: Ottenere la regola della rete virtuale in base all'identità</span><span class="sxs-lookup"><span data-stu-id="e0c2c-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="e0c2c-116">Questo cmdlet ottiene la regola della rete virtuale in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="e0c2c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0c2c-117">PARAMETERS</span></span>

### <span data-ttu-id="e0c2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c2c-118">-DefaultProfile</span></span>
<span data-ttu-id="e0c2c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c2c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0c2c-120">-InputObject</span></span>
<span data-ttu-id="e0c2c-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c2c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e0c2c-122">-Name</span></span>
<span data-ttu-id="e0c2c-123">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e0c2c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0c2c-124">-PassThru</span></span>
<span data-ttu-id="e0c2c-125">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="e0c2c-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e0c2c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0c2c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0c2c-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-127">The name of the resource group.</span></span>
<span data-ttu-id="e0c2c-128">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e0c2c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e0c2c-129">-ServerName</span></span>
<span data-ttu-id="e0c2c-130">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-130">The name of the server.</span></span>

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

### <span data-ttu-id="e0c2c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0c2c-131">-SubscriptionId</span></span>
<span data-ttu-id="e0c2c-132">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e0c2c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c2c-133">CommonParameters</span></span>
<span data-ttu-id="e0c2c-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c2c-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c2c-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0c2c-136">INPUTS</span></span>

### <span data-ttu-id="e0c2c-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e0c2c-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e0c2c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0c2c-138">OUTPUTS</span></span>

### <span data-ttu-id="e0c2c-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e0c2c-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="e0c2c-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0c2c-140">NOTES</span></span>

<span data-ttu-id="e0c2c-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e0c2c-141">ALIASES</span></span>

<span data-ttu-id="e0c2c-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e0c2c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0c2c-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0c2c-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0c2c-145">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="e0c2c-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0c2c-146">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e0c2c-147">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e0c2c-148">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e0c2c-149">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e0c2c-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0c2c-150">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e0c2c-151">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e0c2c-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e0c2c-153">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="e0c2c-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e0c2c-155">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e0c2c-156">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e0c2c-157">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0c2c-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e0c2c-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0c2c-158">RELATED LINKS</span></span>

