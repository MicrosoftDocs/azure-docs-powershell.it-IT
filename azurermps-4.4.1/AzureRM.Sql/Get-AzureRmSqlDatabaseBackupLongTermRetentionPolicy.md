---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512863"
---
# <span data-ttu-id="072a4-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="072a4-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="072a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="072a4-102">SYNOPSIS</span></span>
<span data-ttu-id="072a4-103">Ottiene un database di criteri di conservazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="072a4-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="072a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="072a4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="072a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="072a4-105">DESCRIPTION</span></span>
<span data-ttu-id="072a4-106">Il cmdlet **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** ottiene i criteri di conservazione a lungo termine registrati nel database.</span><span class="sxs-lookup"><span data-stu-id="072a4-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="072a4-107">Il criterio è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="072a4-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="072a4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="072a4-108">EXAMPLES</span></span>

## <span data-ttu-id="072a4-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="072a4-109">PARAMETERS</span></span>

### <span data-ttu-id="072a4-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="072a4-110">-DatabaseName</span></span>
<span data-ttu-id="072a4-111">Specifica il nome del database SQL per cui questo cmdlet ottiene un criterio.</span><span class="sxs-lookup"><span data-stu-id="072a4-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="072a4-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072a4-112">-ResourceGroupName</span></span>
<span data-ttu-id="072a4-113">Specifica il nome del gruppo di risorse che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="072a4-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="072a4-114">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="072a4-114">-ServerName</span></span>
<span data-ttu-id="072a4-115">Specifica il server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="072a4-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="072a4-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="072a4-116">-Confirm</span></span>
<span data-ttu-id="072a4-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="072a4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="072a4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="072a4-118">-WhatIf</span></span>
<span data-ttu-id="072a4-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="072a4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="072a4-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="072a4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="072a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072a4-121">-DefaultProfile</span></span>
<span data-ttu-id="072a4-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="072a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="072a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072a4-123">CommonParameters</span></span>
<span data-ttu-id="072a4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="072a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072a4-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="072a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072a4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="072a4-126">INPUTS</span></span>

## <span data-ttu-id="072a4-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="072a4-127">OUTPUTS</span></span>

## <span data-ttu-id="072a4-128">Note</span><span class="sxs-lookup"><span data-stu-id="072a4-128">NOTES</span></span>

## <span data-ttu-id="072a4-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="072a4-129">RELATED LINKS</span></span>

[<span data-ttu-id="072a4-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="072a4-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="072a4-131">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="072a4-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
