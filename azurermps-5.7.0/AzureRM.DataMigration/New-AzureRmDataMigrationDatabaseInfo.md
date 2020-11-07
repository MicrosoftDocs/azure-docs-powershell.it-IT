---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687921"
---
# <span data-ttu-id="d2e5a-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d2e5a-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="d2e5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e5a-103">Crea l'oggetto DatabaseInfo per il servizio di migrazione del database di Azure, che specifica l'origine del database per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2e5a-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="d2e5a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="d2e5a-106">Il cmdlet New-AzureRmDataMigrationDatabaseInfo crea l'oggetto DatabaseInfo che specifica l'istanza del database di origine di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="d2e5a-107">Il nome del database viene considerato come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="d2e5a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2e5a-108">EXAMPLES</span></span>

### <span data-ttu-id="d2e5a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d2e5a-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="d2e5a-110">Nell'esempio precedente viene creato un nuovo oggetto DatabaseInfo per il database di origine **AdventureWorks2016**.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="d2e5a-111">Questo script presuppone che tu abbia già eseguito l'accesso all'account di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="d2e5a-112">Puoi confermare lo stato di accesso usando il cmdlet Get-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="d2e5a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2e5a-113">PARAMETERS</span></span>

### <span data-ttu-id="d2e5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e5a-114">-DefaultProfile</span></span>
<span data-ttu-id="d2e5a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="d2e5a-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2e5a-116">-Confirm</span></span>
<span data-ttu-id="d2e5a-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e5a-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d2e5a-118">-SourceDatabaseName</span></span>
<span data-ttu-id="d2e5a-119">Nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e5a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e5a-120">-WhatIf</span></span>
<span data-ttu-id="d2e5a-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e5a-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2e5a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d2e5a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2e5a-123">INPUTS</span></span>

### <span data-ttu-id="d2e5a-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d2e5a-124">None</span></span>


## <span data-ttu-id="d2e5a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2e5a-125">OUTPUTS</span></span>

### <span data-ttu-id="d2e5a-126">Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d2e5a-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="d2e5a-127">Note</span><span class="sxs-lookup"><span data-stu-id="d2e5a-127">NOTES</span></span>

## <span data-ttu-id="d2e5a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2e5a-128">RELATED LINKS</span></span>


