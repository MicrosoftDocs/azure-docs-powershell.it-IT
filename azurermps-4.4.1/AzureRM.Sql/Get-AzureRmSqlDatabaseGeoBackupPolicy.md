---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: b8f7d04a709ebb14ed6a7a76cffab556c13d26ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688223"
---
# <span data-ttu-id="4d06a-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4d06a-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="4d06a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d06a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d06a-103">Ottiene un criterio di Geo backup del database.</span><span class="sxs-lookup"><span data-stu-id="4d06a-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d06a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d06a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d06a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d06a-105">DESCRIPTION</span></span>
<span data-ttu-id="4d06a-106">Il cmdlet **Get-AzureRmSqlDatabaseGeoBackupPolicy** ottiene i criteri di backup Geo registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="4d06a-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="4d06a-107">Questa è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="4d06a-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="4d06a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d06a-108">EXAMPLES</span></span>

## <span data-ttu-id="4d06a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d06a-109">PARAMETERS</span></span>

### <span data-ttu-id="4d06a-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4d06a-110">-DatabaseName</span></span>
<span data-ttu-id="4d06a-111">Specifica il nome del database per cui questo cmdlet ottiene i criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="4d06a-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="4d06a-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d06a-112">-ResourceGroupName</span></span>
<span data-ttu-id="4d06a-113">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="4d06a-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="4d06a-114">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4d06a-114">-ServerName</span></span>
<span data-ttu-id="4d06a-115">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="4d06a-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4d06a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d06a-116">-DefaultProfile</span></span>
<span data-ttu-id="4d06a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d06a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d06a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d06a-118">CommonParameters</span></span>
<span data-ttu-id="4d06a-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d06a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d06a-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d06a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d06a-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d06a-121">INPUTS</span></span>

## <span data-ttu-id="4d06a-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d06a-122">OUTPUTS</span></span>

## <span data-ttu-id="4d06a-123">Note</span><span class="sxs-lookup"><span data-stu-id="4d06a-123">NOTES</span></span>

## <span data-ttu-id="4d06a-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d06a-124">RELATED LINKS</span></span>

[<span data-ttu-id="4d06a-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4d06a-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="4d06a-126">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4d06a-126">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)