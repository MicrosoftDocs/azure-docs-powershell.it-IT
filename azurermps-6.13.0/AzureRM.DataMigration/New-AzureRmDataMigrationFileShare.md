---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationFileShare.md
ms.openlocfilehash: b34665f9402186a1e07671e614d91fee59f565d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520219"
---
# <span data-ttu-id="49146-101">New-AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="49146-101">New-AzureRmDataMigrationFileShare</span></span>

## <span data-ttu-id="49146-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49146-102">SYNOPSIS</span></span>
<span data-ttu-id="49146-103">Crea l'oggetto FileShare per il servizio di migrazione del database di Azure, che specifica la condivisione di rete locale a cui eseguire il backup del database di origine.</span><span class="sxs-lookup"><span data-stu-id="49146-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49146-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49146-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49146-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49146-105">DESCRIPTION</span></span>
<span data-ttu-id="49146-106">Il cmdlet New-AzureRmDataMigrationFileShare crea l'oggetto FileShare che specifica la condivisione di rete locale in cui il servizio di migrazione del database di Azure può eseguire i backup del database di origine.</span><span class="sxs-lookup"><span data-stu-id="49146-106">The New-AzureRmDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="49146-107">L'account del servizio che usa l'istanza di SQL Server di origine deve avere privilegi di scrittura per questa condivisione di rete.</span><span class="sxs-lookup"><span data-stu-id="49146-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="49146-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49146-108">EXAMPLES</span></span>

### <span data-ttu-id="49146-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49146-109">Example 1</span></span>
```
PS C:\> New-AzureRmDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="49146-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49146-110">PARAMETERS</span></span>

### <span data-ttu-id="49146-111">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="49146-111">-Credential</span></span>
<span data-ttu-id="49146-112">Credenziali per accedere alla condivisione file.</span><span class="sxs-lookup"><span data-stu-id="49146-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49146-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49146-113">-DefaultProfile</span></span>
<span data-ttu-id="49146-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49146-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49146-115">-Path</span><span class="sxs-lookup"><span data-stu-id="49146-115">-Path</span></span>
<span data-ttu-id="49146-116">Percorso condivisione file.</span><span class="sxs-lookup"><span data-stu-id="49146-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49146-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49146-117">CommonParameters</span></span>
<span data-ttu-id="49146-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49146-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49146-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49146-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49146-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49146-120">INPUTS</span></span>

### <span data-ttu-id="49146-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="49146-121">None</span></span>

## <span data-ttu-id="49146-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49146-122">OUTPUTS</span></span>

### <span data-ttu-id="49146-123">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="49146-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="49146-124">Note</span><span class="sxs-lookup"><span data-stu-id="49146-124">NOTES</span></span>

## <span data-ttu-id="49146-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49146-125">RELATED LINKS</span></span>
