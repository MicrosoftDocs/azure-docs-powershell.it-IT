---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 18ae68a4ecf0a2511f992e42a202468193022d6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994907"
---
# <span data-ttu-id="d6087-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d6087-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="d6087-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6087-102">SYNOPSIS</span></span>
<span data-ttu-id="d6087-103">Imposta i criteri di backup geografici del database.</span><span class="sxs-lookup"><span data-stu-id="d6087-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="d6087-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6087-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6087-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6087-105">DESCRIPTION</span></span>
<span data-ttu-id="d6087-106">Il **cmdlet Set-AzSqlDatabaseGeoBackupPolicy** imposta il criterio di backup geografico registrato su un database.</span><span class="sxs-lookup"><span data-stu-id="d6087-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="d6087-107">Si tratta di una risorsa di Backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="d6087-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="d6087-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6087-108">EXAMPLES</span></span>

## <span data-ttu-id="d6087-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6087-109">PARAMETERS</span></span>

### <span data-ttu-id="d6087-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6087-110">-DatabaseName</span></span>
<span data-ttu-id="d6087-111">Specifica il nome del database per cui questo cmdlet imposta i criteri di backup geografici.</span><span class="sxs-lookup"><span data-stu-id="d6087-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="d6087-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6087-112">-DefaultProfile</span></span>
<span data-ttu-id="d6087-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d6087-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6087-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6087-114">-ResourceGroupName</span></span>
<span data-ttu-id="d6087-115">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="d6087-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d6087-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6087-116">-ServerName</span></span>
<span data-ttu-id="d6087-117">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="d6087-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d6087-118">-State</span><span class="sxs-lookup"><span data-stu-id="d6087-118">-State</span></span>
<span data-ttu-id="d6087-119">Specifica lo stato dei criteri di backup geografici.</span><span class="sxs-lookup"><span data-stu-id="d6087-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="d6087-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="d6087-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d6087-121">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d6087-121">Enabled</span></span> 
- <span data-ttu-id="d6087-122">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="d6087-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6087-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6087-123">-Confirm</span></span>
<span data-ttu-id="d6087-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6087-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6087-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6087-125">-WhatIf</span></span>
<span data-ttu-id="d6087-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6087-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6087-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6087-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6087-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6087-128">CommonParameters</span></span>
<span data-ttu-id="d6087-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6087-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6087-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6087-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6087-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6087-131">INPUTS</span></span>

### <span data-ttu-id="d6087-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d6087-132">System.String</span></span>

## <span data-ttu-id="d6087-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6087-133">OUTPUTS</span></span>

### <span data-ttu-id="d6087-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d6087-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="d6087-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6087-135">NOTES</span></span>

## <span data-ttu-id="d6087-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6087-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6087-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d6087-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="d6087-138">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="d6087-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

