---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023528"
---
# <span data-ttu-id="b5b2f-101">Get-AzureSqlDatabaseServerQuota</span><span class="sxs-lookup"><span data-stu-id="b5b2f-101">Get-AzureSqlDatabaseServerQuota</span></span>

## <span data-ttu-id="b5b2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b2f-103">Ottiene le informazioni sulle quote per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-103">Gets quota information for an Azure SQL Database server.</span></span>

## <span data-ttu-id="b5b2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5b2f-104">SYNTAX</span></span>

### <span data-ttu-id="b5b2f-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b5b2f-105">ByConnectionContext</span></span>
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b5b2f-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="b5b2f-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5b2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5b2f-107">DESCRIPTION</span></span>
<span data-ttu-id="b5b2f-108">Il cmdlet **Get-AzureSqlDatabaseServerQuota** ottiene le informazioni sulle quote per un'istanza specificata del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-108">The **Get-AzureSqlDatabaseServerQuota** cmdlet gets the quota information for a specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="b5b2f-109">Specificare un contesto di connessione o il nome del server.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-109">Specify a connection context or the server name.</span></span>
<span data-ttu-id="b5b2f-110">Se non si specifica un nome di quota, questo cmdlet ottiene tutte le informazioni sulle quote per il server.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-110">If you do not specify a quota name, this cmdlet gets all the quota information for the server.</span></span>

## <span data-ttu-id="b5b2f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5b2f-111">EXAMPLES</span></span>

### <span data-ttu-id="b5b2f-112">Esempio 1: ottenere informazioni per una quota specifica</span><span class="sxs-lookup"><span data-stu-id="b5b2f-112">Example 1: Get information for a specific quota</span></span>
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

<span data-ttu-id="b5b2f-113">Questo comando ottiene la quota denominata Premium_Databases dal server di database SQL di Azure specificato dalla connessione archiviata nella variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-113">This command gets the quota named Premium_Databases from the Azure SQL Database server specified by the connection stored in the $Context variable.</span></span>

### <span data-ttu-id="b5b2f-114">Esempio 2: ottenere informazioni per tutte le quote</span><span class="sxs-lookup"><span data-stu-id="b5b2f-114">Example 2: Get information for all quotas</span></span>
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

<span data-ttu-id="b5b2f-115">Questo comando ottiene tutti i valori di quota dal server specificato dalla $Context di connessione.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-115">This command gets all quota values from the server specified by the connection $Context.</span></span>

## <span data-ttu-id="b5b2f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5b2f-116">PARAMETERS</span></span>

### <span data-ttu-id="b5b2f-117">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b5b2f-117">-ConnectionContext</span></span>
<span data-ttu-id="b5b2f-118">Specifica il contesto di connessione di un server.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-118">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b2f-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="b5b2f-119">-Profile</span></span>
<span data-ttu-id="b5b2f-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5b2f-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5b2f-122">-Quotaname</span><span class="sxs-lookup"><span data-stu-id="b5b2f-122">-QuotaName</span></span>
<span data-ttu-id="b5b2f-123">Specifica il nome del valore di quota ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-123">Specifies the name of the quota value that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5b2f-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b5b2f-124">-ServerName</span></span>
<span data-ttu-id="b5b2f-125">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-125">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5b2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b2f-126">CommonParameters</span></span>
<span data-ttu-id="b5b2f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b2f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b2f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b2f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5b2f-129">INPUTS</span></span>

## <span data-ttu-id="b5b2f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5b2f-130">OUTPUTS</span></span>

### <span data-ttu-id="b5b2f-131">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. ServerQuota []</span><span class="sxs-lookup"><span data-stu-id="b5b2f-131">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServerQuota[]</span></span>

## <span data-ttu-id="b5b2f-132">Note</span><span class="sxs-lookup"><span data-stu-id="b5b2f-132">NOTES</span></span>
* <span data-ttu-id="b5b2f-133">Autenticazione: questo cmdlet può usare l'autenticazione di SQL Server o l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-133">Authentication: This cmdlet can use either SQL Server authentication or certificate-based authentication.</span></span> <span data-ttu-id="b5b2f-134">Per esempi di configurazione dell'autenticazione, vedere il cmdlet New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="b5b2f-134">For examples of setting up authentication, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="b5b2f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5b2f-135">RELATED LINKS</span></span>

[<span data-ttu-id="b5b2f-136">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b5b2f-136">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b5b2f-137">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b5b2f-137">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b5b2f-138">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="b5b2f-138">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


