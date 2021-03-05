---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012013"
---
# <span data-ttu-id="bf06b-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="bf06b-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="bf06b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf06b-102">SYNOPSIS</span></span>
<span data-ttu-id="bf06b-103">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-103">Gets information about a server.</span></span>

## <span data-ttu-id="bf06b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf06b-104">SYNTAX</span></span>

### <span data-ttu-id="bf06b-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf06b-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf06b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bf06b-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf06b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bf06b-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bf06b-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="bf06b-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bf06b-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bf06b-109">DESCRIPTION</span></span>
<span data-ttu-id="bf06b-110">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-110">Gets information about a server.</span></span>

## <span data-ttu-id="bf06b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf06b-111">EXAMPLES</span></span>

### <span data-ttu-id="bf06b-112">Esempio 1: Ottenere il server MySql con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="bf06b-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bf06b-113">Questo cmdlet ottiene i server MySql con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="bf06b-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="bf06b-114">Esempio 2: Ottenere il server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="bf06b-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bf06b-115">Questo cmdlet recupera i server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="bf06b-116">Esempio 3: Elenca tutti i server MySql nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="bf06b-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bf06b-117">Questo cmdlet elenca tutti i server MySql nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="bf06b-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="bf06b-118">Esempio 4: Ottenere il server MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="bf06b-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="bf06b-119">Questo elenco di cmdlet recupera i server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="bf06b-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="bf06b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf06b-120">PARAMETERS</span></span>

### <span data-ttu-id="bf06b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf06b-121">-DefaultProfile</span></span>
<span data-ttu-id="bf06b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf06b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf06b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf06b-123">-InputObject</span></span>
<span data-ttu-id="bf06b-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bf06b-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bf06b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bf06b-125">-Name</span></span>
<span data-ttu-id="bf06b-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-126">The name of the server.</span></span>

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

### <span data-ttu-id="bf06b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf06b-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf06b-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bf06b-128">The name of the resource group.</span></span>
<span data-ttu-id="bf06b-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bf06b-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bf06b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bf06b-130">-SubscriptionId</span></span>
<span data-ttu-id="bf06b-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bf06b-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bf06b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf06b-132">CommonParameters</span></span>
<span data-ttu-id="bf06b-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf06b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf06b-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bf06b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf06b-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="bf06b-135">INPUTS</span></span>

### <span data-ttu-id="bf06b-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bf06b-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bf06b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf06b-137">OUTPUTS</span></span>

### <span data-ttu-id="bf06b-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="bf06b-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="bf06b-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="bf06b-139">NOTES</span></span>

<span data-ttu-id="bf06b-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bf06b-140">ALIASES</span></span>

<span data-ttu-id="bf06b-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="bf06b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bf06b-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bf06b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bf06b-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bf06b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bf06b-144">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bf06b-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bf06b-145">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bf06b-146">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="bf06b-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bf06b-147">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bf06b-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="bf06b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bf06b-149">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bf06b-150">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="bf06b-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bf06b-151">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bf06b-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bf06b-152">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bf06b-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="bf06b-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bf06b-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bf06b-154">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="bf06b-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bf06b-155">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bf06b-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bf06b-156">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bf06b-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bf06b-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf06b-157">RELATED LINKS</span></span>

