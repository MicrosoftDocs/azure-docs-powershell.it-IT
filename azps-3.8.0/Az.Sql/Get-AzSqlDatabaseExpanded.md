---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019511"
---
# <span data-ttu-id="a0d55-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="a0d55-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="a0d55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0d55-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d55-103">Ottiene un database e i relativi valori di proprietà espanse.</span><span class="sxs-lookup"><span data-stu-id="a0d55-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="a0d55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0d55-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d55-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0d55-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d55-106">Il cmdlet **Get-AzSqlDatabaseExpanded** ottiene un database e i relativi valori di proprietà espansi.</span><span class="sxs-lookup"><span data-stu-id="a0d55-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="a0d55-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d55-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a0d55-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0d55-108">EXAMPLES</span></span>

### <span data-ttu-id="a0d55-109">Esempio 1: ottenere un oggetto di database con informazioni su Service Tier Advisor</span><span class="sxs-lookup"><span data-stu-id="a0d55-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a0d55-110">Questo comando restituisce il database con proprietà espanse che contengono le informazioni di Advisor del livello di servizio.</span><span class="sxs-lookup"><span data-stu-id="a0d55-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="a0d55-111">Esempio 2: elencare gli oggetti di database tramite filtri</span><span class="sxs-lookup"><span data-stu-id="a0d55-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="a0d55-112">Questo comando restituisce l'oggetto di database espanso per tutti i database in Server01 che iniziano con "database".</span><span class="sxs-lookup"><span data-stu-id="a0d55-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="a0d55-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0d55-113">PARAMETERS</span></span>

### <span data-ttu-id="a0d55-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0d55-114">-DatabaseName</span></span>
<span data-ttu-id="a0d55-115">Specifica il nome del database da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a0d55-115">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d55-116">-DefaultProfile</span></span>
<span data-ttu-id="a0d55-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a0d55-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0d55-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d55-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0d55-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="a0d55-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a0d55-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a0d55-120">-ServerName</span></span>
<span data-ttu-id="a0d55-121">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="a0d55-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a0d55-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0d55-122">-Confirm</span></span>
<span data-ttu-id="a0d55-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d55-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d55-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d55-124">-WhatIf</span></span>
<span data-ttu-id="a0d55-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d55-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d55-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d55-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d55-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d55-127">CommonParameters</span></span>
<span data-ttu-id="a0d55-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d55-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d55-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0d55-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d55-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0d55-130">INPUTS</span></span>

### <span data-ttu-id="a0d55-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a0d55-131">System.String</span></span>

## <span data-ttu-id="a0d55-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0d55-132">OUTPUTS</span></span>

### <span data-ttu-id="a0d55-133">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="a0d55-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="a0d55-134">Note</span><span class="sxs-lookup"><span data-stu-id="a0d55-134">NOTES</span></span>

## <span data-ttu-id="a0d55-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0d55-135">RELATED LINKS</span></span>

[<span data-ttu-id="a0d55-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a0d55-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
