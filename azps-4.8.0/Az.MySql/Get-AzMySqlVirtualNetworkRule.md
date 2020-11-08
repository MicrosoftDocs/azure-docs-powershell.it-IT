---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 91d774931ac7ef4b8f1d41a70953d4a5b3a322cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191434"
---
# <span data-ttu-id="55a32-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="55a32-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="55a32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55a32-102">SYNOPSIS</span></span>
<span data-ttu-id="55a32-103">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="55a32-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="55a32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55a32-104">SYNTAX</span></span>

### <span data-ttu-id="55a32-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55a32-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="55a32-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="55a32-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="55a32-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="55a32-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="55a32-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55a32-108">DESCRIPTION</span></span>
<span data-ttu-id="55a32-109">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="55a32-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="55a32-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55a32-110">EXAMPLES</span></span>

### <span data-ttu-id="55a32-111">Esempio 1: elenca tutte le regole di rete virtuale nel server MySql specificato</span><span class="sxs-lookup"><span data-stu-id="55a32-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="55a32-112">Questo cmdlet elenca tutte le regole di rete virtuale nel server MySql specificato.</span><span class="sxs-lookup"><span data-stu-id="55a32-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="55a32-113">Esempio 2: ottenere la regola di rete virtuale per nome</span><span class="sxs-lookup"><span data-stu-id="55a32-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="55a32-114">Questo cmdlet ottiene la regola di rete virtuale per nome.</span><span class="sxs-lookup"><span data-stu-id="55a32-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="55a32-115">Esempio 3: ottenere la regola di rete virtuale per identità</span><span class="sxs-lookup"><span data-stu-id="55a32-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="55a32-116">Questo cmdlet ottiene la regola di rete virtuale per identità.</span><span class="sxs-lookup"><span data-stu-id="55a32-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="55a32-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55a32-117">PARAMETERS</span></span>

### <span data-ttu-id="55a32-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a32-118">-DefaultProfile</span></span>
<span data-ttu-id="55a32-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55a32-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a32-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55a32-120">-InputObject</span></span>
<span data-ttu-id="55a32-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="55a32-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="55a32-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="55a32-122">-Name</span></span>
<span data-ttu-id="55a32-123">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="55a32-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="55a32-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55a32-124">-PassThru</span></span>
<span data-ttu-id="55a32-125">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="55a32-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="55a32-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a32-126">-ResourceGroupName</span></span>
<span data-ttu-id="55a32-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55a32-127">The name of the resource group.</span></span>
<span data-ttu-id="55a32-128">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="55a32-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="55a32-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="55a32-129">-ServerName</span></span>
<span data-ttu-id="55a32-130">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="55a32-130">The name of the server.</span></span>

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

### <span data-ttu-id="55a32-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55a32-131">-SubscriptionId</span></span>
<span data-ttu-id="55a32-132">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="55a32-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="55a32-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a32-133">CommonParameters</span></span>
<span data-ttu-id="55a32-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a32-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a32-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55a32-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a32-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55a32-136">INPUTS</span></span>

### <span data-ttu-id="55a32-137">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="55a32-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="55a32-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55a32-138">OUTPUTS</span></span>

### <span data-ttu-id="55a32-139">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="55a32-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="55a32-140">Note</span><span class="sxs-lookup"><span data-stu-id="55a32-140">NOTES</span></span>

<span data-ttu-id="55a32-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="55a32-141">ALIASES</span></span>

<span data-ttu-id="55a32-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55a32-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55a32-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="55a32-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55a32-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="55a32-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55a32-145">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="55a32-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="55a32-146">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="55a32-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="55a32-147">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="55a32-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="55a32-148">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="55a32-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="55a32-149">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="55a32-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="55a32-150">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="55a32-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="55a32-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55a32-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="55a32-152">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="55a32-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="55a32-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="55a32-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="55a32-154">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="55a32-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="55a32-155">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="55a32-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="55a32-156">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="55a32-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="55a32-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55a32-157">RELATED LINKS</span></span>

