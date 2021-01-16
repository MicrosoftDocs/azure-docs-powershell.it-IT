---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387572"
---
# <span data-ttu-id="db05a-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="db05a-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="db05a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db05a-102">SYNOPSIS</span></span>
<span data-ttu-id="db05a-103">Crea l'oggetto DatabaseInfo per il servizio di migrazione del database di Azure, che specifica l'origine del database per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="db05a-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="db05a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db05a-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db05a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db05a-105">DESCRIPTION</span></span>
<span data-ttu-id="db05a-106">Il cmdlet New-AzDataMigrationDatabaseInfo crea l'oggetto DatabaseInfo che specifica l'istanza del database di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="db05a-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="db05a-107">Il nome del database viene considerato come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="db05a-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="db05a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db05a-108">EXAMPLES</span></span>

### <span data-ttu-id="db05a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db05a-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="db05a-110">Nell'esempio precedente viene creato un nuovo oggetto DatabaseInfo per il database di origine **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="db05a-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="db05a-111">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="db05a-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="db05a-112">Puoi confermare lo stato di accesso usando il cmdlet Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="db05a-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="db05a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db05a-113">PARAMETERS</span></span>

### <span data-ttu-id="db05a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db05a-114">-DefaultProfile</span></span>
<span data-ttu-id="db05a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db05a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db05a-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="db05a-116">-SourceDatabaseName</span></span>
<span data-ttu-id="db05a-117">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="db05a-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db05a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db05a-118">CommonParameters</span></span>
<span data-ttu-id="db05a-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db05a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db05a-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db05a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db05a-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db05a-121">INPUTS</span></span>

### <span data-ttu-id="db05a-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="db05a-122">None</span></span>

## <span data-ttu-id="db05a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db05a-123">OUTPUTS</span></span>

### <span data-ttu-id="db05a-124">Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="db05a-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="db05a-125">Note</span><span class="sxs-lookup"><span data-stu-id="db05a-125">NOTES</span></span>

## <span data-ttu-id="db05a-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db05a-126">RELATED LINKS</span></span>
