---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023529"
---
# <span data-ttu-id="6c6d5-101">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6c6d5-101">Get-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="6c6d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c6d5-103">Ottiene informazioni sui server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-103">Gets information about Azure SQL Database servers.</span></span>

## <span data-ttu-id="6c6d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c6d5-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6c6d5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c6d5-105">DESCRIPTION</span></span>
<span data-ttu-id="6c6d5-106">Il cmdlet **Get-AzureSqlDatabaseServer** ottiene informazioni sulle istanze del server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-106">The **Get-AzureSqlDatabaseServer** cmdlet gets information about the instances of Azure SQL Database Server in the current subscription.</span></span>
<span data-ttu-id="6c6d5-107">Se specifichi un server per nome, questo cmdlet restituisce un oggetto che contiene informazioni sul server.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-107">If you specify a server by name, this cmdlet returns an object that contains information about that server.</span></span>
<span data-ttu-id="6c6d5-108">In caso contrario, il cmdlet restituisce informazioni su tutti i server.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-108">Otherwise, the cmdlet returns information about all the servers.</span></span>

## <span data-ttu-id="6c6d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c6d5-109">EXAMPLES</span></span>

### <span data-ttu-id="6c6d5-110">Esempio 1: ottenere informazioni su tutti i server</span><span class="sxs-lookup"><span data-stu-id="6c6d5-110">Example 1: Get information about all servers</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer
```

<span data-ttu-id="6c6d5-111">Questo comando restituisce informazioni su tutte le istanze del server di database SQL di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-111">This command returns information about all instances of Azure SQL Database Server in the current subscription.</span></span>

### <span data-ttu-id="6c6d5-112">Esempio 2: ottenere informazioni su un server specifico</span><span class="sxs-lookup"><span data-stu-id="6c6d5-112">Example 2: Get information about a specific server</span></span>
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="6c6d5-113">Questo comando restituisce informazioni sul server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-113">This command returns information about the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="6c6d5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c6d5-114">PARAMETERS</span></span>

### <span data-ttu-id="6c6d5-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="6c6d5-115">-Profile</span></span>
<span data-ttu-id="6c6d5-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c6d5-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c6d5-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6c6d5-118">-ServerName</span></span>
<span data-ttu-id="6c6d5-119">Specifica il nome del server rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-119">Specifies the name of the server that this cmdlet removes.</span></span>
<span data-ttu-id="6c6d5-120">Specificare il nome del server e non il nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-120">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="6c6d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c6d5-121">CommonParameters</span></span>
<span data-ttu-id="6c6d5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c6d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c6d5-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c6d5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c6d5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c6d5-124">INPUTS</span></span>

### <span data-ttu-id="6c6d5-125">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="6c6d5-125">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="6c6d5-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c6d5-126">OUTPUTS</span></span>

### <span data-ttu-id="6c6d5-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span><span class="sxs-lookup"><span data-stu-id="6c6d5-127">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\></span></span>

## <span data-ttu-id="6c6d5-128">Note</span><span class="sxs-lookup"><span data-stu-id="6c6d5-128">NOTES</span></span>

## <span data-ttu-id="6c6d5-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c6d5-129">RELATED LINKS</span></span>

[<span data-ttu-id="6c6d5-130">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6c6d5-130">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="6c6d5-131">Elenco Server</span><span class="sxs-lookup"><span data-stu-id="6c6d5-131">List Servers</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[<span data-ttu-id="6c6d5-132">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6c6d5-132">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="6c6d5-133">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6c6d5-133">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="6c6d5-134">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6c6d5-134">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)

[<span data-ttu-id="6c6d5-135">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="6c6d5-135">Set-AzureSqlDatabaseServer</span></span>](./Set-AzureSqlDatabaseServer.md)


