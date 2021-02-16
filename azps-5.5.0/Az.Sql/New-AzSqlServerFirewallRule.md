---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178367"
---
# <span data-ttu-id="7a344-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a344-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="7a344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a344-102">SYNOPSIS</span></span>
<span data-ttu-id="7a344-103">Crea una regola del firewall per un server SQL database.</span><span class="sxs-lookup"><span data-stu-id="7a344-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="7a344-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a344-104">SYNTAX</span></span>

### <span data-ttu-id="7a344-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7a344-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a344-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="7a344-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a344-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7a344-107">DESCRIPTION</span></span>
<span data-ttu-id="7a344-108">Il cmdlet **New-AzSqlServerFirewallRule** crea una regola del firewall per il server di SQL database di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="7a344-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="7a344-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a344-109">EXAMPLES</span></span>

### <span data-ttu-id="7a344-110">Esempio 1: Creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="7a344-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="7a344-111">Questo comando crea una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="7a344-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="7a344-112">La regola include gli indirizzi IP di inizio e di fine specificati.</span><span class="sxs-lookup"><span data-stu-id="7a344-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="7a344-113">Esempio 2: Creare una regola del firewall che consente a tutti gli indirizzi IP di Azure di accedere al server</span><span class="sxs-lookup"><span data-stu-id="7a344-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="7a344-114">Questo comando crea una regola del firewall nel server denominato Server01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="7a344-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="7a344-115">Poiché viene *usato il parametro AllowAllAzureIPs,* la regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="7a344-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="7a344-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a344-116">PARAMETERS</span></span>

### <span data-ttu-id="7a344-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="7a344-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="7a344-118">Indica che questa regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="7a344-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="7a344-119">Non è possibile usare questo parametro se si intende usare i parametri *FirewallRuleName,* *StartIpAddress* e *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="7a344-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="7a344-120">Se si vuole consentire agli IP di Azure di accedere al server, questo parametro deve essere usato in una chiamata cmdlet separata che non usa i parametri *FirewallRuleName,* *StartIpAddress* e *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="7a344-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a344-121">-DefaultProfile</span></span>
<span data-ttu-id="7a344-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="7a344-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7a344-123">-EndIpAddress</span></span>
<span data-ttu-id="7a344-124">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="7a344-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="7a344-125">-FirewallRuleName</span></span>
<span data-ttu-id="7a344-126">Specifica il nome della nuova regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="7a344-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a344-127">-ResourceGroupName</span></span>
<span data-ttu-id="7a344-128">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="7a344-128">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a344-129">-ServerName</span></span>
<span data-ttu-id="7a344-130">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="7a344-130">Specifies the name of a server.</span></span>
<span data-ttu-id="7a344-131">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="7a344-131">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7a344-132">-StartIpAddress</span></span>
<span data-ttu-id="7a344-133">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="7a344-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a344-134">-Confirm</span></span>
<span data-ttu-id="7a344-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a344-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a344-136">-WhatIf</span></span>
<span data-ttu-id="7a344-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a344-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a344-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a344-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a344-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a344-139">CommonParameters</span></span>
<span data-ttu-id="7a344-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a344-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a344-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a344-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a344-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="7a344-142">INPUTS</span></span>

### <span data-ttu-id="7a344-143">System.String</span><span class="sxs-lookup"><span data-stu-id="7a344-143">System.String</span></span>

## <span data-ttu-id="7a344-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a344-144">OUTPUTS</span></span>

### <span data-ttu-id="7a344-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="7a344-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="7a344-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="7a344-146">NOTES</span></span>

## <span data-ttu-id="7a344-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a344-147">RELATED LINKS</span></span>

[<span data-ttu-id="7a344-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a344-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="7a344-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a344-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="7a344-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a344-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="7a344-151">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="7a344-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


