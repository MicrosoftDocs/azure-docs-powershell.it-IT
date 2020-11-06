---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 196E1AC9-A1E2-47D2-A3C1-535EFE439EE8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 1bfe5d721930288c65a18be8ccba2ebfe2f90484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515963"
---
# <span data-ttu-id="6ec15-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec15-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="6ec15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ec15-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec15-103">Imposta i criteri di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="6ec15-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ec15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ec15-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ec15-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ec15-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec15-106">Il cmdlet **set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** imposta i criteri di conservazione a lungo termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="6ec15-106">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="6ec15-107">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="6ec15-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="6ec15-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ec15-108">EXAMPLES</span></span>

## <span data-ttu-id="6ec15-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ec15-109">PARAMETERS</span></span>

### <span data-ttu-id="6ec15-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ec15-110">-DatabaseName</span></span>
<span data-ttu-id="6ec15-111">Specifica il nome del database SQL per cui questo cmdlet imposta un criterio.</span><span class="sxs-lookup"><span data-stu-id="6ec15-111">Specifies the name of the SQL Database for which this cmdlet sets a policy.</span></span>

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

### <span data-ttu-id="6ec15-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec15-112">-ResourceGroupName</span></span>
<span data-ttu-id="6ec15-113">Specifica il nome del gruppo di risorse che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="6ec15-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="6ec15-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ec15-114">-ResourceId</span></span>
<span data-ttu-id="6ec15-115">Specifica l'ID di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ec15-115">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec15-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6ec15-116">-ServerName</span></span>
<span data-ttu-id="6ec15-117">Specifica il server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="6ec15-117">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="6ec15-118">-Stato</span><span class="sxs-lookup"><span data-stu-id="6ec15-118">-State</span></span>
<span data-ttu-id="6ec15-119">Specifica uno stato.</span><span class="sxs-lookup"><span data-stu-id="6ec15-119">Specifies a state.</span></span>

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

### <span data-ttu-id="6ec15-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ec15-120">-Confirm</span></span>
<span data-ttu-id="6ec15-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ec15-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ec15-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ec15-122">-WhatIf</span></span>
<span data-ttu-id="6ec15-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ec15-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ec15-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ec15-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ec15-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec15-125">-DefaultProfile</span></span>
<span data-ttu-id="6ec15-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec15-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ec15-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec15-127">CommonParameters</span></span>
<span data-ttu-id="6ec15-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ec15-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec15-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec15-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec15-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ec15-130">INPUTS</span></span>

## <span data-ttu-id="6ec15-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ec15-131">OUTPUTS</span></span>

## <span data-ttu-id="6ec15-132">Note</span><span class="sxs-lookup"><span data-stu-id="6ec15-132">NOTES</span></span>

## <span data-ttu-id="6ec15-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ec15-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ec15-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ec15-134">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="6ec15-135">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="6ec15-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
