---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 07179b5fb139ba43b341114e2bf597fbbca05ed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955198"
---
# <span data-ttu-id="d399f-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d399f-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="d399f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d399f-102">SYNOPSIS</span></span>
<span data-ttu-id="d399f-103">Crea una regola del firewall per un server SQL database.</span><span class="sxs-lookup"><span data-stu-id="d399f-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="d399f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d399f-104">SYNTAX</span></span>

### <span data-ttu-id="d399f-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d399f-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d399f-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="d399f-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d399f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d399f-107">DESCRIPTION</span></span>
<span data-ttu-id="d399f-108">Il cmdlet **New-AzSqlServerFirewallRule** crea una regola del firewall per il server di database SQL Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="d399f-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="d399f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d399f-109">EXAMPLES</span></span>

### <span data-ttu-id="d399f-110">Esempio 1: Creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="d399f-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="d399f-111">Questo comando crea una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="d399f-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="d399f-112">La regola include gli indirizzi IP di inizio e di fine specificati.</span><span class="sxs-lookup"><span data-stu-id="d399f-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="d399f-113">Esempio 2: Creare una regola del firewall che consente a tutti gli indirizzi IP di Azure di accedere al server</span><span class="sxs-lookup"><span data-stu-id="d399f-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="d399f-114">Questo comando crea una regola del firewall nel server denominato Server01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="d399f-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="d399f-115">Poiché viene *usato il parametro AllowAllAzureIPs,* la regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="d399f-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="d399f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d399f-116">PARAMETERS</span></span>

### <span data-ttu-id="d399f-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="d399f-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="d399f-118">Indica che questa regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="d399f-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="d399f-119">Non è possibile usare questo parametro se si intende usare i parametri *FirewallRuleName,* *StartIpAddress* e *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="d399f-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="d399f-120">Se si vuole consentire agli IP di Azure di accedere al server, questo parametro deve essere usato in una chiamata cmdlet separata che non usa i parametri *FirewallRuleName,* *StartIpAddress* e *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="d399f-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="d399f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d399f-121">-DefaultProfile</span></span>
<span data-ttu-id="d399f-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d399f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d399f-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d399f-123">-EndIpAddress</span></span>
<span data-ttu-id="d399f-124">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="d399f-124">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="d399f-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="d399f-125">-FirewallRuleName</span></span>
<span data-ttu-id="d399f-126">Specifica il nome della nuova regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="d399f-126">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="d399f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d399f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d399f-128">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="d399f-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="d399f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d399f-129">-ServerName</span></span>
<span data-ttu-id="d399f-130">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="d399f-130">Specifies the name of a server.</span></span>
<span data-ttu-id="d399f-131">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="d399f-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="d399f-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d399f-132">-StartIpAddress</span></span>
<span data-ttu-id="d399f-133">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="d399f-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="d399f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d399f-134">-Confirm</span></span>
<span data-ttu-id="d399f-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d399f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d399f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d399f-136">-WhatIf</span></span>
<span data-ttu-id="d399f-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d399f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d399f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d399f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d399f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d399f-139">CommonParameters</span></span>
<span data-ttu-id="d399f-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d399f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d399f-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d399f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d399f-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="d399f-142">INPUTS</span></span>

### <span data-ttu-id="d399f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d399f-143">System.String</span></span>

## <span data-ttu-id="d399f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d399f-144">OUTPUTS</span></span>

### <span data-ttu-id="d399f-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="d399f-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="d399f-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="d399f-146">NOTES</span></span>

## <span data-ttu-id="d399f-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d399f-147">RELATED LINKS</span></span>

[<span data-ttu-id="d399f-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d399f-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="d399f-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d399f-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="d399f-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d399f-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="d399f-151">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="d399f-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


