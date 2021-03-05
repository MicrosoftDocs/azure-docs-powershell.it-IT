---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: d7eb52a9da5866b4aed280f1ac35651800c67a25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995874"
---
# <span data-ttu-id="bb44e-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="bb44e-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="bb44e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb44e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb44e-103">Ottiene un database e i relativi valori di proprietà espansi.</span><span class="sxs-lookup"><span data-stu-id="bb44e-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="bb44e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb44e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb44e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb44e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb44e-106">Il **cmdlet Get-AzSqlDatabaseExpanded** ottiene un database e i relativi valori di proprietà espansi.</span><span class="sxs-lookup"><span data-stu-id="bb44e-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="bb44e-107">Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.</span><span class="sxs-lookup"><span data-stu-id="bb44e-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bb44e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb44e-108">EXAMPLES</span></span>

### <span data-ttu-id="bb44e-109">Esempio 1: Ottenere un oggetto di database con informazioni su Service Tier Advisor</span><span class="sxs-lookup"><span data-stu-id="bb44e-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="bb44e-110">Questo comando restituisce il database con proprietà espanse contenenti le informazioni sull'consulente del livello di servizio.</span><span class="sxs-lookup"><span data-stu-id="bb44e-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="bb44e-111">Esempio 2: Elencare oggetti di database con i filtri</span><span class="sxs-lookup"><span data-stu-id="bb44e-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="bb44e-112">Questo comando restituisce l'oggetto di database espanso per tutti i database in Server01 che iniziano con "Database".</span><span class="sxs-lookup"><span data-stu-id="bb44e-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="bb44e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb44e-113">PARAMETERS</span></span>

### <span data-ttu-id="bb44e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb44e-114">-DatabaseName</span></span>
<span data-ttu-id="bb44e-115">Specifica il nome del database da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bb44e-115">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="bb44e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb44e-116">-DefaultProfile</span></span>
<span data-ttu-id="bb44e-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bb44e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb44e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb44e-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb44e-119">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="bb44e-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bb44e-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb44e-120">-ServerName</span></span>
<span data-ttu-id="bb44e-121">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="bb44e-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="bb44e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb44e-122">-Confirm</span></span>
<span data-ttu-id="bb44e-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb44e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb44e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb44e-124">-WhatIf</span></span>
<span data-ttu-id="bb44e-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb44e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb44e-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb44e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb44e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb44e-127">CommonParameters</span></span>
<span data-ttu-id="bb44e-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb44e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb44e-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bb44e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb44e-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb44e-130">INPUTS</span></span>

### <span data-ttu-id="bb44e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bb44e-131">System.String</span></span>

## <span data-ttu-id="bb44e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb44e-132">OUTPUTS</span></span>

### <span data-ttu-id="bb44e-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="bb44e-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="bb44e-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb44e-134">NOTES</span></span>

## <span data-ttu-id="bb44e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb44e-135">RELATED LINKS</span></span>

[<span data-ttu-id="bb44e-136">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="bb44e-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
