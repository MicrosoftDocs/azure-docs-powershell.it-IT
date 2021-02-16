---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179135"
---
# <span data-ttu-id="c99de-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c99de-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="c99de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99de-102">SYNOPSIS</span></span>
<span data-ttu-id="c99de-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="c99de-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c99de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c99de-104">SYNTAX</span></span>

### <span data-ttu-id="c99de-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c99de-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c99de-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="c99de-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c99de-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c99de-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c99de-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c99de-108">DESCRIPTION</span></span>
<span data-ttu-id="c99de-109">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="c99de-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="c99de-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c99de-110">EXAMPLES</span></span>

### <span data-ttu-id="c99de-111">Esempio 1: Creare una nuova regola firewall del server PostgreSql</span><span class="sxs-lookup"><span data-stu-id="c99de-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="c99de-112">Questi cmdlet creano una regola firewall del server PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="c99de-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="c99de-113">Esempio 2: Creare una nuova regola Del firewall PostgreSql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="c99de-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="c99de-114">Questo cmdlet crea una regola del firewall PostgreSql usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="c99de-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="c99de-115">Esempio 3: Creare una nuova regola del firewall PostgreSql per consentire tutti gli IP</span><span class="sxs-lookup"><span data-stu-id="c99de-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="c99de-116">Questo cmdlet crea una nuova regola del firewall PostgreSql per consentire tutti gli IP.</span><span class="sxs-lookup"><span data-stu-id="c99de-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="c99de-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c99de-117">PARAMETERS</span></span>

### <span data-ttu-id="c99de-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="c99de-118">-AllowAll</span></span>
<span data-ttu-id="c99de-119">Presenta per consentire tutti gli IP di intervallo, da 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="c99de-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="c99de-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c99de-120">-AsJob</span></span>
<span data-ttu-id="c99de-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c99de-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c99de-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="c99de-122">-ClientIPAddress</span></span>
<span data-ttu-id="c99de-123">Client ha specificato un singolo INDIRIZZO IP della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c99de-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="c99de-124">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c99de-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c99de-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99de-125">-DefaultProfile</span></span>
<span data-ttu-id="c99de-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c99de-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c99de-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="c99de-127">-EndIPAddress</span></span>
<span data-ttu-id="c99de-128">Indirizzo IP finale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c99de-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="c99de-129">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c99de-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c99de-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c99de-130">-Name</span></span>
<span data-ttu-id="c99de-131">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c99de-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="c99de-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c99de-132">-NoWait</span></span>
<span data-ttu-id="c99de-133">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c99de-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c99de-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99de-134">-ResourceGroupName</span></span>
<span data-ttu-id="c99de-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c99de-135">The name of the resource group.</span></span>
<span data-ttu-id="c99de-136">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c99de-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c99de-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c99de-137">-ServerName</span></span>
<span data-ttu-id="c99de-138">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="c99de-138">The name of the server.</span></span>

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

### <span data-ttu-id="c99de-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="c99de-139">-StartIPAddress</span></span>
<span data-ttu-id="c99de-140">Indirizzo IP iniziale della regola firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c99de-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="c99de-141">Deve essere in formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="c99de-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="c99de-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c99de-142">-SubscriptionId</span></span>
<span data-ttu-id="c99de-143">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c99de-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c99de-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c99de-144">-Confirm</span></span>
<span data-ttu-id="c99de-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c99de-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c99de-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c99de-146">-WhatIf</span></span>
<span data-ttu-id="c99de-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c99de-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c99de-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c99de-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c99de-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99de-149">CommonParameters</span></span>
<span data-ttu-id="c99de-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99de-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99de-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c99de-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99de-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="c99de-152">INPUTS</span></span>

## <span data-ttu-id="c99de-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c99de-153">OUTPUTS</span></span>

### <span data-ttu-id="c99de-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c99de-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="c99de-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="c99de-155">NOTES</span></span>

<span data-ttu-id="c99de-156">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c99de-156">ALIASES</span></span>

## <span data-ttu-id="c99de-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c99de-157">RELATED LINKS</span></span>

