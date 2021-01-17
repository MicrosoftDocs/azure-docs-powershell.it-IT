---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: bafd0e20530198da87c1fa3ece36905e73307a42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378430"
---
# <span data-ttu-id="afccc-101">New-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="afccc-101">New-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="afccc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afccc-102">SYNOPSIS</span></span>
<span data-ttu-id="afccc-103">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="afccc-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="afccc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afccc-104">SYNTAX</span></span>

### <span data-ttu-id="afccc-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afccc-105">CreateExpanded (Default)</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="afccc-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="afccc-106">AllowAll</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="afccc-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="afccc-107">ClientIPAddress</span></span>
```
New-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="afccc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afccc-108">DESCRIPTION</span></span>
<span data-ttu-id="afccc-109">Crea una nuova regola del firewall o aggiorna una regola del firewall esistente.</span><span class="sxs-lookup"><span data-stu-id="afccc-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="afccc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afccc-110">EXAMPLES</span></span>

### <span data-ttu-id="afccc-111">Esempio 1: creare una nuova regola del firewall del server PostgreSql</span><span class="sxs-lookup"><span data-stu-id="afccc-111">Example 1: Create a new PostgreSql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="afccc-112">Questo cmdlet crea una regola del firewall del server PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="afccc-112">This cmdlets create a PostgreSql server Firewall Rule.</span></span>

### <span data-ttu-id="afccc-113">Esempio 2: creare una nuova regola del firewall PostgreSql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="afccc-113">Example 2: Create a new PostgreSql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="afccc-114">Questo cmdlet crea una regola del firewall PostgreSql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="afccc-114">This cmdlets create a PostgreSql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="afccc-115">Esempio 3: creare una nuova regola del firewall PostgreSql per consentire tutti gli IPs</span><span class="sxs-lookup"><span data-stu-id="afccc-115">Example 3: Create a new PostgreSql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="afccc-116">Questo cmdlet crea una nuova regola del firewall PostgreSql per consentire tutti gli IPs.</span><span class="sxs-lookup"><span data-stu-id="afccc-116">This cmdlets create a new PostgreSql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="afccc-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afccc-117">PARAMETERS</span></span>

### <span data-ttu-id="afccc-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="afccc-118">-AllowAll</span></span>
<span data-ttu-id="afccc-119">Presenta per consentire a tutti gli IP dell'intervallo, da 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="afccc-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="afccc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afccc-120">-AsJob</span></span>
<span data-ttu-id="afccc-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="afccc-121">Run the command as a job</span></span>

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

### <span data-ttu-id="afccc-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="afccc-122">-ClientIPAddress</span></span>
<span data-ttu-id="afccc-123">Il client ha specificato un singolo IP della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="afccc-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="afccc-124">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="afccc-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="afccc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afccc-125">-DefaultProfile</span></span>
<span data-ttu-id="afccc-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afccc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afccc-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="afccc-127">-EndIPAddress</span></span>
<span data-ttu-id="afccc-128">Indirizzo IP finale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="afccc-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="afccc-129">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="afccc-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="afccc-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="afccc-130">-Name</span></span>
<span data-ttu-id="afccc-131">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="afccc-131">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="afccc-132">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="afccc-132">-NoWait</span></span>
<span data-ttu-id="afccc-133">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="afccc-133">Run the command asynchronously</span></span>

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

### <span data-ttu-id="afccc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afccc-134">-ResourceGroupName</span></span>
<span data-ttu-id="afccc-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="afccc-135">The name of the resource group.</span></span>
<span data-ttu-id="afccc-136">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="afccc-136">The name is case insensitive.</span></span>

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

### <span data-ttu-id="afccc-137">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="afccc-137">-ServerName</span></span>
<span data-ttu-id="afccc-138">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="afccc-138">The name of the server.</span></span>

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

### <span data-ttu-id="afccc-139">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="afccc-139">-StartIPAddress</span></span>
<span data-ttu-id="afccc-140">Indirizzo IP iniziale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="afccc-140">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="afccc-141">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="afccc-141">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="afccc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afccc-142">-SubscriptionId</span></span>
<span data-ttu-id="afccc-143">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="afccc-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="afccc-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="afccc-144">-Confirm</span></span>
<span data-ttu-id="afccc-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afccc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afccc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afccc-146">-WhatIf</span></span>
<span data-ttu-id="afccc-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afccc-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afccc-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="afccc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afccc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afccc-149">CommonParameters</span></span>
<span data-ttu-id="afccc-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afccc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afccc-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afccc-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afccc-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afccc-152">INPUTS</span></span>

## <span data-ttu-id="afccc-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afccc-153">OUTPUTS</span></span>

### <span data-ttu-id="afccc-154">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="afccc-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="afccc-155">Note</span><span class="sxs-lookup"><span data-stu-id="afccc-155">NOTES</span></span>

<span data-ttu-id="afccc-156">ALIAS</span><span class="sxs-lookup"><span data-stu-id="afccc-156">ALIASES</span></span>

## <span data-ttu-id="afccc-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afccc-157">RELATED LINKS</span></span>

