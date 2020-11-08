---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023530"
---
# <span data-ttu-id="d1cba-101">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1cba-101">Get-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="d1cba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1cba-102">SYNOPSIS</span></span>
<span data-ttu-id="d1cba-103">Ottiene le regole del firewall per il server database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1cba-103">Gets firewall rules for Azure SQL Database Server.</span></span>

## <span data-ttu-id="d1cba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1cba-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1cba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1cba-105">DESCRIPTION</span></span>
<span data-ttu-id="d1cba-106">Il cmdlet **Get-AzureSqlDatabaseServerFirewallRule** ottiene le regole del firewall per un'istanza del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1cba-106">The **Get-AzureSqlDatabaseServerFirewallRule** cmdlet gets firewall rules for an instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="d1cba-107">Se si specifica una regola del firewall per nome, questo cmdlet restituisce le informazioni sulla regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="d1cba-107">If you specify a firewall rule by name, this cmdlet returns information about that firewall rule.</span></span>
<span data-ttu-id="d1cba-108">In caso contrario, il cmdlet restituisce informazioni su tutte le regole del firewall nel server di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="d1cba-108">Otherwise, the cmdlet returns information about all the firewall rules on the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="d1cba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1cba-109">EXAMPLES</span></span>

### <span data-ttu-id="d1cba-110">Esempio 1: ottenere tutte le regole del firewall in un server</span><span class="sxs-lookup"><span data-stu-id="d1cba-110">Example 1: Get all firewall rules on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="d1cba-111">Questo comando consente di ottenere tutte le regole del firewall nel server di database SQL di Azure denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="d1cba-111">This command gets all the firewall rules on the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="d1cba-112">Esempio 2: ottenere una regola del firewall usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="d1cba-112">Example 2: Get a firewall rule by using its name</span></span>
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

<span data-ttu-id="d1cba-113">Questo comando consente di ottenere la regola del firewall denominata FirewallRule24 nel server denominata lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="d1cba-113">This command gets the firewall rule named FirewallRule24 on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="d1cba-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1cba-114">PARAMETERS</span></span>

### <span data-ttu-id="d1cba-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="d1cba-115">-Profile</span></span>
<span data-ttu-id="d1cba-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1cba-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1cba-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d1cba-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1cba-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="d1cba-118">-RuleName</span></span>
<span data-ttu-id="d1cba-119">Specifica il nome della regola del firewall ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1cba-119">Specifies the name of the firewall rule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cba-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d1cba-120">-ServerName</span></span>
<span data-ttu-id="d1cba-121">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="d1cba-121">Specifies the name of a server.</span></span>
<span data-ttu-id="d1cba-122">Questo cmdlet ottiene le regole del firewall dal server specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d1cba-122">This cmdlet gets firewall rules from the server that this parameter specifies.</span></span>
<span data-ttu-id="d1cba-123">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="d1cba-123">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1cba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1cba-124">CommonParameters</span></span>
<span data-ttu-id="d1cba-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1cba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1cba-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1cba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1cba-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1cba-127">INPUTS</span></span>

### <span data-ttu-id="d1cba-128">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="d1cba-128">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="d1cba-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1cba-129">OUTPUTS</span></span>

### <span data-ttu-id="d1cba-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span><span class="sxs-lookup"><span data-stu-id="d1cba-130">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\></span></span>

## <span data-ttu-id="d1cba-131">Note</span><span class="sxs-lookup"><span data-stu-id="d1cba-131">NOTES</span></span>

## <span data-ttu-id="d1cba-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1cba-132">RELATED LINKS</span></span>

[<span data-ttu-id="d1cba-133">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="d1cba-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="d1cba-134">Regole del firewall elenco</span><span class="sxs-lookup"><span data-stu-id="d1cba-134">List Firewall Rules</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[<span data-ttu-id="d1cba-135">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="d1cba-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="d1cba-136">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1cba-136">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="d1cba-137">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1cba-137">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="d1cba-138">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1cba-138">Set-AzureSqlDatabaseServerFirewallRule</span></span>](./Set-AzureSqlDatabaseServerFirewallRule.md)


