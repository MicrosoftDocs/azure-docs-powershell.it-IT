---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e0957e7c68a2332cbd50bbc42d703c41bb277b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509579"
---
# <span data-ttu-id="89ad9-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89ad9-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="89ad9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="89ad9-103">Modifica una regola del firewall nel server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="89ad9-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89ad9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89ad9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ad9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="89ad9-106">Il cmdlet **set-AzureRmSqlServerFirewallRule** modifica una regola del firewall in un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="89ad9-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="89ad9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89ad9-107">EXAMPLES</span></span>

### <span data-ttu-id="89ad9-108">Esempio 1: modificare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="89ad9-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="89ad9-109">Questo comando consente di modificare una regola del firewall denominata Rule01 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="89ad9-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="89ad9-110">Il comando modifica gli indirizzi IP di inizio e fine.</span><span class="sxs-lookup"><span data-stu-id="89ad9-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="89ad9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89ad9-111">PARAMETERS</span></span>

### <span data-ttu-id="89ad9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ad9-112">-DefaultProfile</span></span>
<span data-ttu-id="89ad9-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="89ad9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="89ad9-114">-EndIpAddress</span></span>
<span data-ttu-id="89ad9-115">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="89ad9-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="89ad9-116">-FirewallRuleName</span></span>
<span data-ttu-id="89ad9-117">Specifica il nome della regola del firewall che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="89ad9-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ad9-118">-ResourceGroupName</span></span>
<span data-ttu-id="89ad9-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="89ad9-119">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="89ad9-120">-ServerName</span></span>
<span data-ttu-id="89ad9-121">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="89ad9-121">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="89ad9-122">-StartIpAddress</span></span>
<span data-ttu-id="89ad9-123">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="89ad9-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="89ad9-124">-Confirm</span></span>
<span data-ttu-id="89ad9-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89ad9-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ad9-126">-WhatIf</span></span>
<span data-ttu-id="89ad9-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89ad9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ad9-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89ad9-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ad9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ad9-129">CommonParameters</span></span>
<span data-ttu-id="89ad9-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ad9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ad9-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ad9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ad9-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89ad9-132">INPUTS</span></span>

### <span data-ttu-id="89ad9-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="89ad9-133">None</span></span>
<span data-ttu-id="89ad9-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="89ad9-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89ad9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89ad9-135">OUTPUTS</span></span>

### <span data-ttu-id="89ad9-136">Microsoft. Azure. Commands. SQL. FirewallRule. Model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="89ad9-136">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="89ad9-137">Note</span><span class="sxs-lookup"><span data-stu-id="89ad9-137">NOTES</span></span>

## <span data-ttu-id="89ad9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89ad9-138">RELATED LINKS</span></span>

[<span data-ttu-id="89ad9-139">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89ad9-139">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="89ad9-140">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89ad9-140">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="89ad9-141">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89ad9-141">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="89ad9-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="89ad9-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


