---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030021"
---
# <span data-ttu-id="6ff6c-101">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="6ff6c-101">Get-AzureSqlRecoverableDatabase</span></span>

## <span data-ttu-id="6ff6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ff6c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff6c-103">Ottiene i database recuperabili da un server specificato.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-103">Gets recoverable databases from a specified server.</span></span>

## <span data-ttu-id="6ff6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ff6c-104">SYNTAX</span></span>

### <span data-ttu-id="6ff6c-105">AllDatabasesOnGivenServer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ff6c-105">AllDatabasesOnGivenServer (Default)</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6ff6c-106">GivenDatabaseOnGivenServer</span><span class="sxs-lookup"><span data-stu-id="6ff6c-106">GivenDatabaseOnGivenServer</span></span>
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ff6c-107">GivenDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6ff6c-107">GivenDatabaseObject</span></span>
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ff6c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ff6c-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff6c-109">Il cmdlet **Get-AzureSqlRecoverableDatabase** ottiene i database recuperabili da un server specificato.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-109">The **Get-AzureSqlRecoverableDatabase** cmdlet gets recoverable databases from a specified server.</span></span>
<span data-ttu-id="6ff6c-110">Questo cmdlet ottiene uno specifico database reversibile o tutti i database recuperabili in un server.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-110">This cmdlet gets a specific recoverable database or all recoverable databases on a server.</span></span>

## <span data-ttu-id="6ff6c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ff6c-111">EXAMPLES</span></span>

### <span data-ttu-id="6ff6c-112">Esempio 1: ottenere tutti i database recuperabili</span><span class="sxs-lookup"><span data-stu-id="6ff6c-112">Example 1: Get all recoverable databases</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

<span data-ttu-id="6ff6c-113">Questo comando consente di ottenere tutti i database recuperabili nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-113">This command gets all recoverable databases on the server named Server01.</span></span>

### <span data-ttu-id="6ff6c-114">Esempio 2: ottenere uno specifico database reversibile</span><span class="sxs-lookup"><span data-stu-id="6ff6c-114">Example 2: Get a specific recoverable database</span></span>
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

<span data-ttu-id="6ff6c-115">Questo comando ottiene Recupera il database denominato Database17 nel server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-115">This command gets retrieves the database named Database17 on the server named Server01.</span></span>

## <span data-ttu-id="6ff6c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ff6c-116">PARAMETERS</span></span>

### <span data-ttu-id="6ff6c-117">-Database</span><span class="sxs-lookup"><span data-stu-id="6ff6c-117">-Database</span></span>
<span data-ttu-id="6ff6c-118">Specifica un oggetto che rappresenta il database recuperabile ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-118">Specifies an object that represents the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff6c-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ff6c-119">-DatabaseName</span></span>
<span data-ttu-id="6ff6c-120">Specifica il nome del database recuperabile ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-120">Specifies the name of the recoverable database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff6c-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ff6c-121">-Profile</span></span>
<span data-ttu-id="6ff6c-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ff6c-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ff6c-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6ff6c-124">-ServerName</span></span>
<span data-ttu-id="6ff6c-125">Specifica il nome del server da cui questo cmdlet ottiene i database recuperabili.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-125">Specifies the name of the server from which this cmdlet gets recoverable databases.</span></span>

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff6c-126">CommonParameters</span></span>
<span data-ttu-id="6ff6c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff6c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff6c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ff6c-129">INPUTS</span></span>

### <span data-ttu-id="6ff6c-130">Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="6ff6c-130">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="6ff6c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ff6c-131">OUTPUTS</span></span>

### <span data-ttu-id="6ff6c-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span><span class="sxs-lookup"><span data-stu-id="6ff6c-132">IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\></span></span>

## <span data-ttu-id="6ff6c-133">Note</span><span class="sxs-lookup"><span data-stu-id="6ff6c-133">NOTES</span></span>
* <span data-ttu-id="6ff6c-134">Per eseguire questo cmdlet, è necessario usare l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="6ff6c-134">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="6ff6c-135">Eseguire i comandi seguenti nel computer in cui eseguire questo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6ff6c-135">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="6ff6c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ff6c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6ff6c-137">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6ff6c-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="6ff6c-138">Ottenere un database reversibile</span><span class="sxs-lookup"><span data-stu-id="6ff6c-138">Get Recoverable Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[<span data-ttu-id="6ff6c-139">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6ff6c-139">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="6ff6c-140">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="6ff6c-140">Start-AzureSqlDatabaseRecovery</span></span>](./Start-AzureSqlDatabaseRecovery.md)


