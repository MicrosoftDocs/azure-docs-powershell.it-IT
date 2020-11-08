---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189302"
---
# <span data-ttu-id="e9c41-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e9c41-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="e9c41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9c41-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c41-103">Crea una regola del firewall per un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="e9c41-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="e9c41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9c41-104">SYNTAX</span></span>

### <span data-ttu-id="e9c41-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9c41-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9c41-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9c41-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9c41-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9c41-107">DESCRIPTION</span></span>
<span data-ttu-id="e9c41-108">Il cmdlet **New-AzSqlServerFirewallRule** crea una regola del firewall per il server di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="e9c41-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="e9c41-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9c41-109">EXAMPLES</span></span>

### <span data-ttu-id="e9c41-110">Esempio 1: creare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="e9c41-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="e9c41-111">Questo comando crea una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="e9c41-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="e9c41-112">La regola include gli indirizzi IP iniziali e finali specificati.</span><span class="sxs-lookup"><span data-stu-id="e9c41-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="e9c41-113">Esempio 2: creare una regola del firewall che consente a tutti gli indirizzi IP di Azure di accedere al server</span><span class="sxs-lookup"><span data-stu-id="e9c41-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="e9c41-114">Questo comando crea una regola del firewall nel server denominata Server01 che appartiene al gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="e9c41-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="e9c41-115">Poiché viene usato il parametro *AllowAllAzureIPs* , la regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="e9c41-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="e9c41-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9c41-116">PARAMETERS</span></span>

### <span data-ttu-id="e9c41-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="e9c41-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="e9c41-118">Indica che questa regola del firewall consente a tutti gli indirizzi IP di Azure di accedere al server.</span><span class="sxs-lookup"><span data-stu-id="e9c41-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="e9c41-119">Non è possibile usare questo parametro se si intende usare i parametri *FirewallRuleName* , *StartIpAddress* e *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="e9c41-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="e9c41-120">Se vuoi consentire ad Azure IPs di accedere al server, questo parametro deve essere usato in una chiamata cmdlet separata che non usa i parametri *FirewallRuleName* , *StartIpAddress* e *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="e9c41-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="e9c41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c41-121">-DefaultProfile</span></span>
<span data-ttu-id="e9c41-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e9c41-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9c41-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9c41-123">-EndIpAddress</span></span>
<span data-ttu-id="e9c41-124">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="e9c41-124">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="e9c41-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="e9c41-125">-FirewallRuleName</span></span>
<span data-ttu-id="e9c41-126">Specifica il nome della nuova regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e9c41-126">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="e9c41-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c41-127">-ResourceGroupName</span></span>
<span data-ttu-id="e9c41-128">Specifica il nome di un gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="e9c41-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e9c41-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e9c41-129">-ServerName</span></span>
<span data-ttu-id="e9c41-130">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="e9c41-130">Specifies the name of a server.</span></span>
<span data-ttu-id="e9c41-131">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="e9c41-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="e9c41-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e9c41-132">-StartIpAddress</span></span>
<span data-ttu-id="e9c41-133">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="e9c41-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="e9c41-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9c41-134">-Confirm</span></span>
<span data-ttu-id="e9c41-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9c41-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c41-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c41-136">-WhatIf</span></span>
<span data-ttu-id="e9c41-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9c41-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9c41-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9c41-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c41-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c41-139">CommonParameters</span></span>
<span data-ttu-id="e9c41-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c41-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c41-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9c41-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c41-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9c41-142">INPUTS</span></span>

### <span data-ttu-id="e9c41-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c41-143">System.String</span></span>

## <span data-ttu-id="e9c41-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9c41-144">OUTPUTS</span></span>

### <span data-ttu-id="e9c41-145">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="e9c41-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="e9c41-146">Note</span><span class="sxs-lookup"><span data-stu-id="e9c41-146">NOTES</span></span>

## <span data-ttu-id="e9c41-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9c41-147">RELATED LINKS</span></span>

[<span data-ttu-id="e9c41-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e9c41-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e9c41-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e9c41-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e9c41-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e9c41-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="e9c41-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="e9c41-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

