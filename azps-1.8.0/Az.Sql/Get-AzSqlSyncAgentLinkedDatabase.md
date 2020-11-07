---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 6ef3a84e84e001943cef1791c77f6c2a354da8ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676877"
---
# <span data-ttu-id="0c92d-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="0c92d-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="0c92d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c92d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c92d-103">Restituisce informazioni sui database di SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c92d-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="0c92d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c92d-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c92d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c92d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c92d-106">Il cmdlet **Get-AzSqlSyncAgentLinkedDatabases** restituisce informazioni sui database di SQL Server collegati da un agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c92d-106">The **Get-AzSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="0c92d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c92d-107">EXAMPLES</span></span>

### <span data-ttu-id="0c92d-108">Esempio 1: ottenere i database di SQL Server collegati per un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c92d-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="0c92d-109">Questo comando restituisce i database di SQL Server collegati collegati da un agente di sincronizzazione SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c92d-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="0c92d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c92d-110">PARAMETERS</span></span>

### <span data-ttu-id="0c92d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c92d-111">-DefaultProfile</span></span>
<span data-ttu-id="0c92d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c92d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c92d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c92d-113">-ResourceGroupName</span></span>
<span data-ttu-id="0c92d-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c92d-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="0c92d-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0c92d-115">-ServerName</span></span>
<span data-ttu-id="0c92d-116">Nome di Azure SQL Server in cui si trova l'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c92d-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="0c92d-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="0c92d-117">-SyncAgentName</span></span>
<span data-ttu-id="0c92d-118">Nome dell'agente di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c92d-118">The sync agent name.</span></span>

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

### <span data-ttu-id="0c92d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c92d-119">CommonParameters</span></span>
<span data-ttu-id="0c92d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c92d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c92d-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c92d-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c92d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c92d-122">INPUTS</span></span>

### <span data-ttu-id="0c92d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0c92d-123">System.String</span></span>

## <span data-ttu-id="0c92d-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c92d-124">OUTPUTS</span></span>

### <span data-ttu-id="0c92d-125">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="0c92d-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="0c92d-126">Note</span><span class="sxs-lookup"><span data-stu-id="0c92d-126">NOTES</span></span>

## <span data-ttu-id="0c92d-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c92d-127">RELATED LINKS</span></span>
