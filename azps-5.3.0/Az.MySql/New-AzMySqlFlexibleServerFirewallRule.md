---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: f7e0f511c42dd6eda730380a02e0d46239bf045e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475192"
---
# <span data-ttu-id="9932b-101">New-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9932b-101">New-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="9932b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9932b-102">SYNOPSIS</span></span>
<span data-ttu-id="9932b-103">Crea una nuova regola del firewall per MySQL flexible server</span><span class="sxs-lookup"><span data-stu-id="9932b-103">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="9932b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9932b-104">SYNTAX</span></span>

### <span data-ttu-id="9932b-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9932b-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9932b-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="9932b-106">AllowAll</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9932b-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9932b-107">ClientIPAddress</span></span>
```
New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9932b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9932b-108">DESCRIPTION</span></span>
<span data-ttu-id="9932b-109">Crea una nuova regola del firewall per MySQL flexible server</span><span class="sxs-lookup"><span data-stu-id="9932b-109">Creates a new firewall rule for MySQL flexible server</span></span>

## <span data-ttu-id="9932b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9932b-110">EXAMPLES</span></span>

### <span data-ttu-id="9932b-111">Esempio 1: creare una nuova regola del firewall del server MySql</span><span class="sxs-lookup"><span data-stu-id="9932b-111">Example 1: Create a new MySql server Firewall Rule</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name              StartIPAddress EndIPAddress
----------------- -------------- ------------
firewallrule-test 0.0.0.0        0.0.0.1
```

<span data-ttu-id="9932b-112">Questo cmdlet crea una regola del firewall del server MySql.</span><span class="sxs-lookup"><span data-stu-id="9932b-112">This cmdlets create a MySql server Firewall Rule.</span></span>

### <span data-ttu-id="9932b-113">Esempio 2: creare una nuova regola del firewall MySql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="9932b-113">Example 2: Create a new MySql Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="9932b-114">Questo cmdlet crea una regola firewall MySql usando-ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="9932b-114">This cmdlets create a MySql Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="9932b-115">Esempio 3: creare una nuova regola del firewall MySql per consentire tutti gli IPs</span><span class="sxs-lookup"><span data-stu-id="9932b-115">Example 3: Create a new MySql Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="9932b-116">Questo cmdlet crea una nuova regola del firewall MySql per consentire tutti gli IPs.</span><span class="sxs-lookup"><span data-stu-id="9932b-116">This cmdlets create a new MySql Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="9932b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9932b-117">PARAMETERS</span></span>

### <span data-ttu-id="9932b-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="9932b-118">-AllowAll</span></span>
<span data-ttu-id="9932b-119">Presenta per consentire a tutti gli IP dell'intervallo, da 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="9932b-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

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

### <span data-ttu-id="9932b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9932b-120">-AsJob</span></span>
<span data-ttu-id="9932b-121">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="9932b-121">Run the command as a job</span></span>

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

### <span data-ttu-id="9932b-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9932b-122">-ClientIPAddress</span></span>
<span data-ttu-id="9932b-123">Il client ha specificato un singolo IP della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="9932b-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="9932b-124">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="9932b-124">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9932b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9932b-125">-DefaultProfile</span></span>
<span data-ttu-id="9932b-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9932b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9932b-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="9932b-127">-EndIPAddress</span></span>
<span data-ttu-id="9932b-128">Indirizzo IP finale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="9932b-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="9932b-129">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="9932b-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9932b-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="9932b-130">-Name</span></span>
<span data-ttu-id="9932b-131">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="9932b-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="9932b-132">Se non viene specificato, il valore predefinito è non definito.</span><span class="sxs-lookup"><span data-stu-id="9932b-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="9932b-133">Se AllowAll è presente, il nome predefinito è AllowAll_yyyy-MM-dd_HH-mm-SS.</span><span class="sxs-lookup"><span data-stu-id="9932b-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

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

### <span data-ttu-id="9932b-134">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="9932b-134">-NoWait</span></span>
<span data-ttu-id="9932b-135">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="9932b-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9932b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9932b-136">-ResourceGroupName</span></span>
<span data-ttu-id="9932b-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9932b-137">The name of the resource group.</span></span>
<span data-ttu-id="9932b-138">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9932b-138">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9932b-139">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9932b-139">-ServerName</span></span>
<span data-ttu-id="9932b-140">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="9932b-140">The name of the server.</span></span>

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

### <span data-ttu-id="9932b-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="9932b-141">-StartIPAddress</span></span>
<span data-ttu-id="9932b-142">Indirizzo IP iniziale della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="9932b-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="9932b-143">Deve essere formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="9932b-143">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="9932b-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9932b-144">-SubscriptionId</span></span>
<span data-ttu-id="9932b-145">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9932b-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9932b-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9932b-146">-Confirm</span></span>
<span data-ttu-id="9932b-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9932b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9932b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9932b-148">-WhatIf</span></span>
<span data-ttu-id="9932b-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9932b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9932b-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9932b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9932b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9932b-151">CommonParameters</span></span>
<span data-ttu-id="9932b-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9932b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9932b-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9932b-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9932b-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9932b-154">INPUTS</span></span>

## <span data-ttu-id="9932b-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9932b-155">OUTPUTS</span></span>

### <span data-ttu-id="9932b-156">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9932b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="9932b-157">Note</span><span class="sxs-lookup"><span data-stu-id="9932b-157">NOTES</span></span>

<span data-ttu-id="9932b-158">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9932b-158">ALIASES</span></span>

## <span data-ttu-id="9932b-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9932b-159">RELATED LINKS</span></span>

