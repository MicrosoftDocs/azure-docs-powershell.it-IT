---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2358383cd7cfdbf547ae14476e788d6919baacd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507919"
---
# <span data-ttu-id="7b30b-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="7b30b-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="7b30b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b30b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b30b-103">Ottiene un database eliminato che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="7b30b-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b30b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b30b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b30b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b30b-105">DESCRIPTION</span></span>
<span data-ttu-id="7b30b-106">Il cmdlet **Get-AzureRMSqlDeletedDatabaseBackup** ottiene un backup di database SQL eliminato specificato che è possibile ripristinare o tutti i backup eliminati che è possibile ripristinare.</span><span class="sxs-lookup"><span data-stu-id="7b30b-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="7b30b-107">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="7b30b-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7b30b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b30b-108">EXAMPLES</span></span>

### <span data-ttu-id="7b30b-109">Esempio 1: ottenere tutti i backup di database eliminati in un server</span><span class="sxs-lookup"><span data-stu-id="7b30b-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="7b30b-110">Questo comando ottiene tutti i backup del database eliminati in un server.</span><span class="sxs-lookup"><span data-stu-id="7b30b-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="7b30b-111">Esempio 2: ottenere un backup del database eliminato specificato</span><span class="sxs-lookup"><span data-stu-id="7b30b-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="7b30b-112">Questo comando ottiene il backup del database eliminato per ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="7b30b-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="7b30b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b30b-113">PARAMETERS</span></span>

### <span data-ttu-id="7b30b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7b30b-114">-DatabaseName</span></span>
<span data-ttu-id="7b30b-115">Specifica il nome del database.</span><span class="sxs-lookup"><span data-stu-id="7b30b-115">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b30b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b30b-116">-DefaultProfile</span></span>
<span data-ttu-id="7b30b-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7b30b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b30b-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="7b30b-118">-DeletionDate</span></span>
<span data-ttu-id="7b30b-119">Specifica la data, come oggetto **DateTime** , che il database è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="7b30b-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="7b30b-120">Per ottenere un oggetto **DateTime** , usa il cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="7b30b-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b30b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b30b-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b30b-122">Specifica il nome del gruppo di risorse a cui è assegnato il server.</span><span class="sxs-lookup"><span data-stu-id="7b30b-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7b30b-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7b30b-123">-ServerName</span></span>
<span data-ttu-id="7b30b-124">Specifica il nome del server di database.</span><span class="sxs-lookup"><span data-stu-id="7b30b-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="7b30b-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b30b-125">-Confirm</span></span>
<span data-ttu-id="7b30b-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b30b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b30b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b30b-127">-WhatIf</span></span>
<span data-ttu-id="7b30b-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b30b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b30b-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b30b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b30b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b30b-130">CommonParameters</span></span>
<span data-ttu-id="7b30b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b30b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b30b-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b30b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b30b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b30b-133">INPUTS</span></span>

### <span data-ttu-id="7b30b-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b30b-134">None</span></span>
<span data-ttu-id="7b30b-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7b30b-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b30b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b30b-136">OUTPUTS</span></span>

## <span data-ttu-id="7b30b-137">Note</span><span class="sxs-lookup"><span data-stu-id="7b30b-137">NOTES</span></span>

## <span data-ttu-id="7b30b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b30b-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b30b-139">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7b30b-139">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="7b30b-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="7b30b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
