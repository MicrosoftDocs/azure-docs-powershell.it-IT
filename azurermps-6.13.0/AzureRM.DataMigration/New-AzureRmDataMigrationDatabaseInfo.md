---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688430"
---
# <span data-ttu-id="2e6cd-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2e6cd-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="2e6cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6cd-103">Crea l'oggetto DatabaseInfo per il servizio di migrazione del database di Azure, che specifica l'origine del database per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e6cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e6cd-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e6cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e6cd-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6cd-106">Il cmdlet New-AzureRmDataMigrationDatabaseInfo crea l'oggetto DatabaseInfo che specifica l'istanza del database di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="2e6cd-107">Il nome del database viene considerato come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="2e6cd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e6cd-108">EXAMPLES</span></span>

### <span data-ttu-id="2e6cd-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e6cd-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="2e6cd-110">Nell'esempio precedente viene creato un nuovo oggetto DatabaseInfo per il database di origine **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="2e6cd-111">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="2e6cd-112">Puoi confermare lo stato di accesso usando il cmdlet Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="2e6cd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e6cd-113">PARAMETERS</span></span>

### <span data-ttu-id="2e6cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6cd-114">-DefaultProfile</span></span>
<span data-ttu-id="2e6cd-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e6cd-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2e6cd-116">-SourceDatabaseName</span></span>
<span data-ttu-id="2e6cd-117">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-117">Source Database Name.</span></span>

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

### <span data-ttu-id="2e6cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6cd-118">CommonParameters</span></span>
<span data-ttu-id="2e6cd-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6cd-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6cd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6cd-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e6cd-121">INPUTS</span></span>

### <span data-ttu-id="2e6cd-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2e6cd-122">None</span></span>

## <span data-ttu-id="2e6cd-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e6cd-123">OUTPUTS</span></span>

### <span data-ttu-id="2e6cd-124">Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2e6cd-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="2e6cd-125">Note</span><span class="sxs-lookup"><span data-stu-id="2e6cd-125">NOTES</span></span>

## <span data-ttu-id="2e6cd-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e6cd-126">RELATED LINKS</span></span>
