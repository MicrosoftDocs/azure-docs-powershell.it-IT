---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 2bf632e0135031a9bc2454ac200cbe7aa40bef3c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019495"
---
# <span data-ttu-id="a36de-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="a36de-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="a36de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a36de-102">SYNOPSIS</span></span>
<span data-ttu-id="a36de-103">Ottiene i collegamenti di Geo-replica tra un database SQL di Azure e un gruppo di risorse o SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a36de-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="a36de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a36de-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a36de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a36de-105">DESCRIPTION</span></span>
<span data-ttu-id="a36de-106">Il cmdlet **Get-AzSqlDatabaseReplicationLink** sostituisce il cmdlet **Get-AzSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="a36de-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="a36de-107">Ottiene tutti i collegamenti di Geo-replica tra il database SQL di Azure specificato e un gruppo di risorse o un server AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="a36de-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="a36de-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a36de-108">EXAMPLES</span></span>

## <span data-ttu-id="a36de-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a36de-109">PARAMETERS</span></span>

### <span data-ttu-id="a36de-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a36de-110">-DatabaseName</span></span>
<span data-ttu-id="a36de-111">Specifica il nome del database SQL per cui recuperare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="a36de-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="a36de-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36de-112">-DefaultProfile</span></span>
<span data-ttu-id="a36de-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a36de-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a36de-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a36de-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a36de-115">Specifica il nome del gruppo di risorse a cui è assegnato il partner.</span><span class="sxs-lookup"><span data-stu-id="a36de-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

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

### <span data-ttu-id="a36de-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a36de-116">-PartnerServerName</span></span>
<span data-ttu-id="a36de-117">Specifica il nome di Azure SQL Server per il partner.</span><span class="sxs-lookup"><span data-stu-id="a36de-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36de-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a36de-118">-ResourceGroupName</span></span>
<span data-ttu-id="a36de-119">Specifica il nome del gruppo di risorse Azure per il database per cui recuperare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="a36de-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="a36de-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a36de-120">-ServerName</span></span>
<span data-ttu-id="a36de-121">Specifica il nome del database di SQL Server per il quale recuperare i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="a36de-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="a36de-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a36de-122">-Confirm</span></span>
<span data-ttu-id="a36de-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a36de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a36de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a36de-124">-WhatIf</span></span>
<span data-ttu-id="a36de-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a36de-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a36de-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a36de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a36de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36de-127">CommonParameters</span></span>
<span data-ttu-id="a36de-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a36de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36de-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a36de-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36de-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a36de-130">INPUTS</span></span>

### <span data-ttu-id="a36de-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a36de-131">System.String</span></span>

## <span data-ttu-id="a36de-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a36de-132">OUTPUTS</span></span>

### <span data-ttu-id="a36de-133">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="a36de-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="a36de-134">Note</span><span class="sxs-lookup"><span data-stu-id="a36de-134">NOTES</span></span>

## <span data-ttu-id="a36de-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a36de-135">RELATED LINKS</span></span>

[<span data-ttu-id="a36de-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a36de-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
