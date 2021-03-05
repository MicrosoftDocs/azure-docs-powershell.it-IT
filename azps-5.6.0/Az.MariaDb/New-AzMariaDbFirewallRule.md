---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: c511e605af327f5ac1b913f133cf725baeee894c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970622"
---
# <span data-ttu-id="cc9ce-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc9ce-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="cc9ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9ce-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="cc9ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc9ce-104">SYNTAX</span></span>

### <span data-ttu-id="cc9ce-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc9ce-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc9ce-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="cc9ce-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cc9ce-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="cc9ce-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc9ce-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cc9ce-108">DESCRIPTION</span></span>
<span data-ttu-id="cc9ce-109">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="cc9ce-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc9ce-110">EXAMPLES</span></span>

### <span data-ttu-id="cc9ce-111">Esempio 1: Creare una regola del firewall in un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="cc9ce-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="cc9ce-112">Questo comando crea una regola del firewall in un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="cc9ce-113">Esempio 2: Creare una nuova regola del firewall MariaDB usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="cc9ce-114">Questo cmdlet crea una regola del firewall MariaDB usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="cc9ce-115">Esempio 3: Creare una nuova regola firewall MariaDB per consentire tutti gli IP</span><span class="sxs-lookup"><span data-stu-id="cc9ce-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="cc9ce-116">Questo cmdlet crea una nuova regola del firewall MariaDB per consentire tutti gli IP.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="cc9ce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc9ce-117">PARAMETERS</span></span>

### <span data-ttu-id="cc9ce-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="cc9ce-118">-AllowAll</span></span>
<span data-ttu-id="cc9ce-119">Presenta per consentire tutti gli IP di intervallo, da 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="cc9ce-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc9ce-120">-AsJob</span></span>
<span data-ttu-id="cc9ce-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="cc9ce-121">Run the command as a job</span></span>

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

### <span data-ttu-id="cc9ce-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="cc9ce-122">-ClientIPAddress</span></span>
<span data-ttu-id="cc9ce-123">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="cc9ce-124">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="cc9ce-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9ce-125">-DefaultProfile</span></span>
<span data-ttu-id="cc9ce-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc9ce-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="cc9ce-127">-EndIPAddress</span></span>
<span data-ttu-id="cc9ce-128">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="cc9ce-129">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="cc9ce-130">-Name</span><span class="sxs-lookup"><span data-stu-id="cc9ce-130">-Name</span></span>
<span data-ttu-id="cc9ce-131">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="cc9ce-132">Se non viene specificato, l'impostazione predefinita non è definita.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="cc9ce-133">Se AllowAll è presente, il nome predefinito è AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="cc9ce-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc9ce-134">-NoWait</span></span>
<span data-ttu-id="cc9ce-135">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cc9ce-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc9ce-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9ce-136">-ResourceGroupName</span></span>
<span data-ttu-id="cc9ce-137">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cc9ce-138">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cc9ce-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc9ce-139">-ServerName</span></span>
<span data-ttu-id="cc9ce-140">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-140">The name of the server.</span></span>

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

### <span data-ttu-id="cc9ce-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="cc9ce-141">-StartIPAddress</span></span>
<span data-ttu-id="cc9ce-142">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="cc9ce-143">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="cc9ce-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc9ce-144">-SubscriptionId</span></span>
<span data-ttu-id="cc9ce-145">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-145">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="cc9ce-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc9ce-146">-Confirm</span></span>
<span data-ttu-id="cc9ce-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc9ce-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9ce-148">-WhatIf</span></span>
<span data-ttu-id="cc9ce-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc9ce-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc9ce-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9ce-151">CommonParameters</span></span>
<span data-ttu-id="cc9ce-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9ce-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc9ce-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9ce-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="cc9ce-154">INPUTS</span></span>

## <span data-ttu-id="cc9ce-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc9ce-155">OUTPUTS</span></span>

### <span data-ttu-id="cc9ce-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cc9ce-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="cc9ce-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="cc9ce-157">NOTES</span></span>

<span data-ttu-id="cc9ce-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cc9ce-158">ALIASES</span></span>

## <span data-ttu-id="cc9ce-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc9ce-159">RELATED LINKS</span></span>

