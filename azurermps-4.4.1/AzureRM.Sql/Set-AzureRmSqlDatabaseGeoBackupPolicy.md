---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2cf85aac2d301653787bdf227db1cd187a887986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512827"
---
# <span data-ttu-id="4254a-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4254a-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="4254a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4254a-102">SYNOPSIS</span></span>
<span data-ttu-id="4254a-103">Imposta un criterio di Geo backup del database.</span><span class="sxs-lookup"><span data-stu-id="4254a-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4254a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4254a-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4254a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4254a-105">DESCRIPTION</span></span>
<span data-ttu-id="4254a-106">Il cmdlet **set-AzureRmSqlDatabaseGeoBackupPolicy** imposta i criteri di backup Geo registrati in un database.</span><span class="sxs-lookup"><span data-stu-id="4254a-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="4254a-107">Questa è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="4254a-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="4254a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4254a-108">EXAMPLES</span></span>

## <span data-ttu-id="4254a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4254a-109">PARAMETERS</span></span>

### <span data-ttu-id="4254a-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4254a-110">-DatabaseName</span></span>
<span data-ttu-id="4254a-111">Specifica il nome del database per cui questo cmdlet imposta i criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="4254a-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="4254a-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4254a-112">-ResourceGroupName</span></span>
<span data-ttu-id="4254a-113">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="4254a-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="4254a-114">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4254a-114">-ServerName</span></span>
<span data-ttu-id="4254a-115">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="4254a-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4254a-116">-Stato</span><span class="sxs-lookup"><span data-stu-id="4254a-116">-State</span></span>
<span data-ttu-id="4254a-117">Specifica lo stato dei criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="4254a-117">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="4254a-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4254a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4254a-119">Abilitato</span><span class="sxs-lookup"><span data-stu-id="4254a-119">Enabled</span></span> 
- <span data-ttu-id="4254a-120">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="4254a-120">Disabled</span></span>

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

### <span data-ttu-id="4254a-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4254a-121">-Confirm</span></span>
<span data-ttu-id="4254a-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4254a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4254a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4254a-123">-WhatIf</span></span>
<span data-ttu-id="4254a-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4254a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4254a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4254a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4254a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4254a-126">-DefaultProfile</span></span>
<span data-ttu-id="4254a-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4254a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4254a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4254a-128">CommonParameters</span></span>
<span data-ttu-id="4254a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4254a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4254a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4254a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4254a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4254a-131">INPUTS</span></span>

## <span data-ttu-id="4254a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4254a-132">OUTPUTS</span></span>

## <span data-ttu-id="4254a-133">Note</span><span class="sxs-lookup"><span data-stu-id="4254a-133">NOTES</span></span>

## <span data-ttu-id="4254a-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4254a-134">RELATED LINKS</span></span>

[<span data-ttu-id="4254a-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="4254a-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="4254a-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4254a-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

