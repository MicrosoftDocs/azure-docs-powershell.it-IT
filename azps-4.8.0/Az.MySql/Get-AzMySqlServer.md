---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191432"
---
# <span data-ttu-id="d058d-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="d058d-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="d058d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d058d-102">SYNOPSIS</span></span>
<span data-ttu-id="d058d-103">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="d058d-103">Gets information about a server.</span></span>

## <span data-ttu-id="d058d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d058d-104">SYNTAX</span></span>

### <span data-ttu-id="d058d-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d058d-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d058d-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d058d-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d058d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d058d-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d058d-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="d058d-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d058d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d058d-109">DESCRIPTION</span></span>
<span data-ttu-id="d058d-110">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="d058d-110">Gets information about a server.</span></span>

## <span data-ttu-id="d058d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d058d-111">EXAMPLES</span></span>

### <span data-ttu-id="d058d-112">Esempio 1: ottenere il server MySql con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="d058d-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d058d-113">Questo cmdlet ottiene il server MySql con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="d058d-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="d058d-114">Esempio 2: ottenere il server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="d058d-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d058d-115">Questo cmdlet ottiene il server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="d058d-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="d058d-116">Esempio 3: elenca tutti i server MySql nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="d058d-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d058d-117">Questo cmdlet elenca tutti i server MySql nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d058d-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="d058d-118">Esempio 4: ottenere il server MySql per identità</span><span class="sxs-lookup"><span data-stu-id="d058d-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d058d-119">Questo cmdlet elenca il server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d058d-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="d058d-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d058d-120">PARAMETERS</span></span>

### <span data-ttu-id="d058d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d058d-121">-DefaultProfile</span></span>
<span data-ttu-id="d058d-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d058d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d058d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d058d-123">-InputObject</span></span>
<span data-ttu-id="d058d-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d058d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d058d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d058d-125">-Name</span></span>
<span data-ttu-id="d058d-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d058d-126">The name of the server.</span></span>

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

### <span data-ttu-id="d058d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d058d-127">-ResourceGroupName</span></span>
<span data-ttu-id="d058d-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d058d-128">The name of the resource group.</span></span>
<span data-ttu-id="d058d-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d058d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d058d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d058d-130">-SubscriptionId</span></span>
<span data-ttu-id="d058d-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d058d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d058d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d058d-132">CommonParameters</span></span>
<span data-ttu-id="d058d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d058d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d058d-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d058d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d058d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d058d-135">INPUTS</span></span>

### <span data-ttu-id="d058d-136">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d058d-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d058d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d058d-137">OUTPUTS</span></span>

### <span data-ttu-id="d058d-138">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="d058d-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="d058d-139">Note</span><span class="sxs-lookup"><span data-stu-id="d058d-139">NOTES</span></span>

<span data-ttu-id="d058d-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d058d-140">ALIASES</span></span>

<span data-ttu-id="d058d-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d058d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d058d-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d058d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d058d-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d058d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d058d-144">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d058d-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d058d-145">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d058d-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d058d-146">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="d058d-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d058d-147">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="d058d-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d058d-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d058d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d058d-149">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="d058d-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d058d-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d058d-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d058d-151">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d058d-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="d058d-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d058d-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d058d-153">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d058d-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d058d-154">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d058d-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d058d-155">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d058d-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d058d-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d058d-156">RELATED LINKS</span></span>

