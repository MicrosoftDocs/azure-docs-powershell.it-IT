---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686999"
---
# <span data-ttu-id="a1e1e-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a1e1e-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="a1e1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e1e-103">Crea un nuovo punto di ripristino da cui è possibile ripristinare un database SQL.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1e1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1e1e-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1e1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e1e-106">Il cmdlet **New-AzureRmSqlDatabaseRestorePoint** crea un nuovo punto di ripristino da cui è possibile ripristinare un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="a1e1e-107">Questo cmdlet è attualmente supportato dal servizio SQL Server Datawarehouse in Azure SQL database.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="a1e1e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1e1e-108">EXAMPLES</span></span>

### <span data-ttu-id="a1e1e-109">Esempio 1: creare un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="a1e1e-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="a1e1e-110">Questo comando crea un punto di ripristino per il database SQL di Azure e restituisce i dettagli del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="a1e1e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1e1e-111">PARAMETERS</span></span>

### <span data-ttu-id="a1e1e-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a1e1e-112">-DatabaseName</span></span>
<span data-ttu-id="a1e1e-113">Specifica il nome del database SQL.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e1e-114">-DefaultProfile</span></span>
<span data-ttu-id="a1e1e-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a1e1e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1e1e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e1e-116">-ResourceGroupName</span></span>
<span data-ttu-id="a1e1e-117">Specifica il nome del gruppo di risorse a cui è assegnato il database SQL.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1e-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="a1e1e-118">-RestorePointLabel</span></span>
<span data-ttu-id="a1e1e-119">Specifica l'etichetta del punto di ripristino per facilitare l'identificazione.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1e-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a1e1e-120">-ServerName</span></span>
<span data-ttu-id="a1e1e-121">Specifica il nome del server AzureSQL che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1e-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1e1e-122">-Confirm</span></span>
<span data-ttu-id="a1e1e-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e1e-124">-WhatIf</span></span>
<span data-ttu-id="a1e1e-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1e1e-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e1e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e1e-127">CommonParameters</span></span>
<span data-ttu-id="a1e1e-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e1e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e1e-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e1e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e1e-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1e1e-130">INPUTS</span></span>

## <span data-ttu-id="a1e1e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1e1e-131">OUTPUTS</span></span>

## <span data-ttu-id="a1e1e-132">Note</span><span class="sxs-lookup"><span data-stu-id="a1e1e-132">NOTES</span></span>

## <span data-ttu-id="a1e1e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1e1e-133">RELATED LINKS</span></span>
