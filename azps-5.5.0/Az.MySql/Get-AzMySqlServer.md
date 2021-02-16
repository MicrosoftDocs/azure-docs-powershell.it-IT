---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 4308f2ec3da458f03e53d17a873d92ea5d775ff4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192126"
---
# <span data-ttu-id="d9d27-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="d9d27-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="d9d27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d27-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d27-103">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-103">Gets information about a server.</span></span>

## <span data-ttu-id="d9d27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9d27-104">SYNTAX</span></span>

### <span data-ttu-id="d9d27-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9d27-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9d27-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d9d27-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9d27-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9d27-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d9d27-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="d9d27-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9d27-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9d27-109">DESCRIPTION</span></span>
<span data-ttu-id="d9d27-110">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-110">Gets information about a server.</span></span>

## <span data-ttu-id="d9d27-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9d27-111">EXAMPLES</span></span>

### <span data-ttu-id="d9d27-112">Esempio 1: Ottenere il server MySql con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="d9d27-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d9d27-113">Questo cmdlet ottiene il server MySql con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="d9d27-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="d9d27-114">Esempio 2: Ottenere il server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="d9d27-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d9d27-115">Questo cmdlet ottiene il server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="d9d27-116">Esempio 3: Elenca tutti i server MySql nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="d9d27-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d9d27-117">Questo cmdlet elenca tutti i server MySql nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d9d27-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="d9d27-118">Esempio 4: Ottenere il server MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="d9d27-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d9d27-119">Questo elenco di cmdlet ottiene il server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d9d27-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="d9d27-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9d27-120">PARAMETERS</span></span>

### <span data-ttu-id="d9d27-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d27-121">-DefaultProfile</span></span>
<span data-ttu-id="d9d27-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d27-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9d27-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9d27-123">-InputObject</span></span>
<span data-ttu-id="d9d27-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d9d27-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d9d27-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d9d27-125">-Name</span></span>
<span data-ttu-id="d9d27-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-126">The name of the server.</span></span>

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

### <span data-ttu-id="d9d27-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d27-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9d27-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9d27-128">The name of the resource group.</span></span>
<span data-ttu-id="d9d27-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d9d27-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d9d27-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9d27-130">-SubscriptionId</span></span>
<span data-ttu-id="d9d27-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d9d27-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d9d27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d27-132">CommonParameters</span></span>
<span data-ttu-id="d9d27-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d27-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9d27-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d27-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9d27-135">INPUTS</span></span>

### <span data-ttu-id="d9d27-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d9d27-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d9d27-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9d27-137">OUTPUTS</span></span>

### <span data-ttu-id="d9d27-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="d9d27-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="d9d27-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9d27-139">NOTES</span></span>

<span data-ttu-id="d9d27-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d9d27-140">ALIASES</span></span>

<span data-ttu-id="d9d27-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d9d27-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9d27-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d9d27-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9d27-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9d27-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9d27-144">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="d9d27-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9d27-145">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d9d27-146">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="d9d27-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d9d27-147">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d9d27-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d9d27-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9d27-149">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d9d27-150">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="d9d27-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d9d27-151">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9d27-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d9d27-152">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d9d27-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="d9d27-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d9d27-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d9d27-154">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="d9d27-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d9d27-155">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d9d27-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d9d27-156">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9d27-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d9d27-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9d27-157">RELATED LINKS</span></span>

