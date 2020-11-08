---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F73A078E-F9F2-4520-BF55-DFFE82BE4466
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a8127a77ecfdc5aa36659060cb5469206a9988d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029569"
---
# <span data-ttu-id="fc972-101">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="fc972-101">Remove-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="fc972-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc972-102">SYNOPSIS</span></span>
<span data-ttu-id="fc972-103">Rimuove un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc972-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="fc972-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc972-104">SYNTAX</span></span>

```
Remove-AzureSqlDatabaseServer -ServerName <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc972-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc972-105">DESCRIPTION</span></span>
<span data-ttu-id="fc972-106">Il cmdlet **Remove-AzureSqlDatabaseServer** rimuove l'istanza specificata del server di database SQL di Azure dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="fc972-106">The **Remove-AzureSqlDatabaseServer** cmdlet removes the specified instance of Azure SQL Database Server from the current subscription.</span></span>
<span data-ttu-id="fc972-107">Questo cmdlet elimina tutti i database nel server.</span><span class="sxs-lookup"><span data-stu-id="fc972-107">This cmdlet deletes all databases on the server.</span></span>

## <span data-ttu-id="fc972-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc972-108">EXAMPLES</span></span>

### <span data-ttu-id="fc972-109">Esempio 1: rimuovere un server di database</span><span class="sxs-lookup"><span data-stu-id="fc972-109">Example 1: Remove a database server</span></span>
```
PS C:\>Remove-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="fc972-110">Questo comando rimuove il server di database SQL di Azure denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="fc972-110">This command removes the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="fc972-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc972-111">PARAMETERS</span></span>

### <span data-ttu-id="fc972-112">-Force</span><span class="sxs-lookup"><span data-stu-id="fc972-112">-Force</span></span>
<span data-ttu-id="fc972-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fc972-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc972-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="fc972-114">-Profile</span></span>
<span data-ttu-id="fc972-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc972-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc972-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="fc972-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc972-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fc972-117">-ServerName</span></span>
<span data-ttu-id="fc972-118">Specifica il nome del server rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc972-118">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="fc972-119">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="fc972-119">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="fc972-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc972-120">-Confirm</span></span>
<span data-ttu-id="fc972-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc972-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc972-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc972-122">-WhatIf</span></span>
<span data-ttu-id="fc972-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc972-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc972-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc972-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc972-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc972-125">CommonParameters</span></span>
<span data-ttu-id="fc972-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc972-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc972-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc972-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc972-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc972-128">INPUTS</span></span>

### <span data-ttu-id="fc972-129">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="fc972-129">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="fc972-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc972-130">OUTPUTS</span></span>

## <span data-ttu-id="fc972-131">Note</span><span class="sxs-lookup"><span data-stu-id="fc972-131">NOTES</span></span>

## <span data-ttu-id="fc972-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc972-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc972-133">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fc972-133">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="fc972-134">Eliminare il server</span><span class="sxs-lookup"><span data-stu-id="fc972-134">Delete Server</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505695.aspx)

[<span data-ttu-id="fc972-135">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="fc972-135">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="fc972-136">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="fc972-136">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="fc972-137">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="fc972-137">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="fc972-138">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="fc972-138">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


