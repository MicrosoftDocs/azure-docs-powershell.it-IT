---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: 10a3ca97d5f4bba9bf47eff5b2e4bdbb29b8ff24
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358987"
---
# <span data-ttu-id="cf3d9-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="cf3d9-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="cf3d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3d9-103">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-103">Gets information about a server.</span></span>

## <span data-ttu-id="cf3d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf3d9-104">SYNTAX</span></span>

### <span data-ttu-id="cf3d9-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf3d9-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf3d9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cf3d9-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf3d9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf3d9-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf3d9-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="cf3d9-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cf3d9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf3d9-109">DESCRIPTION</span></span>
<span data-ttu-id="cf3d9-110">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-110">Gets information about a server.</span></span>

## <span data-ttu-id="cf3d9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf3d9-111">EXAMPLES</span></span>

### <span data-ttu-id="cf3d9-112">Esempio 1: ottenere il server MySql con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="cf3d9-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cf3d9-113">Questo cmdlet ottiene i server MySql con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="cf3d9-114">Esempio 2: ottenere il server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="cf3d9-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cf3d9-115">Questo cmdlet ottiene i server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="cf3d9-116">Esempio 3: elenca tutti i server MySql nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="cf3d9-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cf3d9-117">Questo cmdlet elenca tutti i server MySql nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="cf3d9-118">Esempio 4: ottenere il server MySql per identità</span><span class="sxs-lookup"><span data-stu-id="cf3d9-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cf3d9-119">Questo cmdlet elenca i server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="cf3d9-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf3d9-120">PARAMETERS</span></span>

### <span data-ttu-id="cf3d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3d9-121">-DefaultProfile</span></span>
<span data-ttu-id="cf3d9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf3d9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf3d9-123">-InputObject</span></span>
<span data-ttu-id="cf3d9-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf3d9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf3d9-125">-Name</span></span>
<span data-ttu-id="cf3d9-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-126">The name of the server.</span></span>

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

### <span data-ttu-id="cf3d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf3d9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-128">The name of the resource group.</span></span>
<span data-ttu-id="cf3d9-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cf3d9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf3d9-130">-SubscriptionId</span></span>
<span data-ttu-id="cf3d9-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cf3d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3d9-132">CommonParameters</span></span>
<span data-ttu-id="cf3d9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3d9-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf3d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3d9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf3d9-135">INPUTS</span></span>

### <span data-ttu-id="cf3d9-136">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cf3d9-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="cf3d9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf3d9-137">OUTPUTS</span></span>

### <span data-ttu-id="cf3d9-138">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="cf3d9-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="cf3d9-139">Note</span><span class="sxs-lookup"><span data-stu-id="cf3d9-139">NOTES</span></span>

<span data-ttu-id="cf3d9-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cf3d9-140">ALIASES</span></span>

<span data-ttu-id="cf3d9-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf3d9-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf3d9-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf3d9-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf3d9-144">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cf3d9-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf3d9-145">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cf3d9-146">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cf3d9-147">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cf3d9-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cf3d9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf3d9-149">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="cf3d9-150">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cf3d9-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cf3d9-152">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="cf3d9-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cf3d9-154">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cf3d9-155">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cf3d9-156">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="cf3d9-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cf3d9-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf3d9-157">RELATED LINKS</span></span>

