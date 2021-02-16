---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197623"
---
# <span data-ttu-id="f0065-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f0065-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="f0065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0065-102">SYNOPSIS</span></span>
<span data-ttu-id="f0065-103">Modifica una regola del firewall in Azure SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="f0065-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="f0065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0065-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0065-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0065-105">DESCRIPTION</span></span>
<span data-ttu-id="f0065-106">Il cmdlet **Set-AzSqlServerFirewallRule** modifica una regola del firewall in un server di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="f0065-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="f0065-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0065-107">EXAMPLES</span></span>

### <span data-ttu-id="f0065-108">Esempio 1: Modificare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="f0065-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="f0065-109">Questo comando modifica una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="f0065-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="f0065-110">Il comando modifica gli indirizzi IP di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="f0065-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="f0065-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0065-111">PARAMETERS</span></span>

### <span data-ttu-id="f0065-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0065-112">-DefaultProfile</span></span>
<span data-ttu-id="f0065-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f0065-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0065-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0065-114">-EndIpAddress</span></span>
<span data-ttu-id="f0065-115">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="f0065-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="f0065-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f0065-116">-FirewallRuleName</span></span>
<span data-ttu-id="f0065-117">Specifica il nome della regola del firewall modificata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0065-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0065-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0065-118">-ResourceGroupName</span></span>
<span data-ttu-id="f0065-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="f0065-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f0065-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f0065-120">-ServerName</span></span>
<span data-ttu-id="f0065-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="f0065-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f0065-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0065-122">-StartIpAddress</span></span>
<span data-ttu-id="f0065-123">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="f0065-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="f0065-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0065-124">-Confirm</span></span>
<span data-ttu-id="f0065-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0065-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0065-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0065-126">-WhatIf</span></span>
<span data-ttu-id="f0065-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0065-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0065-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0065-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0065-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0065-129">CommonParameters</span></span>
<span data-ttu-id="f0065-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0065-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0065-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0065-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0065-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0065-132">INPUTS</span></span>

### <span data-ttu-id="f0065-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f0065-133">System.String</span></span>

## <span data-ttu-id="f0065-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0065-134">OUTPUTS</span></span>

### <span data-ttu-id="f0065-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="f0065-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f0065-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0065-136">NOTES</span></span>

## <span data-ttu-id="f0065-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0065-137">RELATED LINKS</span></span>

[<span data-ttu-id="f0065-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f0065-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f0065-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f0065-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f0065-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f0065-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f0065-141">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="f0065-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


