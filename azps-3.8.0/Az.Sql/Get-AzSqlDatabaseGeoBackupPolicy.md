---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: d69d6c2976e71183fed07e2c18adc730d8ea6e61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019504"
---
# <span data-ttu-id="69c23-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="69c23-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="69c23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69c23-102">SYNOPSIS</span></span>
<span data-ttu-id="69c23-103">Ottiene un criterio di Geo backup del database.</span><span class="sxs-lookup"><span data-stu-id="69c23-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="69c23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69c23-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c23-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69c23-105">DESCRIPTION</span></span>
<span data-ttu-id="69c23-106">Il cmdlet **Get-AzSqlDatabaseGeoBackupPolicy** ottiene i criteri di backup Geo registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="69c23-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="69c23-107">Questa è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="69c23-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="69c23-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69c23-108">EXAMPLES</span></span>

## <span data-ttu-id="69c23-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69c23-109">PARAMETERS</span></span>

### <span data-ttu-id="69c23-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69c23-110">-DatabaseName</span></span>
<span data-ttu-id="69c23-111">Specifica il nome del database per cui questo cmdlet ottiene i criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="69c23-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69c23-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c23-112">-DefaultProfile</span></span>
<span data-ttu-id="69c23-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="69c23-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69c23-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c23-114">-ResourceGroupName</span></span>
<span data-ttu-id="69c23-115">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="69c23-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="69c23-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="69c23-116">-ServerName</span></span>
<span data-ttu-id="69c23-117">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="69c23-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="69c23-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c23-118">CommonParameters</span></span>
<span data-ttu-id="69c23-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c23-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c23-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69c23-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c23-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69c23-121">INPUTS</span></span>

### <span data-ttu-id="69c23-122">System. String</span><span class="sxs-lookup"><span data-stu-id="69c23-122">System.String</span></span>

## <span data-ttu-id="69c23-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69c23-123">OUTPUTS</span></span>

### <span data-ttu-id="69c23-124">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="69c23-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="69c23-125">Note</span><span class="sxs-lookup"><span data-stu-id="69c23-125">NOTES</span></span>

## <span data-ttu-id="69c23-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69c23-126">RELATED LINKS</span></span>

[<span data-ttu-id="69c23-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="69c23-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="69c23-128">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="69c23-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
