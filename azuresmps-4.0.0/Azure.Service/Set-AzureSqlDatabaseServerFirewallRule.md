---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023821"
---
# <span data-ttu-id="777c2-101">Set-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="777c2-101">Set-AzureSqlDatabaseServerFirewallRule</span></span>

## <span data-ttu-id="777c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="777c2-102">SYNOPSIS</span></span>
<span data-ttu-id="777c2-103">Modifica una regola del firewall esistente in un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="777c2-103">Modifies an existing firewall rule in an Azure SQL Database Server.</span></span>

## <span data-ttu-id="777c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="777c2-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="777c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="777c2-105">DESCRIPTION</span></span>
<span data-ttu-id="777c2-106">Il cmdlet **set-AzureSqlDatabaseServerFirewallRule** modifica l'indirizzo IP iniziale e i valori degli indirizzi IP finali di una regola del firewall esistente nell'istanza specificata del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="777c2-106">The **Set-AzureSqlDatabaseServerFirewallRule** cmdlet modifies the start IP address and end IP address values of an existing firewall rule in the specified instance of Azure SQL Database Server.</span></span>

## <span data-ttu-id="777c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="777c2-107">EXAMPLES</span></span>

### <span data-ttu-id="777c2-108">Esempio 1: modificare una regola del firewall</span><span class="sxs-lookup"><span data-stu-id="777c2-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

<span data-ttu-id="777c2-109">Questo comando consente di modificare l'indirizzo IP iniziale e l'indirizzo IP finale della regola del firewall denominata FirewallRule24 nel server di database SQL di Azure denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="777c2-109">This command modifies the start IP address and end IP address of the firewall rule named FirewallRule24 on the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="777c2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="777c2-110">PARAMETERS</span></span>

### <span data-ttu-id="777c2-111">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="777c2-111">-EndIpAddress</span></span>
<span data-ttu-id="777c2-112">Specifica il valore finale dell'intervallo di indirizzi IP per la regola.</span><span class="sxs-lookup"><span data-stu-id="777c2-112">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="777c2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="777c2-113">-Force</span></span>
<span data-ttu-id="777c2-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="777c2-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="777c2-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="777c2-115">-Profile</span></span>
<span data-ttu-id="777c2-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="777c2-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="777c2-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="777c2-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="777c2-118">-RuleName</span><span class="sxs-lookup"><span data-stu-id="777c2-118">-RuleName</span></span>
<span data-ttu-id="777c2-119">Specifica il nome della regola del firewall che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="777c2-119">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="777c2-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="777c2-120">-ServerName</span></span>
<span data-ttu-id="777c2-121">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="777c2-121">Specifies the name of a server.</span></span>
<span data-ttu-id="777c2-122">Questo cmdlet crea una regola del firewall nel server specificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="777c2-122">This cmdlet creates a firewall rule on the server that this cmdlet specifies.</span></span>
<span data-ttu-id="777c2-123">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="777c2-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="777c2-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="777c2-124">-StartIpAddress</span></span>
<span data-ttu-id="777c2-125">Specifica il valore iniziale dell'intervallo di indirizzi IP per la regola del firewall.</span><span class="sxs-lookup"><span data-stu-id="777c2-125">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="777c2-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="777c2-126">-Confirm</span></span>
<span data-ttu-id="777c2-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="777c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="777c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="777c2-128">-WhatIf</span></span>
<span data-ttu-id="777c2-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="777c2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="777c2-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="777c2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="777c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777c2-131">CommonParameters</span></span>
<span data-ttu-id="777c2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="777c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777c2-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="777c2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777c2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="777c2-134">INPUTS</span></span>

### <span data-ttu-id="777c2-135">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="777c2-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="777c2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="777c2-136">OUTPUTS</span></span>

### <span data-ttu-id="777c2-137">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerFirewallRuleContext</span><span class="sxs-lookup"><span data-stu-id="777c2-137">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext</span></span>

## <span data-ttu-id="777c2-138">Note</span><span class="sxs-lookup"><span data-stu-id="777c2-138">NOTES</span></span>

## <span data-ttu-id="777c2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="777c2-139">RELATED LINKS</span></span>

[<span data-ttu-id="777c2-140">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="777c2-140">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="777c2-141">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="777c2-141">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="777c2-142">Impostare la regola del firewall</span><span class="sxs-lookup"><span data-stu-id="777c2-142">Set Firewall Rule</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[<span data-ttu-id="777c2-143">Get-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="777c2-143">Get-AzureSqlDatabaseServerFirewallRule</span></span>](./Get-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="777c2-144">New-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="777c2-144">New-AzureSqlDatabaseServerFirewallRule</span></span>](./New-AzureSqlDatabaseServerFirewallRule.md)

[<span data-ttu-id="777c2-145">Remove-AzureSqlDatabaseServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="777c2-145">Remove-AzureSqlDatabaseServerFirewallRule</span></span>](./Remove-AzureSqlDatabaseServerFirewallRule.md)


