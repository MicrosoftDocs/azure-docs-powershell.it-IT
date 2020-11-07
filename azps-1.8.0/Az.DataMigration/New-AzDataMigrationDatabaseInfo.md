---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: f1feead56c25b76890edd0fe183e65211294cf87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684499"
---
# <span data-ttu-id="3e500-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="3e500-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="3e500-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e500-102">SYNOPSIS</span></span>
<span data-ttu-id="3e500-103">Crea l'oggetto DatabaseInfo per il servizio di migrazione del database di Azure, che specifica l'origine del database per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="3e500-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="3e500-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e500-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e500-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e500-105">DESCRIPTION</span></span>
<span data-ttu-id="3e500-106">Il cmdlet New-AzDataMigrationDatabaseInfo crea l'oggetto DatabaseInfo che specifica l'istanza del database di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="3e500-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="3e500-107">Il nome del database viene considerato come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="3e500-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="3e500-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e500-108">EXAMPLES</span></span>

### <span data-ttu-id="3e500-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e500-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="3e500-110">Nell'esempio precedente viene creato un nuovo oggetto DatabaseInfo per il database di origine **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="3e500-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="3e500-111">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e500-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="3e500-112">Puoi confermare lo stato di accesso usando il cmdlet Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="3e500-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="3e500-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e500-113">PARAMETERS</span></span>

### <span data-ttu-id="3e500-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e500-114">-DefaultProfile</span></span>
<span data-ttu-id="3e500-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e500-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e500-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e500-116">-SourceDatabaseName</span></span>
<span data-ttu-id="3e500-117">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="3e500-117">Source Database Name.</span></span>

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

### <span data-ttu-id="3e500-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e500-118">CommonParameters</span></span>
<span data-ttu-id="3e500-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e500-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e500-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e500-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e500-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e500-121">INPUTS</span></span>

### <span data-ttu-id="3e500-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3e500-122">None</span></span>

## <span data-ttu-id="3e500-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e500-123">OUTPUTS</span></span>

### <span data-ttu-id="3e500-124">Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="3e500-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="3e500-125">Note</span><span class="sxs-lookup"><span data-stu-id="3e500-125">NOTES</span></span>

## <span data-ttu-id="3e500-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e500-126">RELATED LINKS</span></span>
