---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476131"
---
# <span data-ttu-id="c1166-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c1166-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="c1166-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1166-102">SYNOPSIS</span></span>
<span data-ttu-id="c1166-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="c1166-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c1166-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1166-104">SYNTAX</span></span>

### <span data-ttu-id="c1166-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1166-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1166-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="c1166-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c1166-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c1166-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1166-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1166-108">DESCRIPTION</span></span>
<span data-ttu-id="c1166-109">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="c1166-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c1166-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1166-110">EXAMPLES</span></span>

### <span data-ttu-id="c1166-111">Esempio 1: creare una regola del firewall in un MariaDB</span><span class="sxs-lookup"><span data-stu-id="c1166-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="c1166-112">Questo comando crea una regola del firewall in un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c1166-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="c1166-113">Esempio 2: creare una nuova regola del firewall di MariaDB con-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="c1166-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="c1166-114">Questo cmdlet crea una regola del firewall MariaDB con-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="c1166-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="c1166-115">Esempio 3: creare una nuova regola del firewall di MariaDB per consentire tutti gli IPs</span><span class="sxs-lookup"><span data-stu-id="c1166-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="c1166-116">Questo cmdlet crea una nuova regola del firewall di MariaDB per consentire tutti gli IPs.</span><span class="sxs-lookup"><span data-stu-id="c1166-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="c1166-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1166-117">PARAMETERS</span></span>

### <span data-ttu-id="c1166-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="c1166-118">-AllowAll</span></span>
<span data-ttu-id="c1166-119">Presenta per consentire a tutti gli IP dell'intervallo, da 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="c1166-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1166-120">-AsJob</span></span>
<span data-ttu-id="c1166-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c1166-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c1166-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c1166-122">-ClientIPAddress</span></span>
<span data-ttu-id="c1166-123">Il client ha specificato un singolo IP della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c1166-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="c1166-124">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c1166-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1166-125">-DefaultProfile</span></span>
<span data-ttu-id="c1166-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1166-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1166-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="c1166-127">-EndIPAddress</span></span>
<span data-ttu-id="c1166-128">Indirizzo IP finale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c1166-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="c1166-129">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c1166-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1166-130">-Name</span></span>
<span data-ttu-id="c1166-131">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c1166-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="c1166-132">Se non viene specificato, il valore predefinito è non definito.</span><span class="sxs-lookup"><span data-stu-id="c1166-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="c1166-133">Se AllowAll è presente, il nome predefinito è AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="c1166-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-134">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c1166-134">-NoWait</span></span>
<span data-ttu-id="c1166-135">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c1166-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c1166-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1166-136">-ResourceGroupName</span></span>
<span data-ttu-id="c1166-137">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1166-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c1166-138">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c1166-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-139">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c1166-139">-ServerName</span></span>
<span data-ttu-id="c1166-140">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="c1166-140">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="c1166-141">-StartIPAddress</span></span>
<span data-ttu-id="c1166-142">Indirizzo IP iniziale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c1166-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="c1166-143">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c1166-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1166-144">-SubscriptionId</span></span>
<span data-ttu-id="c1166-145">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c1166-145">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c1166-146">-Confirm</span></span>
<span data-ttu-id="c1166-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1166-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1166-148">-WhatIf</span></span>
<span data-ttu-id="c1166-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1166-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1166-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c1166-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1166-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1166-151">CommonParameters</span></span>
<span data-ttu-id="c1166-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1166-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1166-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1166-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1166-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1166-154">INPUTS</span></span>

## <span data-ttu-id="c1166-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1166-155">OUTPUTS</span></span>

### <span data-ttu-id="c1166-156">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c1166-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="c1166-157">Note</span><span class="sxs-lookup"><span data-stu-id="c1166-157">NOTES</span></span>

<span data-ttu-id="c1166-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c1166-158">ALIASES</span></span>

## <span data-ttu-id="c1166-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1166-159">RELATED LINKS</span></span>

