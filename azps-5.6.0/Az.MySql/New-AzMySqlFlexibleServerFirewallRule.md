---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: e06447fc72dc8dc3bc09768360039a561b1b862a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995440"
---
# <span data-ttu-id="a07e2-101">New-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a07e2-101">New-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="a07e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a07e2-103">Crea una nuova regola del firewall per il server flessibile MySQL</span><span class="sxs-lookup"><span data-stu-id="a07e2-103">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="a07e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a07e2-104">SYNTAX</span></span>

### <span data-ttu-id="a07e2-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a07e2-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a07e2-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="a07e2-106">AllowAll</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a07e2-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a07e2-107">ClientIPAddress</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a07e2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a07e2-108">DESCRIPTION</span></span>
<span data-ttu-id="a07e2-109">Crea una nuova regola del firewall per il server flessibile MySQL</span><span class="sxs-lookup"><span data-stu-id="a07e2-109">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="a07e2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a07e2-110">EXAMPLES</span></span>

### <span data-ttu-id="a07e2-111">Esempio 1: Creare una nuova regola firewall del server MySql</span><span class="sxs-lookup"><span data-stu-id="a07e2-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="a07e2-112">Questi cmdlet creano una regola firewall del server MySql.</span><span class="sxs-lookup"><span data-stu-id="a07e2-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="a07e2-113">Esempio 2: Creare una nuova regola del firewall MySql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="a07e2-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="a07e2-114">Questo cmdlet crea una regola del firewall MySql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="a07e2-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="a07e2-115">Esempio 3: Creare una nuova regola del firewall MySql per consentire tutti gli IP</span><span class="sxs-lookup"><span data-stu-id="a07e2-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="a07e2-116">Questo cmdlet crea una nuova regola del firewall MySql per consentire tutti gli IP.</span><span class="sxs-lookup"><span data-stu-id="a07e2-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="a07e2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a07e2-117">PARAMETERS</span></span>

### <span data-ttu-id="a07e2-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="a07e2-118">-AllowAll</span></span>
<span data-ttu-id="a07e2-119">Presenta per consentire tutti gli IP di intervallo, da 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="a07e2-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="a07e2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a07e2-120">-AsJob</span></span>
<span data-ttu-id="a07e2-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a07e2-121">Run the command as a job</span></span>

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

### <span data-ttu-id="a07e2-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="a07e2-122">-ClientIPAddress</span></span>
<span data-ttu-id="a07e2-123">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="a07e2-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="a07e2-124">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="a07e2-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a07e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07e2-125">-DefaultProfile</span></span>
<span data-ttu-id="a07e2-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a07e2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07e2-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="a07e2-127">-EndIPAddress</span></span>
<span data-ttu-id="a07e2-128">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="a07e2-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="a07e2-129">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="a07e2-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a07e2-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a07e2-130">-Name</span></span>
<span data-ttu-id="a07e2-131">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="a07e2-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="a07e2-132">Se non viene specificato, l'impostazione predefinita non è definita.</span><span class="sxs-lookup"><span data-stu-id="a07e2-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="a07e2-133">Se AllowAll è presente, il nome predefinito è AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="a07e2-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="a07e2-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a07e2-134">-NoWait</span></span>
<span data-ttu-id="a07e2-135">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a07e2-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a07e2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07e2-136">-ResourceGroupName</span></span>
<span data-ttu-id="a07e2-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a07e2-137">The name of the resource group.</span></span>
<span data-ttu-id="a07e2-138">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a07e2-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a07e2-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a07e2-139">-ServerName</span></span>
<span data-ttu-id="a07e2-140">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="a07e2-140">The name of the server.</span></span>

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

### <span data-ttu-id="a07e2-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="a07e2-141">-StartIPAddress</span></span>
<span data-ttu-id="a07e2-142">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="a07e2-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="a07e2-143">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="a07e2-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="a07e2-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a07e2-144">-SubscriptionId</span></span>
<span data-ttu-id="a07e2-145">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a07e2-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a07e2-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a07e2-146">-Confirm</span></span>
<span data-ttu-id="a07e2-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a07e2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a07e2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07e2-148">-WhatIf</span></span>
<span data-ttu-id="a07e2-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a07e2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07e2-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a07e2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a07e2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07e2-151">CommonParameters</span></span>
<span data-ttu-id="a07e2-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07e2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07e2-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a07e2-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07e2-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="a07e2-154">INPUTS</span></span>

## <span data-ttu-id="a07e2-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a07e2-155">OUTPUTS</span></span>

### <span data-ttu-id="a07e2-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a07e2-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="a07e2-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="a07e2-157">NOTES</span></span>

<span data-ttu-id="a07e2-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a07e2-158">ALIASES</span></span>

## <span data-ttu-id="a07e2-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a07e2-159">RELATED LINKS</span></span>

