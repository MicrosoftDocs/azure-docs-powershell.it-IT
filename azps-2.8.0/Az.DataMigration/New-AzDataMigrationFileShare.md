---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: cc09f7ac0a5f4378c65700cd9681118200d629ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674732"
---
# <span data-ttu-id="1381b-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="1381b-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="1381b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1381b-102">SYNOPSIS</span></span>
<span data-ttu-id="1381b-103">Crea l'oggetto FileShare per il servizio di migrazione del database di Azure, che specifica la condivisione di rete locale a cui eseguire il backup del database di origine.</span><span class="sxs-lookup"><span data-stu-id="1381b-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="1381b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1381b-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1381b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1381b-105">DESCRIPTION</span></span>
<span data-ttu-id="1381b-106">Il cmdlet New-AzDataMigrationFileShare crea l'oggetto FileShare che specifica la condivisione di rete locale in cui il servizio di migrazione del database di Azure può eseguire i backup del database di origine.</span><span class="sxs-lookup"><span data-stu-id="1381b-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="1381b-107">L'account del servizio che usa l'istanza di SQL Server di origine deve avere privilegi di scrittura per questa condivisione di rete.</span><span class="sxs-lookup"><span data-stu-id="1381b-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="1381b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1381b-108">EXAMPLES</span></span>

### <span data-ttu-id="1381b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1381b-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="1381b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1381b-110">PARAMETERS</span></span>

### <span data-ttu-id="1381b-111">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="1381b-111">-Credential</span></span>
<span data-ttu-id="1381b-112">Credenziali per accedere alla condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1381b-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="1381b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1381b-113">-DefaultProfile</span></span>
<span data-ttu-id="1381b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1381b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1381b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1381b-115">-Path</span></span>
<span data-ttu-id="1381b-116">Percorso condivisione file.</span><span class="sxs-lookup"><span data-stu-id="1381b-116">File share path.</span></span>

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

### <span data-ttu-id="1381b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1381b-117">CommonParameters</span></span>
<span data-ttu-id="1381b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1381b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1381b-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1381b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1381b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1381b-120">INPUTS</span></span>

### <span data-ttu-id="1381b-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1381b-121">None</span></span>

## <span data-ttu-id="1381b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1381b-122">OUTPUTS</span></span>

### <span data-ttu-id="1381b-123">Microsoft. Azure. Management. DataMigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="1381b-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="1381b-124">Note</span><span class="sxs-lookup"><span data-stu-id="1381b-124">NOTES</span></span>

## <span data-ttu-id="1381b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1381b-125">RELATED LINKS</span></span>