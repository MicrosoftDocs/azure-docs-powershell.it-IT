---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0f65a007a37df559802a134ec5d6d8fc6fb33d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179159"
---
# <span data-ttu-id="0afd9-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afd9-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="0afd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afd9-102">SYNOPSIS</span></span>
<span data-ttu-id="0afd9-103">Ottiene informazioni su una configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="0afd9-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0afd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0afd9-104">SYNTAX</span></span>

### <span data-ttu-id="0afd9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0afd9-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0afd9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0afd9-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0afd9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0afd9-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0afd9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0afd9-108">DESCRIPTION</span></span>
<span data-ttu-id="0afd9-109">Ottiene informazioni su una configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="0afd9-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="0afd9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0afd9-110">EXAMPLES</span></span>

### <span data-ttu-id="0afd9-111">Esempio 1: Ottenere la configurazione PostgreSql specificata in base al nome</span><span class="sxs-lookup"><span data-stu-id="0afd9-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="0afd9-112">Questo cmdlet viene specificato per nome per la configurazione PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="0afd9-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="0afd9-113">Esempio 2: Elencare tutte le configurazioni nel server PostgreSql specificato</span><span class="sxs-lookup"><span data-stu-id="0afd9-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="0afd9-114">Questo cmdlet elenca tutte le configurazioni nel server PostgreSql specificato.</span><span class="sxs-lookup"><span data-stu-id="0afd9-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="0afd9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0afd9-115">PARAMETERS</span></span>

### <span data-ttu-id="0afd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afd9-116">-DefaultProfile</span></span>
<span data-ttu-id="0afd9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0afd9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afd9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0afd9-118">-InputObject</span></span>
<span data-ttu-id="0afd9-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0afd9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0afd9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0afd9-120">-Name</span></span>
<span data-ttu-id="0afd9-121">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="0afd9-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afd9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afd9-122">-ResourceGroupName</span></span>
<span data-ttu-id="0afd9-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0afd9-123">The name of the resource group.</span></span>
<span data-ttu-id="0afd9-124">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0afd9-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0afd9-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0afd9-125">-ServerName</span></span>
<span data-ttu-id="0afd9-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="0afd9-126">The name of the server.</span></span>

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

### <span data-ttu-id="0afd9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0afd9-127">-SubscriptionId</span></span>
<span data-ttu-id="0afd9-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0afd9-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0afd9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afd9-129">CommonParameters</span></span>
<span data-ttu-id="0afd9-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afd9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afd9-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0afd9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afd9-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="0afd9-132">INPUTS</span></span>

### <span data-ttu-id="0afd9-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0afd9-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0afd9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0afd9-134">OUTPUTS</span></span>

### <span data-ttu-id="0afd9-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="0afd9-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="0afd9-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="0afd9-136">NOTES</span></span>

<span data-ttu-id="0afd9-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0afd9-137">ALIASES</span></span>

<span data-ttu-id="0afd9-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0afd9-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0afd9-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0afd9-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0afd9-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0afd9-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0afd9-141">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="0afd9-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0afd9-142">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="0afd9-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0afd9-143">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="0afd9-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0afd9-144">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="0afd9-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0afd9-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0afd9-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0afd9-146">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="0afd9-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0afd9-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0afd9-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0afd9-148">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="0afd9-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="0afd9-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0afd9-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0afd9-150">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="0afd9-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0afd9-151">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0afd9-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0afd9-152">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0afd9-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0afd9-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0afd9-153">RELATED LINKS</span></span>

