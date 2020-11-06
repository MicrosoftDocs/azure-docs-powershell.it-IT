---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 0e07ce9eb3f3368e17c20a339c65a410b5f1d553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512855"
---
# <span data-ttu-id="cbcea-101">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cbcea-101">Get-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="cbcea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbcea-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcea-103">Ottiene o elenca i gruppi di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="cbcea-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbcea-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbcea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbcea-105">DESCRIPTION</span></span>
<span data-ttu-id="cbcea-106">Ottiene un gruppo di failover di database SQL di Azure specifico o elenca i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="cbcea-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>

<span data-ttu-id="cbcea-107">Per eseguire il comando, è possibile che venga usato un server nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="cbcea-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="cbcea-108">I valori restituiti riflettono lo stato del server specificato rispetto al gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="cbcea-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="cbcea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbcea-109">EXAMPLES</span></span>

### <span data-ttu-id="cbcea-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cbcea-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="cbcea-111">Elenca tutti i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="cbcea-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="cbcea-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cbcea-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="cbcea-113">Ottenere un gruppo di failover specifico.</span><span class="sxs-lookup"><span data-stu-id="cbcea-113">Get a specific Failover Group.</span></span>

## <span data-ttu-id="cbcea-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbcea-114">PARAMETERS</span></span>

### <span data-ttu-id="cbcea-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcea-115">-FailoverGroupName</span></span>
<span data-ttu-id="cbcea-116">Il nome del gruppo di failover di database SQL di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="cbcea-116">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcea-117">-ResourceGroupName</span></span>
<span data-ttu-id="cbcea-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cbcea-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cbcea-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="cbcea-119">-ServerName</span></span>
<span data-ttu-id="cbcea-120">Nome del server di database SQL di Azure da cui recuperare il gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="cbcea-120">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="cbcea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcea-121">-DefaultProfile</span></span>
<span data-ttu-id="cbcea-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbcea-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbcea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcea-123">CommonParameters</span></span>
<span data-ttu-id="cbcea-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcea-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcea-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbcea-126">INPUTS</span></span>

### <span data-ttu-id="cbcea-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cbcea-127">System.String</span></span>

## <span data-ttu-id="cbcea-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbcea-128">OUTPUTS</span></span>

### <span data-ttu-id="cbcea-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="cbcea-129">System.Object</span></span>

## <span data-ttu-id="cbcea-130">Note</span><span class="sxs-lookup"><span data-stu-id="cbcea-130">NOTES</span></span>

## <span data-ttu-id="cbcea-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbcea-131">RELATED LINKS</span></span>

[<span data-ttu-id="cbcea-132">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cbcea-132">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cbcea-133">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cbcea-133">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cbcea-134">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cbcea-134">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="cbcea-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cbcea-135">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="cbcea-136">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cbcea-136">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cbcea-137">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="cbcea-137">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="cbcea-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="cbcea-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
