---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 993d7ef8958e96cebcd104d25550e860cdfd1853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519690"
---
# <span data-ttu-id="5cb25-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="5cb25-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="5cb25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cb25-102">SYNOPSIS</span></span>
<span data-ttu-id="5cb25-103">Ottiene i collegamenti di Geo-replica tra un database SQL di Azure e un gruppo di risorse o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5cb25-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cb25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cb25-104">SYNTAX</span></span>

### <span data-ttu-id="5cb25-105">ByDatabaseName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5cb25-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cb25-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="5cb25-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cb25-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cb25-107">DESCRIPTION</span></span>
<span data-ttu-id="5cb25-108">Il cmdlet **Get-AzureRMSqlDatabaseReplicationLink** sostituisce il cmdlet **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="5cb25-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="5cb25-109">Ottiene tutti i collegamenti di Geo-replica tra il database SQL di Azure specificato e un gruppo di risorse o un server AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="5cb25-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="5cb25-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cb25-110">EXAMPLES</span></span>

## <span data-ttu-id="5cb25-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cb25-111">PARAMETERS</span></span>

### <span data-ttu-id="5cb25-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5cb25-112">-DatabaseName</span></span>
<span data-ttu-id="5cb25-113">Specifica il nome del database SQL per cui recuperare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="5cb25-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="5cb25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cb25-114">-DefaultProfile</span></span>
<span data-ttu-id="5cb25-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5cb25-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cb25-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb25-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="5cb25-117">Specifica il nome del gruppo di risorse a cui è assegnato il partner.</span><span class="sxs-lookup"><span data-stu-id="5cb25-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cb25-118">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="5cb25-118">-PartnerServerName</span></span>
<span data-ttu-id="5cb25-119">Specifica il nome di Azure SQL Server per il partner.</span><span class="sxs-lookup"><span data-stu-id="5cb25-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb25-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cb25-120">-ResourceGroupName</span></span>
<span data-ttu-id="5cb25-121">Specifica il nome del gruppo di risorse Azure per il database per cui recuperare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="5cb25-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="5cb25-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5cb25-122">-ServerName</span></span>
<span data-ttu-id="5cb25-123">Specifica il nome del database di SQL Server per il quale recuperare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="5cb25-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="5cb25-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5cb25-124">-Confirm</span></span>
<span data-ttu-id="5cb25-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cb25-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb25-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cb25-126">-WhatIf</span></span>
<span data-ttu-id="5cb25-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cb25-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cb25-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cb25-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cb25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb25-129">CommonParameters</span></span>
<span data-ttu-id="5cb25-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cb25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb25-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb25-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb25-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cb25-132">INPUTS</span></span>

### <span data-ttu-id="5cb25-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5cb25-133">System.String</span></span>

## <span data-ttu-id="5cb25-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cb25-134">OUTPUTS</span></span>

### <span data-ttu-id="5cb25-135">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="5cb25-135">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="5cb25-136">Note</span><span class="sxs-lookup"><span data-stu-id="5cb25-136">NOTES</span></span>

## <span data-ttu-id="5cb25-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cb25-137">RELATED LINKS</span></span>

[<span data-ttu-id="5cb25-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="5cb25-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
