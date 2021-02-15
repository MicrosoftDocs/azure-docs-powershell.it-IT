---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209778"
---
# <span data-ttu-id="56208-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="56208-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="56208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56208-102">SYNOPSIS</span></span>
<span data-ttu-id="56208-103">Crea l'oggetto DatabaseInfo per il servizio di migrazione del database di Azure, che specifica l'origine del database per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="56208-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="56208-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56208-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56208-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56208-105">DESCRIPTION</span></span>
<span data-ttu-id="56208-106">Il cmdlet New-AzDataMigrationDatabaseInfo crea l'oggetto DatabaseInfo che specifica l'istanza del database di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="56208-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="56208-107">Il nome del database viene immesso come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="56208-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="56208-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56208-108">EXAMPLES</span></span>

### <span data-ttu-id="56208-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56208-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="56208-110">Nell'esempio precedente viene creato un nuovo oggetto DatabaseInfo per il database di origine **AdventureWorks2016.**</span><span class="sxs-lookup"><span data-stu-id="56208-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="56208-111">Questo script presuppone che l'utente sia già connesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="56208-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="56208-112">È possibile confermare lo stato di accesso usando il cmdlet Get-AzSubscription.</span><span class="sxs-lookup"><span data-stu-id="56208-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="56208-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56208-113">PARAMETERS</span></span>

### <span data-ttu-id="56208-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56208-114">-DefaultProfile</span></span>
<span data-ttu-id="56208-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56208-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56208-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="56208-116">-SourceDatabaseName</span></span>
<span data-ttu-id="56208-117">Nome database di origine.</span><span class="sxs-lookup"><span data-stu-id="56208-117">Source Database Name.</span></span>

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

### <span data-ttu-id="56208-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56208-118">CommonParameters</span></span>
<span data-ttu-id="56208-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56208-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56208-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56208-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56208-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="56208-121">INPUTS</span></span>

### <span data-ttu-id="56208-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56208-122">None</span></span>

## <span data-ttu-id="56208-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56208-123">OUTPUTS</span></span>

### <span data-ttu-id="56208-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="56208-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="56208-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="56208-125">NOTES</span></span>

## <span data-ttu-id="56208-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56208-126">RELATED LINKS</span></span>
